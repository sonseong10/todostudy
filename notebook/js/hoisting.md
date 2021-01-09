# Hoisting

호이스팅이란 "끌어올린다" 라는 뜻으로 변수 및 함수 선언문이 스코프 내의 최상단으로 끌어올려지는 현상 을 말합니다.

여기서 주의할 점은 "선언문" 이라는 것이며 "대입문"은 끌어올려지지 않습니다.

```js
console.log(temp) // undefined
var temp = "hoisting"
console.log(temp) // hoisting
```

```javascript
func()
function func() {
  console.log("hoisting")
}
// hoisting
```

## Notice

함수 표현식(Function Expression)은 호이스팅 되지 않습니다.

```javascript
hois()
var hois = function () {
  console.log("func")
}
// TypeError: hois is not a function
```

함수와 변수 선언문 중에는 함수 선언문이 먼저입니다.

```javascript
func()
var func = function () {
  console.log("var func")
}
function func() {
  console.log("func")
}
// func
```

`const`, `let`은 호이스팅 되지 않습니다.

```javascript
console.log(conHoi)
const conHoi = "temp"
//ReferenceError: Cannot access 'conHoi' before initialization
console.log(letHoi)
const letHoi = "temp"
//ReferenceError: Cannot access 'letHoi' before initialization
```

**More**

[Link site](https://velog.io/@surim014/JavaScript%EC%97%90%EC%84%9C%EC%9D%98-Hoisting%EC%9D%B4%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80)
