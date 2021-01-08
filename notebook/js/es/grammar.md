![es icon](https://gnutec.net/wp-content/uploads/2019/08/es-ecmascript-logo.png)

# ES(ECMAScript)

`자바스크립트를 표준화하기 위해 만들어졌습니다.`

## ES Grammar

모든 ES 내용이 아닌 `ES6(2015) ~ ES11(2020)`까지 추가된 내용 중 문법만 정리하였습니다.

## Shorthead property names

```js
const student = {
  name: "minsu",
  age: "19",
}

const name = "minsu"
let age = "19"

const oldWay = {
  name: name,
  age: age,
}

const newWay = {
  name,
  age,
}

console.log(student, oldWay, newWay)
```

result

```
{name: "minsu", age: "19"}
{name: "minsu", age: "19"}
{name: "minsu", age: "19"}
```

## Destructuring Assignment

### Obj

```js
const fruit = {
  name: "apple",
  shape: "🍎",
}

// old
const name = fruit.name
const shape = fruit.shape
console.log(name, shape)

// new
const { name, shape } = fruit
console.log(name, shape)
```

### Array

```js
const fruits = ["apple", "banana"]

// old
const one = fruits[0]
const two = fruits[1]
console.log(one, two)

// new
const [one, two] = fruits
console.log(one, two)
```

## Spread Syntax

```js
const temp1 = { color: "red" }
const temp2 = { color: "blue" }
const array = [temp1, temp2]

// way1
const arrayClone = array.slice()
console.log(arrayClone)

// way2
const arrayClone = [...array]
console.log(arrayClone)

const objClone = { ...array }
console.log(objClone)
```

### Add

```js
// 값이 변경 된다면 모든 위치에서 변경 되므로 주의 해야합니다.
const arrayClone = [...array, { colro: "yellow" }]
console.log(arrayClone)
temp1.color = "green"
console.log(arrayClone)
```

result

```
{color: "green", color: "blue", color: "yellow"}
{color: "green", color: "blue", color: "yellow"}
```

### Combination

```js
// 만약 키의 값이 겹친다면 마지막 값으로 덮어씁니다.
const sameKey = { ...temp1, ...temp2 }
console.log(sameKey)
```

result

```
{color: "blue"}
```

## Default parameters

```js
function noDefult(num) {
  console.log(num)
}

noDefult(3) // 3
noDefult() // undifind
```

```js
// old
function Defult(num) {
  if (num == null) {
    num = "Defult num"
  }
  console.log(num)
}
Defult(3) // 3
Defult() // Defult num

// new
function Defult(num = "Defult num") {
  console.log(num)
}
Defult(3) // 3
Defult() // Defult num
```

## Ternary Operator

```js
// old
if (0 < 1) {
  console.log("true")
} else {
  console.log("false")
} // true

// new
0 < 1 ? console.log("true") : console.log("false")
// true

console.log(0 > 1 ? "true" : "false")
// fales
```

## Template Literals

```js
const user = { name: "foo", age: 13 }

// old
console.log("--------\n" + "name: " + user.name + ", age: " + user.age)
//  --------
//  name: foo, age: 13

// new
console.log(`--------
name: ${user.name}, age: ${user.age}`)
//  --------
//  name: foo, age: 13
```

## Optional Chaining

```js
const parent1 = {
  name: "foo",
  child: {
    age: 13,
  },
}
const parent2 = {
  name: "hoo",
}

// old
function showChild(parent) {
  console.log(parent.child.age)
}

showChild(parent1) // 13
showChild(parent2) // TypeError

// fix error

// way1
function showChild(parent) {
  console.log(parent.child ? parent.child.age : "no child")
}

// way2
function showChild(parent) {
  console.log(parent.child && parent.child.age)
}

// way3
function showChild(parent) {
  console.log(parent.child?.age)
}
```

## Nullish coalescing Operator

```js
// before
const count = 0 //
const userCount = count || "Error"
console.log(userCount) // Error

// after
const count = 0
const userCount = count ?? "Error"
console.log(userCount) // 0
```

**More**
[Link youtube](https://www.youtube.com/watch?v=36HrZHzPeuY)
