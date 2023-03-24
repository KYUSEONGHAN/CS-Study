![](https://assets.gcore.pro/blog/dns-servers-what-they-are-and-how-they-work/1631695472.jpg)

## DNS
- Domain Name System
- TCP/IP 네트워크 상에서 사람이 기억하기 쉽게 문자로 만들어진 도메인을 숫자로 된 IP 주소로 바꾸는 서버를 DNS라고 한다.

## 면접 질문: DNS 동작 과정
- 브라우저에서 Nesite.com을 검색한 뒤, 사용하고 있는 통신사인 KT DNS 서버에게 도메인 주소에 해당하는 IP 주소를 요청한다. (브라우저 기본 DNS 설정은 통신사 DNS 서버이다.)
- ISP 서버에서는 캐시 데이터가 없다는 것을 확인하고 Root DNS 서버에게 어디로 가야 하는지 요청한다. (만약 캐시가 있다면 8번 단계로 건너뛴다.)
- Root DNS 서버는 TLD DNS 서버 주소만 관리하므로 ***.com 도메인을 보고, com 최상위 도메인을 관리하는 TLD DNS 서버 주소를 안내한다.
- ISP 서버는 com 서버에게 어디로 가야 하는지 다시 요청한다.
- com 서버는 가비아 DNS 서버가 해당 도메인이 관리되고 있다는 사실을 확인하고, 가비아 DNS 서버 주소를 안내한다.
- ISP 서버는 가비아 서버에게 다시 요청한다.
- 가비아 서버는 요청 받은 도메인 주소의 IP 주소를 확인하고 알려준다. 동시에 ISP 서버는 해당 정보를 캐시로 기록한다.
- ISP 서버는 브라우저에게 알아 낸 IP 주소를 안내한다.

## 참고자료 출처
[https://steady-coding.tistory.com/523](https://steady-coding.tistory.com/523)