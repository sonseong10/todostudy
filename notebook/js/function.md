# Function

- fundamental building block in the progrm

  (프로그램의 기본 구성 요소)

- subprogram can be used multiple time

  (서브 프로그램에서 다중사용 가능)

- performs a task or calculates a value

  (작업을 수행하거나 값을 계산)

- function is object in JS

**Function are treated like any other variable**

- can be assiqned as a value to variable

  (변수에 할당 가능)

- can be passed as an argument to other functions.

  (다른 함수의 인자로 사용가능)

- can be returned by another function

  (다른 함수에 리턴값으로 사용가능)

using)

```js
function [name]([parameter]) {[return]}
```

one function === one thing

naming: doSomething, command, varb

e.g) addandsub() → addNumber(), subNumber()

Function expression

a function declaration can be called earlier than it is defiend. (hosted)

a function expression is created the execution reaches it.

```js
// anonymous function
const test = function () {
  console.log("testText")
}
test()
const test1 = test
test1()

// Named function
const test = function printText() {
  console.log("testText")
}
```

## Parameter

premitive parameter: passed by value

object parameter: passed by reference

```js
function changeName(obj) {
  obj.name = "tester"
}
const yeol = { name: "yeol" }
console.log(yeol.name)
changeName(yeol)
console.log(yeol.name)
```

## Default parameter (+ES6)

```js
//before
function Message(message, to) {
  if (to === undefined) {
    to = "me"
  }
  console.log(`${message}, to ${to}`)
}
Message("Hi!")
//after
function Message(message, to = "me") {
  console.log(`${message}, to ${to}`)
}
Message("Hi!")
```

## Rest parameter (+ES6)

using) ...[parameter]

```js
function printAll(...arg) {
	for(let i = 0; i < arg.length; i++){
		console.log(arg[i]);
	}
	for (const args of arg) {
		console.log(args);
	}

	arg.forEach(args) => console.log(args);
}

printAll('1','2','3');
```

## Local scope

※ 안에서 밖이 보이게 밖에선 안이 보이지 않게

```js
let globlaMsg = "global"
function printMsg() {
  let msg = "inside"
  console.log(msg)
  console.log(globlaMsg)
  function printAnothor() {
    console.log(msg)
    let childMsg = "hello"
  }
  console.log(childMsg) // ReferenceError error
}
printMsg()
```

## Return

```jsx
function sum(a, b) {
  return a + b
}
let result = sum(2, 4)
console.log(`sum: ${result}`)
```

no using return = return undefined;

**Early return, Early exit**

```js
// bad
function upgradeUser(user) {
  if (user.point > 10) {
    console.log("go to next level!")
  }
}

// good
function upgradeUser(user) {
  if (user.point <= 10) {
    return
  } else {
    console.log("go to next level!")
  }
}

let user = { point: 8 }
upgradeUser(user)
```

## Callback function

```js
function quiz(answer) {
  if (answer === "answer") {
    printT()
  } else {
    printF()
  }
}
// anonymous function
let printT = function () {
  console.log("True!")
}

// named function
// better debugging in debugger's stack traces
// recursions
let printF = function print() {
  console.log("False!")
}

quiz("answer")
quiz("123")
```

## ArrowFunction

always anonymous function

```js
//Function
const add = function (num1, num2) {
  return num1 + num2
}
//ArrowFunction
const add = (num1, num2) => num1 + num2
```

## IIFE

immediately invoked Function Expression

```js
function hello() {
  console.log("IIFE")
}
hello()

//IIFE
;(function hello() {
  console.log("IIFE")
})()
```
