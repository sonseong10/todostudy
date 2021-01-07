![web request response](https://miro.medium.com/max/700/1*8-fT6K1o6nHiBRxKppcqOg.png)

## 주요단어

AJAX ⇒ Asynchronous JavaScript And XML

XHR ⇒ XMLHttpRequest → object

fetch() API ⇒ New technology → can't use IE

## ModernUes(JSON)

JavaScript Object Notation → object

- simplest data interchange format
- lightweight text-based structure
- easy to read
- key-value pairs
- used for serialization and transmission of data
  between the network the network connection
- independent programming language and platform

- 가장 간단한 데이터 교환 형식
- 가벼운 텍스트 기반 구조
- 읽기 쉬움
- 키 : 값
- 네트워크 연결과 네트워크 간의 데이터 직렬화 및 전송에 사용
- 독립적인 프로그래밍 언어 및 플랫폼

![serialization and deserialization](https://miro.medium.com/max/781/0*MmmFxL-hkPh_t6Xg.jpg)

## Object to Json

```jsx
// can not be used type: function, undefined, symbol
const people = {
  name: "Tom",
  age: 25,
  size: null,
  lang: ["en", "ko"],
  birthDate: new Date(),
  sayHello: () => {
    console.log(`${people.name} Hello!`)
  },
}
// way
let json = JSON.stringify(people)
console.log(json)
//{"name":"Tom","age":25,"size":null,"lang":["en","ko"],
//"birthDate":"2020-08-24T01:21:09.954Z"}
typeof json // String

// next level
let json = JSON.stringify(people, (key, value) => {
  console.log(`key: ${key}, value: ${value}`)
  return value
})
console.log(json)
typeof json // String

// next level
let json2 = JSON.stringify(people, (key, value) => {
  console.log(`key: ${key}, value: ${value}`)
  return key === "name" ? "Jessi" : value
})
console.log(json)
typeof json // String

//stringify() Precautions: Double reference
let room = {
  number: 23,
}

let meetup = {
  title: "Conference",
  participants: ["john", "ann"],
}

meetup.place = room // meetup은 room을 참조합니다.
room.occupiedBy = meetup // room은 meetup을 참조합니다.

JSON.stringify(meetup) // Error: Converting circular structure to JSON
```

## Json to Object

```jsx
//setting
const people = {
  name: "Tom",
  age: 25,
  size: null,
  lang: ["en", "ko"],
  birthDate: new Date(),
  sayHello: () => {
    console.log(`${people.name} Hello!`)
  },
}
const json = JSON.stringify(people)

//way
let obj = JSON.parse(json)
console.log(obj)
typeof obj // Object

//next level
let obj = JSON.parse(json, (key, value) => {
  console.log(`key: ${key}, value: ${value}`)
  return value
})

//next level
let obj = JSON.parse(json, (key, value) => {
  return key === "birthDate" ? new Date(value) : value
})
```
