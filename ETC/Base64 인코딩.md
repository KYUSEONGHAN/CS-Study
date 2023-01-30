## 인코딩
- encoding
- 정보의 형태나 형식을 표준화, 보안, 처리 속도 향상, 저장 공간 절약 등을 위해서 다른 형태나 형식으로 변환하는 처리 혹은 그 처리 방식을 말한다.

## Base64 인코딩
- Binary Data를 Text로 변경하는 Encoding이다.
- 변경하는 방식을 간략하게 설명하면 Binary DataFMF 6 Bit씩 자른 뒤, 6 Bit에 해당하는 문자를 아래 Base64 색인표에서 찾아 치환한다.
![](https://cdn-images-1.medium.com/max/1600/1*jU2iAYGT1FuHN597AiIMuw.png)
- 즉, Base64는 HTML 또는 이메일과 같이 문자를 위한 Media에 Binary Data를 포함해야 될 필요가 있을 때, 포함된 Binary Data가 시스템 독립적으로 동일하게 전송 또는 저장되는걸 보장하기 위해 사용한다.

## 참고자료 출처
[https://effectivesquid.tistory.com/entry/Base64-%EC%9D%B8%EC%BD%94%EB%94%A9%EC%9D%B4%EB%9E%80](https://effectivesquid.tistory.com/entry/Base64-%EC%9D%B8%EC%BD%94%EB%94%A9%EC%9D%B4%EB%9E%80)



