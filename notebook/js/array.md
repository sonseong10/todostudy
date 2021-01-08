# Array

![array](https://user-images.githubusercontent.com/68719427/103960143-d8d85d00-5194-11eb-8cbd-a43358a54d07.png)

## Index position

```js
const fruits = ["🍊", "🍅"]
console.log(fruits)
console.log(fruits.length)
console.log(fruits[0])
console.log(fruits[fruits.length - 1]) //array last index

//Looping over an array
//print all frutis

//old way
for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i])
}

//next way
for (let fruit of fruits) {
  console.log(fruit)
}

//now way
fruits.forEach((fruit) => console.log(fruit))
```

## Array addtion, deletion, copy

```js
// pusp: add an item to the end
fruits.push("🍏", "🍑")
console.log(fruits)
// pop: remove an item from the end
fruits.pop()
console.log(fruits)

// unshift: add an item to the benigging
fruits.unshift("🍏", "🍑")
console.log(fruits)
// shift: remove an item from the benigging
fruits.shift()
console.log(fruits)

// !important shift, unshift are slower then pop, push

// splice: remove an item by index position
fruits.splice(1) // remove index behind all
console.log(fruits)
fruits.splice(1, 1) // remove index count all
console.log(fruits)
fruits.splice(1, 1, "🍉") // remove index count all and add index
fruits.splice(1, 0, "🍇") // no remove index and add index
console.log(fruits)

// concat: combine two arrays
const fruits2 = ["🍒", "🍍"]
const newFruits = fruits.concat(fruits2)
console.log(newFruits)
```

## Searching Array

```js
//indexOf: find the index
console.log(newFruits.indexOf("🍒")) // index number
console.log(newFruits.indexOf("cat")) // -1

//includes: boolean the index
console.log(newFruits.includes("🍒")) // true

//lastIndexOf: find the index
newFruits.push("🍒")
console.log(newFruits.indexOf("🍒")) // firest index number
console.log(newFruits.lastIndexOf("🍒")) // last index number
```

## Array to String & String to Array

```js
const animalArray = ["dog", "cat", "panda"]
// join: make a String out of an array
const joinArray = animalArray.join() // join('') or join('and')
console.log(joinArray)
const animalString = "dog,cat,panda"
// split: make a Array out of an String
const splitString = animalString.split(",") // split([Separator],[number])
console.log(splitString)
```

## Array to opposite direction

```js
const alphabet = ["a", "b", "c", "d"]
const revAlpahbet = alphabet.reverse()
console.log(revAlpahbet)
```

## Array make new array

```js
const student = ["minsu", "yeoghee", "chulsu", "donghee"]
const studentClass = student.slice(2, student.lenght)
console.log(studentClass)
```

**From now on, we only use this array.**

```js
class Student {
  constructor(name, age, enrolled, score) {
    this.name = name
    this.age = age
    this.enrolled = enrolled
    this.score = score
  }
}

const students = [
  new Student("A", 25, true, 50),
  new Student("B", 22, false, 40),
  new Student("C", 24, true, 75),
  new Student("D", 25, false, 66),
  new Student("E", 21, true, 90),
]
```

## Array Sort APIs

```js
// find a student with the score 90

const res = students.find((student) => student.score === 90)
console.log(res)
```

```js
// make an array of enrolled students// student[ ] = (enrolled ===true)

const res = students.filter((student) => student.enrolled)
console.log(res)
```

```js
// make an array of only score array

const res = students.map((student) => student.score)
console.log(res)
```

```js
//check if there is a student with the score lower than 50

// some(): like using ||
const res = students.some((student) => student.score < 50)
console.log(res) // true
// every(): like using &&
const res = students.every((student) => student.score < 50)
console.log(res) // false
```

### compute students average score

```js
//reduce(): Sequentially accumulate
const res = students.reduce((prev, curr) => {
  console.log("----------")
  console.log(prev)
  console.log(curr)
  return prev + curr.score
}, 0)
console.log(res)

//reduceRight(): Reverse accumulate
const res = students.reduceRight((prev, curr) => {
  console.log("----------")
  console.log(prev)
  console.log(curr)
  return prev + curr.score
}, 0)
console.log(res)

//modern JS
const res = students.reduce((prev, curr) => prev + curr.score, 0)
console.log(res / students.length)
```

### make a String conraining all the scores(should: "90,20,40,...")

```js
const res = students.map((student) => student.score).join()
console.log(res)

const res = students
  .map((student) => student.score)
  .filter((score) => score >= 50)
  .join()
console.log(res)
```

### sorted in ascending order(should: "1,2,3,...")

```js
// Ascending order
let res = students
  .map((student) => student.score)
  .sort((a, b) => a - b)
  .join()
console.log(res)
// Descending order
let res = students
  .map((student) => student.score)
  .sort((a, b) => b - a)
  .join()
console.log(res)
```

**More**

[Link youtube](https://www.youtube.com/watch?v=yOdAVDuHUKQ)
