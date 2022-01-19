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



### HTTP

HyperText Transfer Protocol

- 모든 것이 http로 전송됨
- HTML, TEXT, IMG
- 음성, 영상, 파일
- JSON, XML

HTTP/1.1?

- 가장 많이 사용.



TCP : HTTP/1.1, HTTP/2

UDP : HTTP/3

HTTP/1.1 주로 사용

HTTP/2, HTTP/3도 점점 증가



HTTP 특징

- 클라이언트 서버 구조
- 무상태 프로토콜(stateless), 비연결성
- HTTP메시지
- 단순함, 확장 가능



무상태 프로토콜

- 서버가 클라이언트의 상태를 보존해주지 않음
- 장점 : 서버 확장성 높음
- 단점 : 클라이언트가 추가 데이터 전송



Stateful, Stateless 차이



Statelss 실무 한계

- 모든 것을 무상태로 설계할수 있는경우/없는경우 공존



HTTP는 비연결성이 기본임



HTTP Persistent Conenections로 문제 해결



Stateless

- 정해진 시간에 발생하는 대용량 트래픽



요청메시지

시작라인

start-line = request-line

request-line = method SP request-target SP HTTP-version CRLF



응답메시지

start-line = HTTP-version SP status-code SP reason-phrase CRLF



API URI



GET : 조회

POST : 처리, 등록

PUT : 리소스 대체 or 생성

PATCH : 변경

DELETE : 리소스 삭제

HEAD : GET과 동일. 메시지 제외하고 상태줄과 헤더만 반환

OPTIONS : 대상 리소스에 대한 통신 가능 옵션을 설명

CONNECT : 대상자원으로 식별되는 서버에 대한 터널을 설정

TRAACE ; 루프백 테스트를 수행

