# What is www, http and https?

| 종류  |               풀네임                |                                            기능                                            |
| :---: | :---------------------------------: | :----------------------------------------------------------------------------------------: |
|  WWW  |           World Wide Web            |                          웹 클라이언트와 서버 간의 통신에 관한 것                          |
| HTTP  |    Hyper Text Transfer Protocol     |                     HTML 문서와 같은 리소스를 가져올 수 있는 통신 규약                     |
| HTTPS | Hyper Text Transfer Protocol Secure | 요청 및 응답 정보를 암호화하는 SSL(Secure Socket Layer)을 이용하여 보안이 보증된 통신 규약 |

![web prosess](https://mdn.mozillademos.org/files/13679/Client-server-chain.png)

http는 **요청(request)** 을 처리하고 **응답(response)** 이라고 하는 답변을 제공합니다 클라이언트와 서버 사이에는 서로 다른 작업을 수행하고게이트웨이나 캐시 등의 역할을 하는 **프록시(proxies)** 라고 하는 수많은 엔티가 있다.

Client: (user = Web browser) 거의 항상 요청(request)을 전담한다.

Server: 클라이언트의 요청에 따라 문서를 서비스하는 서버가 있습니다. 온디맨드 방식으로 문서를 전체 또는 부분적으로 생성하여 응답(response)합니다.

**Proxy의 기능**

| 종류           | 기능                                               |
| -------------- | -------------------------------------------------- |
| caching        | 캐시는 브라우저 캐시처럼 공용 또는 개인일 수 있음  |
| filtering      | ex) 바이러스 백신 검사                             |
| load balancing | 여러 서버가 서로 다른 요청을 처리할 수 있도록 허용 |
| authentication | 다른 리소스에 대한 액세스 제어                     |
| logging        | 이력 정보 저장 허용                                |

more [Link](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)
