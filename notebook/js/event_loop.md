# Event Loop

## JS Engine

![JS Engine](https://miro.medium.com/max/2048/1*4lHHyfEhVB0LnQ3HlhSs8g.png)

자바스크립트 엔진은 Memory Heap 과 Call Stack 으로 구성되어 있습니다.
자바스크립트는 단일 스레드 (sigle thread) 프로그래밍 언어인데, 이 의미는 Call Stack이 하나 라는 이야기입니다.

`따라서 멀티동작이 되지 않고, 하나씩 처리한다는 의미입니다.`

`Memory Heap` : 메모리 할당이 일어나는 곳.
(ex, 우리가 프로그램에 선언한 변수, 함수 등이 담겨져 있음)

`Call Stack` : 코드가 실행될 때 쌓이는 곳. **stack** 형태로 쌓임.

`Stack(스택)` : 자료구조 중 하나, 선입후출(LIFO, Last In First Out)의 룰을 따릅니다.

![자바스크립트 비동기 처리 과정](http://sculove.github.io/blog/2018/01/18/javascriptflow/browser-structure.png)

## Web API

Web API 는 브라우저에서 제공하는 API 로, DOM, Ajax, Timeout 등이 있습니다.
Call Stack에서 실행된 비동기 함수는 Web API를 호출하고,

`Web API는 콜백함수를 Callback Queue에 밀어 넣습니다.`

### Callback Queue

**비동기적으로 실행된 콜백함수가 보관** 되는 영역입니다.

- Queue(큐) : 자료 구조 중 하나, 선입선출(FIFO, Frist In Frist OUT)의 룰을 따릅니다.

## Microtask Queue

promis.then 등 등

**Event Loop는 우선적으로 Microtask Queue를 확인합니다.**

만약 **Microtask Queue에 콜백이 있고 Call Stack이 비어져 있는 상태**라면 Call Stack에 담습니다.

**Microtask Queue에 더이상 처리해야할 콜백이 없다면**, Task Queue에 확인 후 처리합니다.

## Animation Frames

![Render Queue](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTIWFl3K-JUdKn6B1ldMNX_nJvU4X81-O_tjg&usqp=CAU)

1sec 당 60 frame을 지향하며 이벤트루프는 그보다 빠르기 때문에 약간의 웹 브라우저마다 포커싱 타임이 다릅니다.

requestAnimationFrame API가 실행되면 콜백이 Animation Frames으로 담긴다.

## Result

```js
console.log("script start")

setTimeout(function () {
  console.log("setTimeout")
}, 0)

Promise.resolve()
  .then(function () {
    console.log("promise1")
  })
  .then(function () {
    console.log("promise2")
  })

requestAnimationFrame(function () {
  console.log("RAF")
})
console.log("script end")
```

```
script start
script end
promise1
promise2
requestAnimationFrame
setTimeout
```

### event loop 작동순서

![event loop gif](https://miro.medium.com/max/700/0*TFNP5xrCj3wT8eHO.gif)

![event loop gif](https://miro.medium.com/max/700/0*iHLzfmlOAroed4Bz.gif)

![event loop gif](https://miro.medium.com/max/700/0*47VbpeN4KkZOFRTS.gif)

![event loop gif](https://miro.medium.com/max/700/0*s4eSFL2uQeI_yVYo.gif)

![event loop gif](https://miro.medium.com/max/700/0*6nwYdxp13B3rNcay.gif)

![event loop gif](https://miro.medium.com/max/700/0*Z8_B7kp-5_cEbmue.gif)

이미지 출처 [Link site](https://medium.com/@lydiahallie/javascript-visualized-promises-async-await-a3f1aad8a943)

**More**

[Link site](http://sculove.github.io/blog/2018/01/18/javascriptflow/)

[Link MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/EventLoop)

[Link youtube](https://www.youtube.com/watch?v=8aGhZQkoFbQ&t=406s)
