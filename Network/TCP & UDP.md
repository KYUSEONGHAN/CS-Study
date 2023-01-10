![](https://nordvpn.com/wp-content/uploads/blog-tcp-vs-udp.svg)

- TCP
    - Transmission Control Protocol
    - 연결지향형 프로토콜
    - 인터넷상에서 데이터를 메세지의 형태로 보내기 위해 IP와 함께 사용하는 프로토콜
    - 특징
        1. 연결형 서비스로 가상 회선 방식을 제공
        2. 3-way handshaking과정을 통해 연결을 설정하고 4-way handshaking을 통해 해제한다.
        3. 흐름 제어 및 혼잡 제어
        4. 높은 신뢰성을 보장
        5. UDP에 비해 속도가 느리다.
        6. 전이중(full-duplex), 점대정(point-to-point) 방식
        
- UDP
    - 데이터를 데이터그램 단위로 처리하는 프로토콜
    - 특징
        1. 비연결형 서비스로 데이터그램 방식을 제공
        2. 정보를 주고 받을 때, 정보를 보내거나 받는다는 신호절차를 거치지 않는다.
        3. 최소한의 오류만 검출
        4. 신뢰성이 낮다.
        5. TCP보다 속도가 빠르다.
        6. 예: 스트리밍 실시간 서비스
        
- TCP vs UDP

    |프로토콜 종류|TCP|UDP|
    |---|-----|-----|
    |연결 방식|연결형|비연결형|
    |패킷 교환 방식|가상 회선 방식|데이터그램 방식|
    |전송 순서|순서 보장|순서가 바뀔 수 있다|
    |수신 여부 확인|확인|확인 안함|
    |통신 방식|1:1|1:1, 1:N, N:N|
    |신뢰성|높다|낮다|
    |속도|느림|빠름|
    
- 참고 자료 

[https://nordvpn.com/blog/tcp-or-udp-which-is-better/](https://nordvpn.com/blog/tcp-or-udp-which-is-better/)