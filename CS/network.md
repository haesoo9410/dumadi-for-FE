# 🌏 네트워크

### TCP

- 연결형 통신에 사용되는 프로토콜을 의미합니다.
- 3 way handshake 를 사용하여 신뢰성을 가지며, 1:1 통신만 가능합니다.

### UDP

- 비연결형 통신에 사용되는 프로토콜을 의미합니다.
- 확인 작업을 거치지 않아 데이터를 효율적으로 빠르게 보낼 수 있으며, 다대다 통신도 가능합니다.

### 3-way-handshake

- TCP프로토콜로 네트워크 연결 시 연결요청을 의미하는 SYN과 확인응답을 의미하는 ACK를 3번 주고받는 것을 의미합니다.
- 송신측은 연결확립 요청을 위해 SYN을 보내면 수신측을 허가응답과 전송허가 요청을 위해 SYN ACK를 보내고, 마지막으로 송신측이 ACK를 보내어 연결이 수립됩니다.

### HTTP 0.9

- 이후 버전과 차이를 두기위해 0.9 버전이라는 명칭이 붙었습니다.
- GET요청만 가능했으며 응답은 파일내용 그 자체입니다.

### HTTP/1.0

- 버전정보와 상태코드가 추가되었습니다.
- Content Type이 추가되어 다른 파일도 보낼 수 있게 되었습니다.

### HTTP/1.1

- 커넥션이 재사용될 수 있도록 하였습니다.
- 파이프라이닝이 추가되어 응답이 끝나기 전에 다음데이터를 미리 요청할 수 있습니다.

### HTTP/2.0

- 하나의 TCP연결에 여러개의 스트림을 이용할 수 있게 되었습니다.
- 내용은 바이너리데이터로, 헤더는 압축하여 네트워크 속도를 개선하였습니다.

### HTTP/3.0

- UDP위에서 동작하는 구글의 QUIC프로토콜을 사용합니다.
- 3 way handshake 와 TLS handshake를 결합하고, 패킷 손실 감지에 걸리는 시간도 감축시켰습니다.

### http vs https

- http는 서버 클라이언트 모델에서 데이터를 주고 받기 위한 프로토콜입니다.
- https는 http에 암호화가 추가되었습니다.

### https의 암호화방식

- 인증서를 활용한 공개기 키반으로 서버와 클라이언트간 검증이 이루어집니다.
- TLS핸드셰이크 마지막에 대칭키를 제작하여 이를 통해 데이터를 주고받습니다.

### 실시간 통신 방식 종류

- 폴링, 롱폴링, 웹소켓, SSE(Server Send Event)로 실시간 웹 통신을 진행합니다.
- 웹소켓은 http 프로토콜을 준수하지 않습니다.
