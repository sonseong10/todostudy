# Browser Rendering

브라우저가 화면에 나타나는 요소를 렌더링 할 때, 웹킷(Webkit)이나 게코(Gecko) 등과 같은 렌더링 엔진 을 사용합니다.

### 렌더링 엔진

|       이름       |    엔진     |
| :--------------: | :---------: |
|     브레이브     |   블링크    |
|      비발디      |   블링크    |
|      사파리      |   웹키트    |
|       엣지       |  크로미움   |
|      오페라      |   블링크    |
|   오페라클래식   |   블링크    |
|       웨일       |   블링크    |
| 인터넷익스플로러 | 트라이던트  |
|       크롬       |   블링크    |
|    파이어폭스    | 게코,웹키트 |

렌더링 엔진이 HTML, CSS, Javascript로 렌더링할 때 **CRP(Critical Rendering Path)** 라는 프로세스를 사용하며 다음 단계들로 이루어집니다.

![CRP](https://post-phinf.pstatic.net/MjAxNzA3MDJfMTEy/MDAxNDk4OTI1MjU4OTY3.OR6bSfoKWEl_T4gQ1RDjKZ7dimgljLViK9QRPe9uQRQg.3FOoFdCJQGOBFEErH1EXUtHKnUfTg0-kkmnToN3-LHsg.PNG/image_3480670191498924844279.png?type=w1200)

1. HTML 파싱
2. DOM(Document Object Model) 트리 구축
3. CSS 파싱, CSSOM(CSS Object Model) 트리 구축
4. Javascript 실행
   > Notice) HTML 중간에 script가 있다면 HTML 파싱이 중단된다.
5. DOM과 CSSOM을 조합하여 렌더트리(Render Tree) 구축
   > Notice) display: none 속성과 같이 화면에서 보이지도 않고 공간을 차지하지 않는 것은 렌더트리로 구축되지 않는다.
6. 뷰포트 기반으로 렌더트리의 각 노드가 가지는 정확한 위치와 크기 계산 (Layout/Reflow 단계)
7. 계산한 위치/크기를 기반으로 화면에 그림 (Paint 단계)

**More**

[Link Site](https://boxfoxs.tistory.com/408)
