# this 바인딩

JavaScript에서 함수의 this 키워드는 다른 언어와 조금 다르게 동작합니다. 또한 `엄격 모드`와 `비엄격 모드`에서도 일부 차이가 있습니다.

EC(Execution Context)가 생성될 때마다 this의 바인딩이 일어나며 우선순위 순으로 나열합니다.

## 엄격 모드

- `new` 를 사용한 경우 해당 객체로 바인딩 됩니다.
  (반환 값이 객체가 아니면 this 객체가 반환 됨).

```javascript
function C() {
  this.a = 37
}

var o = new C()
console.log(o.a) // 37

function C2() {
  this.a = 37
  return { a: 38 }
}

o = new C2()
console.log(o.a) // 38
```

- `call`, `apply`, `bind` 와 같은 명시적 바인딩을 사용했을 때 인자로 전달된 객체에 바인딩 됩니다.

```javascript
function f() {
  return this.a
}

var g = f.bind({ a: "azerty" })
console.log(g()) // azerty

var h = g.bind({ a: "yoo" }) // bind는 한 번만 동작
console.log(h()) // azerty

var o = { a: 37, f: f, g: g, h: h }
console.log(o.a, o.f(), o.g(), o.h()) // 37, 37, azerty, azerty
```

- 객체의 메서드로서 호출할 경우 해당 객체에 바인딩 됩니다.

```javascript
var o = {
  prop: 37,
  f: function () {
    return this.prop
  },
}

console.log(o.f()) // 37
```

## 비엄격 모드

- 단순 호출

```javascript
function f1() {
  return this
}

// 웹 브라우저
f1() === window // true

// Node.js
f1() === global // true
```

**More**
[Link MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Operators/this)
