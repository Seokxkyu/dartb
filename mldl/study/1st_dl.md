# 7-1 인공 신경망

## 패선 MNIST
```python
from tensorflow import keras

(train_input, train_target), (test_input, test_target) = keras.datasets.fashion_mnist.load_data()

print(train_input.shape, train_target.shape)
print(test_input.shape, test_target.shape)

import matplotlib.pyplot as plt
fig, axs = plt.subplots(1, 10, figsize=(10,10))
for i in range(10):
    axs[i].imshow(train_input[i], cmap='gray_r')
    axs[i].axis('off')
plt.show()
```

### 로지스틱 회귀
- 픽셀값 0 ~ 255 사이 값을 가지므로, 255로 나누어 스케일링해서 변환
- 경사 하강법 사용한 로지스틱 회귀 모델 (epoch 지정)
- SGDClassifier, Scikit-learn의 알고리즘은 다중 분류를 여러 개의 이진 분류로 나누어 사용 (One Versus All)
- loss=log로 지정


## 인공 신경망
- 경사하강법 사용한 로지스틱 회귀와 동일한 모델 (출력층 1개 있는 경우)
- 입력층 = 입력 데이터 자체
- 입력층의 각 픽셀은 10개의 서로 다른 뉴런(출력층)을 계산해내기 위해 서로 다른 가중치 w를 곱함
- 가중치 곱하고 절편 b가 더해짐 (선형 함수)

### Tensorflow vs Pytorch
```python
from tensorflow import keras
```

### 케라스 모델 만들기
- 딥러닝 데이터 많기 때문에 교차검증 잘 수행하지 않음
- 계산비용 많이 들고, 검증 안정

```python
import tensorflow.keras as keras
from sklearn.model_selection import train_test_split

train_scaled, val_scaled, train_target, val_target = train_test_split(
    train_scaled, train_target, test_size=0.2, random_state=42)

print(train_scaled.shape, train_target.shape)  # (48000, 784) (48000,)
print(val_scaled.shape, val_target.shape)      # (12000, 784) (12000,)

# 10개 밀집층 지정 fully connected layer
# 출력층 유닛 개수는 항상 클래스 (분류) 개수와 동일
# 활성함수로 다중 분류 위한 softmax 함수 이용 (이진 분류 시 softmax 대신 시그모이드)
# input_shape은 sample의 크기로 지정
dense = keras.layers.Dense(10, activation='softmax', input_shape=(784,))

# dense 객체 전달
model = keras.Sequential(dense)
```

### 모델 설정
- 손실 함수 정의하는 게 가장 중요
- 추가적인 측정 지표 metrics로 지정 가능 (정확도)
> `sparse` :  target 출력해보면 정수형인데, 그대로 사용할 수 없고, 출력층 10개 유닛에서 softmax 함수 거쳐서 나온 10개의 확률 값 (로그 변환) X 타깃 값 = 원핫 인코딩

```python
# sparse 지정 (타깃 값 정수형)
model.compile(loss='sparse_categorical_crossentropy', metrics='accuracy')

print(train_target[:10])
```

- 이진 분류 `binary_crossentropy`
- 다중 분류 `categorical_crossentropy`

### 모델 훈련
```python
model.fit(train_scaled, train_target, epochs=5)

model.evaluate(val_scaled, val_target)
```
- epoch 올라갈수록 모델 성능 상승


# 7-2 심층 신경망
## 2개의 층
- 입력층 (784개 뉴런) 미고려
- 은닉층 (100개 뉴런)
    - 활성화 함수 거쳐서 비선형으로 변형 (선형식 합쳐지지 않도록)
    - sigmoid, relu 등 활용 (keras 모듈 포함)

- 출력층 (10개 뉴런) 
    - 다중 분류: `소프트맥스(softmax) 함수`
    - 이진 분류: `시그모이드(sigmoid) 함수`

```python
# 은닉층
dense1 = keras.layers.Dense(100, activation='sigmoid', input_shape=(784,))

# 출력층
dense2 = keras.layers.Dense(10, activation='softmax')

model = keras.Sequential([dense1, dense2])
model.summary()
```

## 층을 추가하는 다른 방법
```python
import tensorflow.keras as keras

# 객체화 하자마자 Sequential 메서드로 바로 전달
model = keras.Sequential([
    keras.layers.Dense(100, activation='sigmoid', input_shape=(784,), name='hidden'),
    keras.layers.Dense(10, activation='softmax', name='output')
], name='패션 MNIST 모델')

# add 메서드 사용
model = keras.Sequential()
model.add(keras.layers.Dense(100, activation='sigmoid', input_shape=(784,)))
model.add(keras.layers.Dense(10, activation='softmax'))
```

## ReLU 함수와 Flatten 층
```python
# Flatten 층 추가 (입력 크기가 28x28인 이미지 데이터를 1차원으로 변환하는 전처리 수행)
model.add(keras.layers.Flatten(input_shape=(28, 28)))

# Dense 층 추가 (활성화 함수로 ReLU 사용)
model.add(keras.layers.Dense(100, activation='relu'))

# 출력 층 추가 (10개의 클래스를 분류, softmax 활성화 함수 사용)
model.add(keras.layers.Dense(10, activation='softmax'))
```
- `sigmoid 활성함수`의 단점
    - 선형 출력값이 너무 커지거나 작아지면, sigmoid 함수 값의 변화가 매우 작아짐 (포화)
    - 모델이 빠르게 신경망 모델이 대응하여 학습하기 어려움

- `ReLU 활성 함수`
    - 뉴런의 선형 출력 값이 0보다 크면 z값을 직접 출력하고, 0보다 작으면 버려버리는 함수


### Optimizer 옵티마이저 (최적화)
- 확률적 경사하강법 `sgd`
- 미니배치 경사하강법 `batch_size=32`
```python
# 문자열 전달
model.compile(optimizer='sgd', loss='sparse_categorical_crossentropy', metrics='accuracy')

# 객체 전달 
sgd = keras.optimizer.SGD()
model.compile(optimizer='sgd', loss='sparse_categorical_crossentropy', metrics='accuracy')

# 객체 전달 (매개변수 값 바꿀 때 사용)
sgd = keras.optimizer.SGD(learning_rate=0.1)

# 모멘텀, 네스테로프 모멘텀
sgd = keras.optimizer.SGD(momentum=0.9, nesterov=True)

model = keras.Sequential()
model.add(keras.layers.Flatten(input_shape=(28,28)))
model.add(keras.layers.Dense(100, activation='relu'))
model.add(keras.layers.Dense(10, activation='softmax'))

# Adam 매개변수로 전달
model.compile(optimizer='adam', loss='sparse_categorical_crossentropy', metrics='accuracy')
model.fit(train_scaled, train_target, epochs=5)

model.evaluate(val_scaled, val_target)
```

#### 기본 경사하강법 옵티마이저
- `모멘텀 (Momentum)`
- `네스테로프 모멘텀 (Nesterov Momentum)`

#### 적응적 학습률 옵티마이저
- `RMSprop`
- `Adam`
- `Adagrad`

## 심층 신경망 정리
- RandomForest의 앙상블 방식과 비교하여 개별 트리의 독립적인 학습이 이루어지는 것과 대조적으로, 은닉층의 (유닛)뉴런들이 개별로 훈련되는게 아니라 한번에 `동시에` 훈련

- 전통적인 머신러닝 모델과 비교하여, 신경망 모델은 이미지, 텍스트 같은 비정형화된 데이터에 대해 잘 학습 (특성을 다음 층으로 잘 전달) 
