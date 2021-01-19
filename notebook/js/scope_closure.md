# Scope and Closure

## Scope

예전에는 함수 단위로만 스코프가 생성 되었다면 ES6 이후로
hoisting으로 인한 오류 방지를 위한 Scope로 const와 let을 사용함으로 예방 할 수 있습니다.

`전역변수`: 지역스코프 `{}` 안에 속한 변수가 아니며 전역적으로 접근이 가능합니다.

`지역변수`: 지역스코프 `{}` 안에 속한 변수이며 전역적으로 접근이 불가능합니다.

### Scope chain

참조하는 과정에서 지역스코프 안에 참조값이 없다면 전역으로 참조값을 찾는 과정을 뜻합니다.

- 지역 범위 (Local Scope, Own scope)
- 외부 함수 범위 (Outer Functions Scope)
- 전역 범위 (Global Scope)

## Closure

외부 함수의 실행이 종료되어 소멸된 이후에도 내부 함수가 외부 함수에 접근 할수 있습니다.

**코드로 쉽게 이해하기**

```js
const msg = "hello" // 전역변수
function printMsg() {
  let lang = "JS" // 지역변수
  console.log(`${msg}, ${lang}`) // hello, JS
  function inner() {
    console.log(`${msg}, ${lang}`) // hello, JS >> Closure
  }
  inner()
}
printMsg()
console.log(`${msg}, ${lang}`) //  ReferenceError
```

## Notice

특정 작업에 클로저가 필요하지 않는데 다른 함수 내에서 함수를 불필요하게 작성하는 것은 현명하지 않습니다.
이것은 처리 속도와 메모리 소비 측면에서 스크립트 성능에 부정적인 영향을 미칩니다.

**More**

[Link MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Closures)

[Link youtube](https://www.youtube.com/watch?v=tpl2oXQkGZs&t=237s)
