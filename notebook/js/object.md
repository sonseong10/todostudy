# Object

- one of the JavaScript's data type

  (JavaScript의 데이터 유형 중 하나)

- a collection of related data and/or functionality.

  (관련 데이터 또는 기능의 모음)

- Nearly all object in JavaScript are instances of object

  (JS의 오브젝트는 대부분 객체의 인스턴스)

- object= { key : value };
- instance of a class

  (클래스의 한 인스턴스)

- created many times

  (비번한 사용)

- data in

  (데이터를 보유함)

**How to use**

```js
// 1. Literals and properties
const obj1 = {} // 'object literal' syntax
const obj = new Object() // 'object constructor' syntex

//not use object
const name = "yeol"
const age = 24
print(name, age)
function print(name, age) {
  console.log(name)
  console.log(age)
}

// using object
const user = { name: "Yeol", age: 24 }
print(user)
function print(user) {
  console.log(user.name)
  console.log(user.age)
}

// JS === Dynamically typed language
// create object
user.job = "none"
user["job"] = "none"
console.log(user.job)

// delete object
delete user.job
delete user["job"]
```

```js
// 2. Computed properties
// key should be always string
console.log(user.name)
console.log(user["name"])

// object access key
function printValue(obj, key) {
  console.log(obj[key])
}
printValue(user, "age")
printValue(user, "name")
```

```js
//3. property value shorthand
const user1 = { name: "foo", age: 12 }
const user2 = { name: "pin", age: 20 }

//before using
function makeUser(name, age) {
  return {
    name: name,
    age: age,
  }
}

//better then use
const user3 = makeUser("Tom", 30)
console.log(user3)
function makeUser(name, age) {
  return {
    name,
    age,
  }
}
const user3 = makeUser("Tom", 30)
console.log(user3)

// Constructor function
// now usefully
function User(name, age) {
  // this ={};
  this.name = name
  this.age = age
  //return this;
}
const user3 = new User("Tom", 30)
console.log(user3)
```

```js
// 4. in operator: property existence check ('key' in object)
console.log("name" in user3) // true
```

```js
// 5. for..in VS for..of
// for (key in obj)
for (key in user3) {
  console.log(key)
}

// for (value of iinterableW)
const arr = [1, 2, 3, 4, 5]
for (value of arr) {
  console.log(value)
}
```

```js
//6. cloning
// object.assign(dest, [obj1, obj2...])
const people1 = { name: "tami", age: 34 }
const people2 = people1
people2.name = "Tami"
console.log(people1.name) // Tami

//way1
const people3 = {}
for (key in people1) {
  people3[key] = people1[key]
}
console.log(people3.name) // Tami

//way2
const people4 = {}
Object.assign(people4, people1)
console.log(people4.name)

//best way
const people5 = Object.assign({}, people1)
console.log(people5.name)
```

**More**

[Link MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Object)
