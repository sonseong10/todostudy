# Prototype

보이지 않는 속성인 `[[Prototype]]`은 자신의 프로토타입 객체를 참조 합니다. JavaScript에서 함수는 객체이므로 프로토타입을 가집니다.

`__proto__` 속성으로 참조할 수 있으나 모든 브라우저에서 동작하는 것은 아니기 때문에 조심 해야 합니다.

```javascript
// new = 생성자 함수 = 객체
// Sub.prototype = 객체

function Ultra() {}
Ultra.prototype.ultraProp = "temp"

function Super() {}
Super.prototype = new Ultra()

function Sub() {}
Sub.prototype = new Super()

const foo = new Sub() // -> const foo = { }
console.log(foo.ultraProp) // temp
```

![prototype](https://evan-moon.github.io/static/c4c3f4bd82adfc1f6422180eedbd4fb0/ee604/thumbnail.png)

## Prototype Chain

프로토타입 객체를 `연속적으로 연결되어 프로퍼티를 찾는 방식`을 **프로토타입 체인** 이라고 합니다.

### 프로퍼티를 참조할 때

- 찾고자 하는 프로퍼티가 객체에 존재하면 사용 합니다.
- 없으면 `[[Prototype]]` 링크를 타고 끝까지 올라가면서 해당 프로퍼티를 찾습니다.
  > 찾으면 그 값을 사용하고 없으면 undefined 를 반환 합니다.

###프로퍼티에 값을 할당할 때

- 찾고자 하는 프로퍼티가 객체에 존재하면 값을 바꿉니다.
- 프로퍼티가 없고 `[[Prototype]]` 링크를 타고 올라가서 해당 프로퍼티를 찾았을 경우
  > 해당 프로퍼티가 변경가능한 값, 새로운 직속 프로퍼티를 할당해서 상위 프로퍼티가 가려지는 현상이 발생 합니다.
  > 그 프로퍼티가 변경불가능한 값, 비엄격 모드에선 무시되고 엄격 모드에선 에러가 발생 합니다.

**More**

[Link site](https://opentutorials.org/module/532/6573)
[Link site](https://www.toptal.com/javascript/javascript-prototypes-scopes-and-performance-what-you-need-to-know)
