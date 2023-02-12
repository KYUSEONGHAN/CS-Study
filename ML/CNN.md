![](https://t1.daumcdn.net/cfile/tistory/9913A0505ECBD00329)

## CNN
- convolution neural network, 합성곱 신경망
- 인간의 시신경을 모방하여 만든 딥러닝 구조 중 하나
- 이미지 처리 분야가 CNN이 나오고부터 엄청나게 빠르게 발전함.
- deep neural network에서 이미지나 영상과 같은 데이터를 처리할 때, 발생하는 문제점을 보완하는 방식 중 하나
- 이미지를 분석하기 위한 패턴을 찾을 때, 유용하며 이미지를 직접 학습하고 패턴을 사용해 이미지를 분류한다.
- 신경망에서 학습을 통해 자동으로 적합한 필터를 생성해주는 특징이 있다.
- 특징 추출 단계 (feature extraction)
    - convolution layer
        - 필터를 통해 이미지의 특징을 추출
    - polling layer: 특징을 강화시키고 이미지의 크기를 줄임
- 이미지 분류 단계 (classification)
    - flatten layer
        - 데이터 타입을 FC 네트워크 형태로 변경.
    - softmax layer
        - classification 수행
- 자율주행, 얼굴인식, 객체인식 등에서 활용

## Convolution
![](https://miro.medium.com/max/850/1*LS6qplIzS5oRWNii2KcWcA.png)
- 합성곱
- 통계, 컴퓨터 비전, 자연어 처리, 이미지 처리, 신호 처리 등 다양한 분야에서 이용되는 방법
- 합성곱 식에서 사용되는 함수 f, g에서 f는 우리가 가지고 있는 본래의 신호, 행렬, 이미지 등이 되기도 한다.
- 이 때, 함수 g는 필터, 가중치 같은걸로 표현되기도 한다.
- 이 두 함수를 합성곱 하면 주어진 신호, 행렬, 이미지를 우리가 원하는 함수로 만들어낼 수 있다.
- 즉, 함수 f가 주어졌을 때, 우리가 원하는 목적에 따라 함수 g를 선정하여 분해, 변환, 필터링 할 수 있다는 장점이 있다.
- 이러한 이유로 합성곱이 딥러닝 분야에서 활발하게 활용되는 것이다.
- 위 설명을 CNN에 섞여서 정리하자면, 조그만 필터로 이미지를 상하좌우 convolution하면서 그 부분의 특징값들을 뽑아낸다.
- 입력에 가까울수록 가장자리(edge), 곡선(curve)와 같은 저수준(low level) 특징을 학습한다.
- 출력에 가까워질수록 질감, 물체 일부분과 같은 고수준 특징을 인식한다.

## Convolution Layer
- 입력 데이터로부터 특징을 추출하는 역할을 수행
- convolution layer: filter + activation function
- filter: 특징 추출
- activation function: filter 값을 비선형 값으로 바꿔주는 활성화 함수

## 참고자료 출처
[https://supermemi.tistory.com/104?category=837542](https://supermemi.tistory.com/104?category=837542)