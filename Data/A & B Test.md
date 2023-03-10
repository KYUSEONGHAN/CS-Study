![](https://velog.velcdn.com/images/cosmos/post/18c38409-7358-458b-b5e0-60506da1dd8f/image.png)

## A/B Test
- A/B 테스트는 기존 서비스(A)와 새로 적용하고 싶은 서비스(B)를 통계적인 방법으로 비교하여 새로운 서비스가 기존 서비스에 비해 정밀 효과가 있는지를 알아보는 방법

## A/B 테스트 방법
- 가설 설정 -> 메트릭 정의 -> 실험 설계 - 결과 도출

## A/B 테스트 단계
1 가설 설정
- 가설 설정에서 가설은 과학적인 방법을 이용하여 참인지 거짓인지를 판별할 수 있는 명제로써 검증하고자 하는 것이 무엇인지를 문장형태로 구체화하는 것이다.
- ex) 다운로드 버튼의 색상을 초록색으로 바꾸면 기존 빨간색일 때보다 더 많은 사용자가 다운로드할 것이다.

2 메트릭 정의
- 가설을 설정했다면 이 가설이 참인지 거짓인지를 보이기 위한 측정 기준이 필요한데 이를 메트릭이라고 한다.
- 메트릭은 검증하고자 하는 가설에 따라 달라진다.
- 메트릭은 하나의 가설에 대해서 두 개 이상이 될 수 있다.

3 실험 설계
- 실험 환경은 검증할 요소 외 다른 요소들은 기존 환경과 모두 동일하게 만들어줘야 한다.
- 그 이유는 검증하고자하는 결과와 바뀐 부분의 연관성을 정확하게 파악하기 위해서이다.
- 실험 환경이 준비가 되었다면 다음은 두 집단을 하나는 기존 환경에 하나는 실험 환경에 배정해야 한다.
- 집단을 배정할 때에는 반드시 랜덤 하게 배정 해주어야 한다.
- 실험 결과에 대한 해석을 정확하게 하기 위해서이다.

4 결과 도출
- 실험 설계가 완ㄹ되면 이제 두 집단에 대하여 미리 정의한 메트릭을 계산한다.
- 통계적으로 유의한 차이가 있다면 우리는 새롭게 적용한 서비스가 기존의 서비스보다 더 낫다고 판단하게 된다.
- 여기에 주로 사용되는 통계적 가설 검정방법은 `2 표본 t-검정`이다.
- 만약 통계적으로 유의한 차이가 없다면 가설 설정에 문제는 없었는지, 실험 설계에서 잘못된 부분은 없었는지, 데이터는 충분히 확보되었는지를 확인하여 다시 가설 검정 절차를 수행.

## A/B 테스트 장단점
- 장점
    - A/B 테스트는 새로운 방식이 과연 기존 방식에 비해서 효과가 있는가에 대한 답을 비교적 빠르게 제공한다는 장점이 있다.
    - 새롭게 적용할 서비스와 기존 서비스를 비교할 수 있는 모든 분야에 적용이 가능
- 단점
    - A/B 테스트는 실험 설계를 잘했다고 가설 검정에서 보고자 했던 결과와 요인 사이에 인과관계를 정확히 알 수 없다는 단점이 있습니다.
    

## 참고문헌 및 출처
[https://zephyrus1111.tistory.com/28](https://zephyrus1111.tistory.com/28)