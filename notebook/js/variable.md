# Variable

### VAR(사용을 자제)

```js
console.log(num) //undefined
num = 1
var num
console.log(num) //1
```

Reason)

var hoisting

(선언된 위치와 상관없이 맨 위로 위치시킴)

var is no block scope

### let(+ES6)

mutable(변경가능)

```js
let name = "Hello"
console.log(name) //Hello
name = "World"
console.log(name) //World
```

> block scope/grobal scope

```js
let grobal = "World"
{
  let block = "Hello"
  console.log(block) //Hello
  console.log(grobal) //World
}
console.log(block) //
console.log(grobal) //World
```

### const(+ES6)

immutable(변경불가)

- security (보안+)
- thread safety(동시다발적 변경 방지)
- reduce human mistakes(실수방지)

```js
const grobal = "World"
console.log(grobal) //World
{
  const block = "Hello"
  console.log(grobal) //World
  grobal = "!"
  console.log(block) //Hello
  console.log(grobal) //syntax error
}
```
