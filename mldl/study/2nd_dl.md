# 7-3 신경망 모델 훈련
## 손실 곡선
```python
model.compile(loss='sparse_categorical_crosssentropy', metrics='accuracy')
history = model.fit(train_scaled, train_target, epochs=5, verbose=0)
print(history.history.keys())
```
```python
dict_keys(['loss', 'accuracy'])
```

![alt text](image-2.png)
```python
plt.plot(history.history['loss'])
plt.xlabel('epoch')
plt.ylabel('loss')
plt.show()
```
![alt text](image-1.png)
```python
plt.plot(history.history['accuracy'])
plt.xlabel('epoch')
plt.ylabel('accuracy')
plt.show()
```



- `history` 객체에는 훈련 측정값이 담겨 있는 `history` 딕셔너리가 들어 있고, 해당 딕셔너리에는 손실 `loss`와 정확도 `accuracy`값 들어 있음
- 에포크보다 손실이 감소하고 정확도 향상

## 더 많은 에포크
### 검증 손실
- 에포크에 대한 과대적합과 과소적합 파악하려면 훈련 세트에 대한 점수 뿐만 아니라 검증 세트에 대한 점수도 필요
- 에포크마다 검증 손실 계산하기 위한 케라스 모델의 `fit()` 메서드에 검증 데이터 전달 

    ![image](image.png)
    > 인공 신경망 모델이 최적화하는 대상은 정확도가 아닌 **손실함수**이므로, 손실 감소에 비례하여 정확도가 높아지지 않는 경우도 있음

    ```python
    model = model_fn()
    model.compile(loss='sparse_categorical_crossentropy', metrics='accuracy')
    history = model.fit(train_scaled, train_target, epochs=20, verbose=0, validation_data(val_scaled, val_target))
    > 검증 세트에 대한 손실은 `val_loss`에 들어 있고 정확도는 `val_accuracy`에 들어 있음
    ```

    ![image](image-3.png)

### 옵티마이저
- 과대적합을 막기 위한 신경망 특화 규제 방법
- `Adam 옵티마이저`는 적응적 학습률을 사용하기 때문에, 에포크가 진행되면서 학습률 크기 조정 가능

    ![image](image-4.png)
    > 열 번째 에포크까지 전반적인 감소 추세 이어지므로, 과대적합 감소


## 드롭아웃
- 훈련 과정에서 층에 있는 일부 뉴런을 랜덤하게 껴서 (즉 뉴런의 출력을 0으로 만들어) 과대 적합을 방지하는 방법

![image](image-5.png)