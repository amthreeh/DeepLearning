# DeepLearning
USW DeepLearning, CNN


## WEEK 9_ CNN

### 합성곱(CNN)
- input 이미지에 filter가 움직이며 내적함.
- Frobenius inner product
- 합성곱층은 함수 tf.nn.conv2d와 클래스 tf.keras.layers.Conv2d로 구현되어 있다.
* filter 형식: FN X H X W X FC 
* Stride: 몇 칸씩 이동하는지
* Padding: 빈칸을 0으로 채워서 해상도를 늘리는 효과
  - padding은 숫자로 지정할 수 없음.
  - padding='SAME': input image와 featuremap의 크기가 동일함.
  - padding='VALID': padding을 진행하지 않음. -> 해상도가 줄어들게됨.
해상도가 줄어들게되면 층을 깊게 쌓을 수가 없기 때문에 padding을 통해 너무 크기가 작아지는것을 줄임.
* MaxPooling: 최대값을 뽑아냄.

- 수평 sobel 필터, 수직 sobel 필터 사용함.
![image](https://github.com/amthreeh/DeepLearning/assets/103898937/a34a4b06-0f53-4464-bb88-5255b7b19c72)

* CNN: 합성곱 -> RELU -> MaxPooling
  -> 특징파악하고 해상도 낮춤을 반복함.
  - 이를 통해 local하게 이미지를 구별함.
  


