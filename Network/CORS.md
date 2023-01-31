![](https://blog.kakaocdn.net/dn/bGFCGK/btqzYp0iB4M/TcGaIXZuXiqb9J4Kzhq9I0/img.png)

## CORS
- 브라우저에서는 보안적인 이유로 cross-origin HTTP 요청들을 제한한다.
- 그래서 cross-origin 요청을 하려면 서버의 동의가 필요하다.
- 만약 서버가 동의한다면 브라우저에서는 요청을 허락하고, 동의하지 않는다면 브라우저에서 거절한다.
- 이러한 허락을 구하고 거절하는 메커니즘을 CORS(Cross-Origin Resource Sharing)이라고 부른다.
- 그래서 브라우저에서 cross-origin 요청을 안전하게 할 수 있도록 하는 메커니즘이다.

## cross-origin
- cross-origin은 다음 중 한 가지라도 다른 경우를 말한다.
1. 프로토콜 - http와 https는 프로토콜이 다르다.
2. 도메인 - domain.com과 other-domain.com은 다르다.
3. 포트 번호 - 8080포트와 3000포트는 다르다.

## CORS는 왜 필요한가?
- CORS 없이 모든 곳에서 데이터를 요청할 수 있게 되면, 다른 사이트에서 원래 사이트를 흉내낼 수 있게 된다.
- 예를 들어 기존 사이트와 완전히 동일하게 동작하도록 하여 사용자가 로그인을 하도록 만들고, 로그인했던 세션을 탈취하여 악의적으로 정보를 추출하거나 다른 사람의 정보를 입력하는 등 공격을 할 수 있다.

## 참고자료 출처
[https://hannut91.github.io/blogs/infra/cors](https://hannut91.github.io/blogs/infra/cors)