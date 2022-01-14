# 심층 신경망 DNN (Deep Neural Network)

## 💡 What is DNN?

> ***입력층(input layer)과 출력층(output layer) 사이에 여러 개의 은닉층(hidden layer)들로 이뤄진 인공신경망 (Artificial Neural Network, ANN)***
> 

![Untitled](https://user-images.githubusercontent.com/63443366/149503693-b87c32e1-5ee0-43f9-b98a-293856fc7354.png)

✅ **복잡한 비선형 관계(non-linear relationship)들을 모델링할 수 있다**

✅ **ANN 문제 해결위해 은닉층 확대**

### 📌 심층 신경망의 목적

> **분류 및 수치예측**
> 

🌟 **이미지 트레이닝이나 문자인식과 같은 분야에서 유용하게 사용**

## 💡 신경망 작동 방법의 종류

> ***Feed-Forward Neural Network(FFN), Backpropagation(역전파), Recurrent Neural Network(RNN)***
> 

### 📌 Feed-Forward Network(FFN)

> **input(입력층)에서 hidden(은닉층)으로 hidden(은닉층)에서 output(출력층)으로 쭉 한 방향으로 흐르는 신경망**
> 

![Untitled 1](https://user-images.githubusercontent.com/63443366/149503731-9d027061-7ae2-4cde-a29e-0bb0f5d2e8de.png)

✅ **오차에 대한 가중치의 조절이 불가능**

✅ **입력층, 은닉층, 출력층까지 순서대로 계산**

### 📌 **Backpropagation(역전파)**

> **내가 뽑고자 하는 Target값과 실제 모델이 계산한 Output이 얼마나 차이 나는지 계산 후 그 오차값을 다시 뒤로 전파해가며 각 노드가 가지고 있는 변수들을 갱신**
> 

![Untitled 2](https://user-images.githubusercontent.com/63443366/149503775-7994c234-b016-4650-adb8-d014aa80449c.png)

🌟 **Weight, bias 변수들을 어떻게 업데이트할 것인가?, 각 노드가 가지고 있는 변수들을 얼만큼 변경할 것인가?**

- ***Chain Rule ( 미분의 연쇄법칙 )***

*Mean Squared Error* 함수를 사용하여 에러 E 구하기

$E = \frac 12 \sum(t_{i} - y_{i})^{2}$

### 📌 **Recurrent Neural Network(RNN)**

> **RNN은 이전에 입력된 데이터의 sequence 정보를 은닉층(hidden state)에 저장해 놓고 나중에 새로운 데이터가 입력이 되면 이전 sequence 정보를 고려하여 결과를 출력**
> 

![Untitled 3](https://user-images.githubusercontent.com/63443366/149503808-f47ee52e-c514-47aa-b16d-57c1b887e76b.png)

***ex ) 언어 모델링  : 언어의 배열에 따라 다음에 나올 단어를 예측할 수 있다***