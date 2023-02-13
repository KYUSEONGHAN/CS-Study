![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FdVfds2%2FbtqLkhbs7T4%2FU97igLNa0nSfvmBPn5BnbK%2Fimg.png)

## Training Set
- 훈련 데이터
- 모델을 학습하는데 사

## Validation Set
- 검정 데이터
- training set으로 만들어진 모델의 성능을 측정하기 위해 사용된다
- 일반적으로 어떤 모델이 가장 데이터에 적합한지 찾아내기 위해서 다양한 파라미터 모델을 사용하게 되며
- 그 중, validaion set으로 가장 성능이 좋았던 모델을 선택한다.

## Test Set
- 테스트 데이터
- Test set(테스트 데이터)은 validation set으로 사용할 모델이 결정 된 후, 마지막으로 딱 한번 해당 모델의 예상되는 성능을 측정하기 위해 사용된다. 
- 이미 validation set은 여러 모델에 반복적으로 사용되었고 그중 운 좋게 성능이 보다 더 뛰어난 것으로 측정되어 모델이 선택되었을 가능성이 있다. 
- 때문에 이러한 오차를 줄이기 위해 한 번도 사용해본 적 없는 test set을 사용하여 최종 모델의 성능을 측정하게 된다.

## Validation set과 Test set의 차이
-  Validation set은 여러 모델들 각각에 적용되어 성능을 측정하며, 최종 모델을 선정하기 위해 사용된다. 
- 반면 test set은 최종 모델에 대해 단 한번 성능을 측정하며, 앞으로 기대되는 성능을 예측하기 위해 사용된다.

## 참고자료 출처
[https://modern-manual.tistory.com/19](https://modern-manual.tistory.com/19)