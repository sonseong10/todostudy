# Local storage vs Session storage vs Cookie

모두 클라이언트 상에서 `key/value 쌍을 저장`할 수 있는 메커니즘으로 `value는 반드시 문자열` 이어야 한다. 또한 모두 [동일 출처 정책(SOP)](<https://ko.wikihow.com/%ED%91%9C%EC%A4%80-%EC%9A%B4%EC%98%81-%EC%A0%88%EC%B0%A8(SOP,-Standard-Operation-Procedure)-%EC%9E%91%EC%84%B1%EB%B2%95>) 을 따르기 때문에 다른 도메인에서 접근할 수 없습니다.

- local storage

  1. 5MB/10MB
  2. 클라이언트 사이드에서만 읽기가 가능하며, 자바스크립트나 브라우저를 통해 **명시적**으로 삭제 가능합니다.
  3. 유저가 브라우저 윈도우를 닫더라도 데이터는 삭제되지 않습니다.
  4. XSS에 취약합니다.

* session storage

  1. 5MB
  2. local storage와 비슷하나 데이터는 **오직 브라우저의 윈도우나 탭이 열려있을 때만** 이용 가능하다.
  3. 윈도우나 탭이 닫히면 스토리지의 데이터도 삭제된다.
  4. XSS에 취약합니다.

- cookie
  1. 4KB
  2. 모든 HTTP 요청마다 쿠키의 데이터가 함께 서버로 보내지므로 클라이언트뿐만아니라 **서버에서도 읽기가 가능**합니다.
  3. 만약 SSL을 사용하고 있지 않다면, 쿠키는 퍼블릭 와이파이에 의해 가로채가는 것이 가능합니다.
  4. HttpOnly cookie flag를 사용하면 자바스크립트로 접근이 불가능하게 만들어서 XSS에 방어할 수 있습니다.
  5. CSRF에 취약합니다.

### 정리

|     비교      |      cookie      |     local storage     |     session storage     |
| :-----------: | :--------------: | :-------------------: | :---------------------: |
|    생성자     | 클라이언트/서버  |      클라이언트       |       클라이언트        |
|   지속시간    | 설정 여부에 따름 | 명시적으로 지울때까지 | 탭 / 윈도우 닫을 때까지 |
|     용량      |       5KB        |      5MB / 10MB       |           5MB           |
| 서버와의 통신 |        O         |           X           |            X            |
|    취약점     |    CSRF 공격     |       XSS 공격        |        XSS 공격         |

### 참고

[stackoverflow](https://stackoverflow.com/questions/19867599/what-is-the-difference-between-localstorage-sessionstorage-session-and-cookies)
