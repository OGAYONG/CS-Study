모든 개발자를 위한 HTTP 웹 기본 지식

## 인터넷 네트워크

#### IP 프로토콜의 한계

* 비연결성
  * 패킷을 받을 대상이 없거나 서비스 불능상태여도 패킷 전송됨
* 비신뢰성
  * 중간에 패킷이 사라지면?
  * 패킷이 순서대로 안오면?
* 프로그램 구분
  * 같은 IP를 사용하는 서버에서 통신하는 어플리케이션이 둘 이상일 경우?

#### TCP/UDP

**TCP** : 전송제어 프로토콜 (Transmission Control Protocol)

- 연결지향 : 3 way handshake
- 데이터 전달 보증
- 순서 보장

** 3 way handshake

1. SYN -> 접속 요청
2. SYN + ACK <-  요청 수락 및 역 요청
3. ACK -> 요청 수락

**UDP** : 사용자 데이터그램 프로토콜

- 단순하고 빠름

  

#### DNS 필요 이유

- 기억하기 어렵다
- 변경될 수 있다





## URI / 웹 브라우저 요청 흐름

#### URI(Uniform Resource Identifier) = URL(Resource Locator) + URN(Resource Name)

**웹브라우저 요청 흐름**

