# Event Flow

이벤트 핸들링에서 알아둬야 할 캡쳐링, 버블링의 대하여 설명합니다.

### Target, CurrentTarget 차이

target: 이벤트의 발생위치
currentTarget: 이벤트의 주인

## Capturing, Bubbling

![event_flow](https://dmitripavlutin.com/static/9a8fc772a94452ca819295094c99b1a9/ff59c/javascript-event-propagation-5.png)

### Bubbling (=Bubble phase, = propagate down)

한 요소에 이벤트가 발생하면, 이 요소에 할당된 핸들러가 동작하고, 이어서 부모 요소의 핸들러가 동작합니다. 가장 최상단의 조상 요소를 만날 때까지 이 과정이 반복되면서 요소 각각에 할당된 핸들러가 동작합니다.

`거의 모든 이벤트는 버블링 됩니다.`

> 키워드는 ‘거의’ 입니다.
> focus 이벤트와 같이 버블링 되지 않는 이벤트도 있습니다. 버블링 되지 않는 이벤트의 종류에 대해선 조금 후에 알아보겠습니다. 몇몇 이벤트를 제외하곤 대부분의 이벤트는 버블링 됩니다.

### Bubbling 중단하기

event.stopPropagation()을 사용하여 버블링을 중단시킬수 있습니다.

- `event.stopImmediatePropagation()`
  event.stopPropagation()은 위쪽으로 일어나는 버블링은 막아주지만, 다른 핸들러들이 동작하는 건 막지 못합니다.요소에 할당된 다른 핸들러의 동작도 막으려면 event.stopImmediatePropagation()을 사용해야 합니다. 이 메서드를 사용하면 요소에 할당된 특정 이벤트를 처리하는 핸들러 전부 동작하지 않습니다.

`Notice`

> 꼭 필요한 경우를 제외하곤 버블링을 막으면 안됩니다.
> 이벤트 버블링을 막아야 하는 경우는 거의 없습니다. 버블링을 막아야 해결되는 문제라면 커스텀 이벤트 등을 사용해 문제를 해결할 수 있습니다.

### Capturing (= Capture phase, = propagate up)

한 요소에 이벤트가 발생하면, 버블링과 반대로 이벤트가 최상위 조상에서 시작해 아래로 전파됩니다.
특수 케이스를 제외 하고는 잘 사용하지 않습니다.

## Bubbling, Capturing 사용법

addEventListener에서 useCapture값 조절합니다.

useCapture: true => Bubbling
useCapture: false => Capturing

[addEventListener MDN](https://developer.mozilla.org/ko/docs/Web/API/EventTarget/addEventListener)

```js
temp.addEventListener("click"(event), ()=>{
  //something
}(callback),
[true]//Bubbling(default)
)
```

**More**

[Link Youtube](https://www.youtube.com/watch?v=7gKtNC3b_S8&t=91s)

[Link Site](https://ko.javascript.info/bubbling-and-capturing)
