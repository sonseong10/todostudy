# CSS vs JS Animation

인터렉티브한 웹을 생산하기 위해 Animation은 필수적인 요소로 자리 잡고 있습니다.
사용자 눈에 가장 부드러운 60fps가 유지하기 위해 css Animation 또는 JS(JavaScript) Animation
을 적재적소하게 사용해야 합니다.

## css Animation

CSS의 `가상선택자(:hover, ::after ...), transition, animation` 등등 속성을 사용할 수 있습니다.

### 장점

- 반응형으로 애니메이션을 구현하기에 유용한데, @media 쿼리로 애니메이션을 적용하면 됩니다.
- 외부 라이브러리를 필요로 하지 않습니다.
- CSS 자체가 선언형(declarative)이기 때문에 어떤 요소가 애니메이션을 가져야 한다는 직관적인 표현이 가능합니다.
- 메인 쓰레드가 아닌 별도의 컴포지터 쓰레드(Compositor Thread)에서 그려지기 때문에 효율적입니다.

### 단점

- 세밀한 구성이 불가능 합니다.
- 모바일에서 성능저하를 발생시킬 수 있습니다.

## JS(JavaScript) Animation

세밀한 동작을 필요로 하거나 [velocity.js](http://velocityjs.org/), [threejs](https://threejs.org/)등 이미 제작된 기능을 사용 하여 편리하게 적용 할 수 있습니다.

### 장점

- 요소의 스타일이 변하는 순간마다 제어할 수 있기 때문에 애니메이션의 세밀한 구성이 가능해집니다.
- GPU를 통한 하드웨어 가속을 제어할 수 있습니다. 이는 CSS의 특정 속성으로 인한 가속을 막아주는데, 하드웨어 가속이 모바일에서 성능저하를 발생시킬 수 있기 때문에 이런 면에선 좋습니다.
- 브라우저 호환성 측면에서 transition/animation 속성보다 뛰어납니다.

### 단점

- 계속해서 요소의 위치를 재계산하기 때문에 간단한 작업에서는 비효율적입니다.
- 사용자 눈에 가장 부드러운 60fps가 유지되지 어렵습니다.

## 구현 상황에 맞는 사용법

**CSS Animation**

- UI 요소 상태 전환 등, 간단한 원샷의 애니메이션을 적용하고 싶을 때
- UI 요소가 작거나, 그 요소만의 자체적인 상태를 갖고 있을 때

**Javascript Animation**

- 바운스, 중지, 일시정지, 되감기 등의 고급 효과를 원할 때
- 애니메이션에 대해 세밀한 작업을 해야하는 경우

- 전체 장면에 대한 애니메이션을 하고 싶다면 (RAF)requestAnimationFrame을 사용합니다.
  -> javascript 의 고급의 접근방식.

**More**

[Link Site](https://developers.google.com/web/fundamentals/design-and-ux/animations/css-vs-javascript?hl=ko)

[Link Site](https://velog.io/@hyun_sang/CSS-%EC%95%A0%EB%8B%88%EB%A9%94%EC%9D%B4%EC%85%98-VS-JSJavaScript-%EC%95%A0%EB%8B%88%EB%A9%94%EC%9D%B4%EC%85%98)

[Link Site](https://www.codeinwp.com/blog/best-javascript-animation-libraries/)
