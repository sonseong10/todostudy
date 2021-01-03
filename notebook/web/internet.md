![web icon](https://logodix.com/logo/2094289.png)

# Web

## How does the internet work?

얕게]

컴퓨터로 통신 하기위해 각각의 컴퓨터를 연결 할 필요가 발생했다.
단일 연결 이후 지역구 나아가 전세계로 통신이 필요해지며
각각의 컴퓨터를 라우터로 연결하고 라우터를 모뎀에 연결하고
ISP를 통해 전세계 사람들과 통신을 할 수 있게 되었다.

Computer >> router >routing> ISP >DNS> 웹서버

깊게]

1. 브라우저를 처음으로 실행시켰을때 홈페이지 또는 첫화면이 나타날 것이다.
2. 만약 접속하고 싶은 홈페이지의 도메인주소를 입력하고 엔터를 친다.
   (ex: https://www.google.com)
3. 작성된 도메인주소는 ISP(인터넷서비스제공자)에게 전달된다.
4. 도메인 주소를 전달받은 ISP 는 회사내 자체적으로 보유하고 있는 DNS 에서 똑같은 도메인명이 존재하는지 찾는다.
5. 찾은 IP주소를 (ex: 172.217.7.23) ISP 에 가져다준다.
6. 그리고 ISP 에서는 전달받은 IP 주소의 메인서버(웹서버)에 문서를 요청한다.
   (우리나라에서 가장가까운 구글서버라고 보면 된다.)
7. 서버는 요청에 맞는 .HTML .CSS .JS 등 의 문서로 ISP 에게 응답한다.
8. 마지막으로 ISP 는 응답받은 문서들을 클라이언트 측에 보낸 후
   브라우저는 전달받은 문서를 차례대로 랜더링하는 과정을 거친다.
9. 화면에 프린트한다.

more [Link](https://developer.mozilla.org/ko/docs/Learn/Common_questions/How_does_the_Internet_work)

## What is www, http and https?

| 종류  |               풀네임                |                                            기능                                            |
| :---: | :---------------------------------: | :----------------------------------------------------------------------------------------: |
|  WWW  |           World Wide Web            |                          웹 클라이언트와 서버 간의 통신에 관한 것                          |
| HTTP  |    Hyper Text Transfer Protocol     |                     HTML 문서와 같은 리소스를 가져올 수 있는 통신 규약                     |
| HTTPS | Hyper Text Transfer Protocol Secure | 요청 및 응답 정보를 암호화하는 SSL(Secure Socket Layer)을 이용하여 보안이 보증된 통신 규약 |

![web prosess](https://mdn.mozillademos.org/files/13679/Client-server-chain.png)

http는 **요청(request)** 을 처리하고 **응답(response)** 이라고 하는 답변을 제공합니다 클라이언트와 서버 사이에는 서로 다른 작업을 수행하고게이트웨이나 캐시 등의 역할을 하는 **프록시(proxies)** 라고 하는 수많은 엔티가 있다.

Client: (user = Web browser) 거의 항상 요청(request)을 전담한다.

Server: 클라이언트의 요청에 따라 문서를 서비스하는 서버가 있습니다. 온디맨드 방식으로 문서를 전체 또는 부분적으로 생성하여 응답(response)합니다.

Proxy의 기능

| 종류           | 기능                                               |
| -------------- | -------------------------------------------------- |
| caching        | 캐시는 브라우저 캐시처럼 공용 또는 개인일 수 있음  |
| filtering      | ex) 바이러스 백신 검사                             |
| load balancing | 여러 서버가 서로 다른 요청을 처리할 수 있도록 허용 |
| authentication | 다른 리소스에 대한 액세스 제어                     |
| logging        | 이력 정보 저장 허용                                |

more [Link](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)

## DNS and how it work?

**DNS (Domain Name System)** 은 찾고있는 웹 사이트를 IP(웹 사이트 주소)와 일치시키는 방법을 제공하는 인터넷의 중심 부분입니다.
노트북, 태블릿, 휴대폰, 웹 사이트 등 인터넷에 연결된 모든 것에는 숫자로 구성된 인터넷 프로토콜(IP) 주소가 있습니다. 좋아하는 웹 사이트에 IP 주소가 있지만 분명히 기억하기는 쉽지 않습니다. 그러나 도메인 이름은 사람들이 쉽게 인식하고 기억할 수 있습니다.즉, DNS는 도메인 이름을 IP 주소와 동기화하여 사람이 기억에 남는 도메인 이름을 사용하고 컴퓨터는 인터넷의 IP주소를 조회 할 수 있습니다

more [Link](https://www.verisign.com/en_US/website-presence/online/how-dns-works/index.xhtml)

**What is Domain Name**

넓은 의미로는 네트워크상에서 컴퓨터를 식별하는 호스트명을 가리키며, 좁은 의미에서는 도메인 레지스트리에게서 등록된 이름을 의미한다.
숫자로 된 IP 주소에 비해 외우기 쉬우며, 여러 개의 IP 주소가 한 도메인에 대응되거나(서브 도메인) 여러 도메인이 하나의 IP 주소로 대응되는(가상 호스트) 것도 가능하다.

## Browsers and how they work?

![Web Browsers icon](https://icon-library.com/images/web-browser-icon-png/web-browser-icon-png-0.jpg)

웹 브라우저를 사용하면 인터넷 어디로 든 이동할 수 있습니다. 정보는 웹에서 텍스트, 이미지 및 비디오가 전송되는 방식을 정의하는 HTTP을 사용하여 전송됩니다. 이 정보는 공유되고 일관된 형식으로 표시되어야 전 세계 모든 브라우저를 사용하는 사람들이 정보를 볼 수 있습니다.

안타깝게도 모든 브라우저 제작자가 동일한 방식으로 형식을 해석하는 것은 아닙니다. 사용자에게 이것은 웹 사이트가 다르게 보이고 작동 할 수 있음을 의미합니다. 모든 사용자가 선택한 브라우저에 관계없이 인터넷을 즐길 수 있도록 브라우저 간의 일관성을 만드는 것을 웹 표준 이라고 합니다 .

웹 브라우저는 인터넷에 연결된 서버에서 데이터를 가져올 때 렌더링 엔진이라는 소프트웨어를 사용하여 해당 데이터를 텍스트와 이미지로 변환합니다.
**렌더링 엔진**

- Internet Explorer : Trident
- Firefox 및 기타 Mozilla 브라우저 : Gecko
- Chrome 및 Opera 15+ : Blink
- Chrome (iPhone) 및 Safari : Webkit

사용자는 하이퍼 링크를 통해 웹의 다른 페이지나 사이트로 이동할 수 있습니다. 모든 웹 페이지, 이미지 및 비디오에는 웹 주소라고도하는 고유 한 URL(Uniform Resource Locator)이 있습니다.

more [Link](https://www.mozilla.org/en-US/firefox/browsers/what-is-a-browser/)
