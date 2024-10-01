# 7-3 신경망 모델 훈련
## 손실 곡선
```python
model.compile(loss='sparse_categorical_crosssentropy', metrics='accuracy')
history = model.fit(train_scaled, train_target, epochs=5, verbose=0)
print(history.history.keys())
dict_keys(['loss', 'accuracy'])

plt.plot(history.history['loss'])
plt.xlabel('epoch')
plt.ylabel('loss')
plt.show()

plt.plot(history.history['accuracy'])
plt.xlabel('epoch')
plt.ylabel('accuracy')
plt.show()
```

## 더 많은 에포크