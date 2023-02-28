![](https://www.goldenplanet.co.kr/data/data/2021/11/2021-11-11_16-33-12-50935-1636615992.png)

## RNN
- Recurrent Neural Network, 순환신경망
- 인공 신경망의 한 종류로서, 내부의 순환 구조가 포함되어 있기 때문에 시간에 의존적이거나 순차적인 데이터 학습에 활용된다.
- RNN은 입력값과 출력값이 시퀀스의 길이에 관계없이 받아들일 수 있는 구조이기 때문에 언어 모델링, 기계 번역, 음성 인식, 이미지 캡션 생성 등으로 다양하게 사용 가능하다.
- 특징
    - 신경망에 은닉 상태 및 루프가 있다
    - 루프 구조를 통해 신경망은 은닉 상태에 과거의 정보를 저장하고 시퀀스에 대해 연산할 수 있다.

## RNN의 한계점 및 대책
- RNN은 시계열 데이터의 장기 의존 관계를 학습하는 것에 한계가 있다.
- 길이가 길어짐에 따라 신경망을 하나 통과할 때마다 기울기 값이 조금씩 작아져서, 이전 시각 t까지 역전파 되기 전에 0이 되어 소멸하게 되는 기울기 소실 또는 반대로 기울기가 너무 커지는 기울기 폭발 문제가 일어나기 때문이다.
- 기울기 클리핑이라는 기법을 사용하면 기울기 폭발을 해결할 수 있다.
- RNN 계층의 신경망 구성에 게이트를 추가하면 기울기 소멸을 해결할 수 있다.

## 참고자료 출처
[https://www.goldenplanet.co.kr/our_contents/blog?number=857](https://www.goldenplanet.co.kr/our_contents/blog?number=857)