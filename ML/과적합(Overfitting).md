![](https://www.datarobot.com/wp-content/uploads/2018/03/Screen-Shot-2018-03-22-at-11.22.15-AM-e1527613915658.png)

## 모델 학습 - underfitting, overfitting
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FD837m%2FbtqEng4RauO%2FfagMDQiBdeERGOhYbVTvk0%2Fimg.png)
- 만약 동일한 점들이 주어지고 이 점을 대표할 수 있는 함수(곡선)을 추정하는 경우에서, 가운데가 optimize하다고 한다면
- 왼쪽은 지나친 단순화로 인해 에러가 많이 발생해 underfitting이라고 한다.
- 오른쪽은 너무 정확하게 표현한 나머지 training data에 대한 정확도는 좋지만 실제 test에서는 에러가 날 수 있는 상황이라 overfitting이라 한다.
- 모델은 과대적합과 과소적합이 발생하지 않도록 설계하는 것이 중요하다.

## Overfitting
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fos0E5%2FbtqEmoQh8Z6%2FtU2unf6BnFNmwb4Yxssoik%2Fimg.png)
- 과대적합, 과적합
- 학습 데이터(Training Set)에 대해 과하게 학습된 상황
- 특정 데이터에 너무 정확하게 일치하여 추가 데이터나 미래 관찰에대해 잘 예측하지 못하는 것
- 따라서, 학습 데이터 이외의 데이터에 대해선 모델이 잘 동작하지 못한다.
- 학습 데이터가 부족하거나, 데이터의 특성에 비해 모델이 너무 복잡한 경우 발생.
- Training Set에 대한 Loss는 계속 떨어지는데, Test Set에 대한 Loss는 감소하다가 다시 증가한다.

## Overfitting 감지할려면
- (1) K-fold 교차 검증 이용
- (2) test set에 대한 성능이 Train set보다 훨씬 낮게 나온다면 overfitting이 나온다고 판단할 수 있다.

## Overfitting 방지법
- 프루닝
- 정규화 (데이터를 일정한 규칙에 따라 변형하여 이용하기 쉽게 만듬)
- 앙상블링
- 데이터증강
- cross validation(교차 검증, 주어진 데이터를 일부는 학습을 시켜 모델을 만드는데 사용하고 일부는 모델을 검증하는데 사용하는것)
- cross validation ex: 전체 데이터의 70%는 훈련 데이터(train data)로, 30%는 테스트 데이터(test data)로 사용.

## Model Capacity
- 과대적합의 원인 중 하나
- 모델이 더 복잡한 형상을 나타낼 수 있는 정도를 의미

## Overfitting 해결책
- 학습 데이터 늘리기(data argumentation)
- L1/L2 정규화
- Dropout (학습할 때 일부 뉴런을 끄고 학습)
- Model Capacity 낮추기 (모델이 학습 데이터에 비해 과하게 복잡하지 않도록 layer 개수를 줄이는 등 모델을 간단하게 만듬)

## Underfitting
- 과소적합
- 데이터가 너무 적거나 학습이 제대로 이루어지지 않은 상태.
- Overfitting과 반대되는 상태
- 언더피팅의 경우 머신러닝에서는 흔히 Bias(편향)가 많다고 한다.

## 참고자료 출처
[https://22-22.tistory.com/35](https://22-22.tistory.com/35)
[https://aws.amazon.com/ko/what-is/overfitting/](https://aws.amazon.com/ko/what-is/overfitting/)
[https://m.blog.naver.com/dhstar914/221272078843](https://m.blog.naver.com/dhstar914/221272078843)