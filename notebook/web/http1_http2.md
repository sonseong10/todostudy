# HTTP

HTTP는 웹상에서 클라이언트와 웹서버간 통신을 위한 프로토콜 입니다.

## HTTP1 vs HTTP2

![](https://miro.medium.com/max/700/1*m3TqLQ2sXE51-6b8rNLsmA.gif)

## HTTP/1.1

- 연결당 하나의 요청과 응답을 처리하기 때문에 동시 전송 문제와 다수의 리소스를 처리하기에 속도와 성능 이슈가 존재합니다.
- HOL(Head Of Line) Blocking (특정 응답 지연)
  > HTTP/1.1의 사양상의 제한으로 클라이언트의 리퀘스트의 순서와 서버의 응답순서는 동기화해야 됨
- RTT(Round Trip TIme) 증가 합니다.(양방향 지연)
- 헤더 정보가 많아집니다. (특히 쿠키)
  > http/1.1의 헤더에는 많은 메타 정보들이 저장되어 있음.
  > 사용자가 방문한 웹페이지는 다수의 http 요청이 발생하게 되는데 이 경우 매 요청시 마다 중복된 헤더 값을 전송하게 되며 각 도메인에 설정된 쿠키 정보도 매 요청시 마다 헤더에 포함되어 전송

### 문제점들을 해결하기 위한 UI 개발자와 프론트엔드 개발자의 노력

- 이미지 스프라이트
  여러 개의 이미지를 하나의 이미지로 합쳐서 관리하는 이미지 (ex. 아이콘)(사용할 때는 좌표 범위로 구분하여 사용)
- 도메인 샤딩
  리소스를 여러 개의 도메인 으로 나누어 저장하여, 페이지 로드 시간을 빠르게하는 일종의 트릭 혹은 방법.
  - 여러 개의 도메인으로 나누어진 리소스를 다운받기 때문에 browser 는 더 많은 리소스를 한번에 더 많이 받을 수 있습니다.
  - 최신 브라우저들은 보통 한 도메인에 약 6개의 동시 다운로드를 제공합니다.
  - 이 갯수를 초과하는 페이지의 경우 초과하는 갯수를 6으로 나눈 도메인에 리소스를 뿌려두면, 병렬적으로 리소스들을 다운받을 수 있습니다.
- CSS/JavaScript 압축
- Data URI

## HTTP/2.0

- SDPY(구글 제안 프로토콜) 기반으로 HTTP/2.0 등장했습니다.
- HTTP/2.0은 HTTP/1.1이 느려서 버전을 개선한 것입니다.

### HTTP/2.0이 빠른 이유

- Multiplexed Streams (한 커넥션에 여러개의 메세지를 동시에 주고 받을 수 있음)
- 요청이 커넥션 상에서 다중화 되므로 HOL(Head Of Line) Blocking 이 발생하지 않음
- Stream Prioritization (요청 리소스간 의존관계를 설정)
- Header Compression (Header 정보를 HPACK 압축 방식을 이용하여 압축 전송)
- Server Push (HTML문서 상에 필요한 리소스를 클라이언트 요청없이 보내줄 수 있음)
- 프로토콜 협상 메커니즘 - 프로토콜 선택, 예. HTTP / 1.1, HTTP / 2 또는 기타.
- HTTP / 1.1과의 높은 수준의 호환성 - 메소드, 상태 코드, URI 및 헤더 필드
- 페이지 로딩 속도 향상

**More**

[Link youtube](https://www.youtube.com/watch?v=WfA1uDAgXf8)

[HTTP3 MDN](https://developer.mozilla.org/en-US/docs/Glossary/HTTP_3)
