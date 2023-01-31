![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbU3txF%2FbtrzmkcCO6c%2FPk5JPn4N3ipvyP5ROei2rK%2Fimg.jpg)

## HTTPS
- HTTP + S로, HTTP에 SSL을 더한것이다.
- SSL, secure socket layer
- SSL은 TCP/IP 네트워크에서 통신할 때 사용되는 암호화 기법 프로토콜이다.
- 즉, HTTP를 통해 주고 받는 HTML 정보를 암호화시켜 외부 사용자로부터 데이터를 지키는 것이다.

## 공개키 암호화 방식
- SSL은 공개키 암호화 방식을 이용해서 문서를 보안한다.
- 이 방식의 핵심은 공개키와 개인키가 있는 것이다.
- 공개키는 누구에게나 공개되어 모두가 접근이 가능한 키고, 개인키는 본인을 제외한 누구도 접근이 불가능한 키다.
1. 서버는 공개키와 개인키를 만든다.
2. 믿을만한 저장소와 계약해 두 키를 관리하도록 한다.
3. 저장소(CA)도 자신만의 공개키와 개인키를 가지고 자체 암호화를 하여 SSL 인증서를 발급한다.
4. 클라이언트의 데이터 요청이 들어오면 서버는 CA에서 만든 SSL 인증서를 보내준다.
5. 클라이언트는 CA의 공개키를 이용해 SSL 인증서와 복호화(암호 해독) 한다.
6. SSL 내부의 서버 공개키를 이용해서 암호화하여 인증서를 서버에게 보낸다.
7. 서버는 개인키로 암호화된 인증서를 복호화(암호 해독)하고 다시 암호화하여 클라이언트에게 보낸다.
- 이 같은 방식으로 서버와 클라이언트의 문서를 외부에 노출되지 않도록 한다.

## 참고자료 출처
[https://fomaios.tistory.com/entry/Network-HTTPS%EC%9D%98-%EB%B3%B4%EC%95%88-%EC%9B%90%EB%A6%ACfeat-SSL%EA%B3%B5%EA%B0%9C%ED%82%A4-%EC%95%94%ED%98%B8%ED%99%94-%EB%B0%A9%EC%8B%9D](https://fomaios.tistory.com/entry/Network-HTTPS%EC%9D%98-%EB%B3%B4%EC%95%88-%EC%9B%90%EB%A6%ACfeat-SSL%EA%B3%B5%EA%B0%9C%ED%82%A4-%EC%95%94%ED%98%B8%ED%99%94-%EB%B0%A9%EC%8B%9D)