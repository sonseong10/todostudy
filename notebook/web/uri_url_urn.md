# URI vs URL vs URN ?

요즘에는 URL 대신 URI라는 표현을 더 많이 사용합니다. 보통 URL과 URI는 동일한 의미로 쓰이고 있지만, 엄밀하게 차이점을 구분하자면 다음과 같습니다.

**URI (Uniform Resource Identifier)** : 네트워크 상에 존재하는 자원을 구분하는 `식별자(ID)`로서 의미가 강합니다.

**URL (Uniform Resource Locator)** : 네트워크 상에 존재하는 `자원의 위치`를 말합니다. 즉 자원의 어디에 있는지 나타내는 Where의 개념입니다.

**URN (Uniform Resource Name)** : 자원의 이름을 나타내는 말입니다. 즉 자원이 무엇인지를 말하는 What의 개념으로 이해할 수 있습니다. URN은 `서로 중복되지 않는 유일한 값`이어야 합니다.

![URI_URL_URN](https://img1.daumcdn.net/thumb/R800x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F2637274E52C96C5514)

## URI 구문

![URI](https://t1.daumcdn.net/cfile/tistory/255D3F4755AF337B1B)

### 스킴 혹은 프로토콜

![protocol](https://mdn.mozillademos.org/files/8013/mdn-url-protocol@x2.png)

일반적으로 그것은 HTTP 프로토콜이거나 혹은 보안이 적용된 버전인 HTTPS일 겁니다. 웹은 이들 중 하나를 반드시 필요로 하며, 이외의 브라우저들은 mailto: (메일 클라이언트를 열기 위해) 혹은 파일 전송을 다루기 위한 ftp: 와 같은 다른 프로토콜도 처리하는 방법들이 있습니다.

|    이름     | 설명                              |
| :---------: | --------------------------------- |
|    data     | 데이터 URI                        |
|    file     | 호스트가 지정하는 파일 이름들     |
|     ftp     | 파일 전송 프로토콜                |
| http(https) | 하이퍼텍스트 전송 프로토콜 (보안) |
|   mailto    | 전자 메일 주소                    |
|     ssh     | 보안 쉘                           |
|     tel     | 전화번호                          |

### 도메인 이름(Authority)

![domain](https://mdn.mozillademos.org/files/8015/mdn-url-domain@x2.png)

DNS혹은 권한입니다. 그것은 어떤 웹 서버가 요청을 받게 될지를 나타냅니다. 혹은, IP address를 직접 사용할 수도 있지만, 불편하므로 웹에서 그리 자주 사용되지는 않습니다.

### 포트

![port](https://mdn.mozillademos.org/files/8017/mdn-url-port@x2.png)

웹 서버 상의 리소스에 접근하는데 사용되는 기술적인 "문(gate)"을 나타냅니다. 리소스에 접근하기 위한 권한을 얻기 위해 웹 서버가 HTTP 프로토콜의 `표준 포트(HTTP는 80, HTTPS는 443)를 사용하는 경우 일반적으로 생략`됩니다. 그게 아니라면 `포트 입력은 필수`입니다.

### 경로

![path](https://mdn.mozillademos.org/files/8019/mdn-url-path@x2.png)

웹 서버 상의 리소스 경로입니다. 초기 웹에서, 이와 같은 경로는 웹 서버 상에 있는 파일의 실제 위치를 나타냈었습니다. 오늘날에는, 대부분 물리적인 실제 위치를 사용하지 않고 `웹 서버에 의해 다뤄지는 추상화를 사용`합니다.

### 파라미터

![parameter](https://mdn.mozillademos.org/files/8021/mdn-url-parameters@x2.png)

웹 서버에 제공되는 추가적인 파라메터입니다. 이런 파라메터들은 & 심볼로 구분되는 키/값 쌍의 목록입니다. 각각의 웹 서버는 파라메터들을 따르는 자신만의 규칙을 가집니다.

### 프래그먼트

![anchor](https://mdn.mozillademos.org/files/8023/mdn-url-anchor@x2.png)

리소스 내에서의 "북마크"의 한 종류를 나타내며, 브라우저에게 그런 "북마크된" 지점에 위치한 컨텐츠를 보여주기 위한 방법을 제공합니다. 예를 들자면, HTML 문서 상에서, 브라우저는 앵커가 정의된 지점으로 스크롤될 것입니다;

**More**

[Link MDN](https://developer.mozilla.org/ko/docs/Web/HTTP/Basics_of_HTTP/Identifying_resources_on_the_Web)

[Link Site](https://mygumi.tistory.com/139)
