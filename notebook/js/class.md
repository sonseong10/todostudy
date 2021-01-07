# class(+ES6)

## desc

- template
- declare once
- no data in

**How to use**

```js
'use strict'
// 1. using class
class Preson {
	constructor(name,age) {
		this.name = name;
		this.age = age;
	}
	speak() {
		console.log(`${this.name}: hello`);
	}
}

// 2. getter&setter
class User {
	constructor(firstName, lastName, age) {
		this.firstName= firstName;
		this.lastName = lastName;
		this.age = age;
	}
	get age() {
		 return this._age;
	}

	set age(value) {
		/* if(value < 0) {
		*  	throw Error('age can not be negative');
		*/ }
		this._age = value < 0 ? 0 : value;
		this._age = value;
	}
}
const user1 = new User('Steve', 'job', -1);
console.log(user1.age);

// 3. Fields (public, private)
// may be soon using
class Experiment {
	publicField = 2;
	#privateField = 1;
}
const experiment = new Experiment();
console.log(experiment.publicField);
console.log(experiment.privateField);

// 4. Static properties and methods
// same soon using
class hiddenValue {
	static hidden ='Im Hidden';
	constructor(testNumber) {
		this.testNumber = testNumber;
	}

	static printHiddenValie() {
		console.log(hiddenValue.hidden);
	}
}
const testnum = new hiddenValue(1);
console.log(hiddenValue.hidden);
hiddenValue.printHiddenValie();
```

## 상속&다양성

```jsx
class Shape {
  constructor(width, height, color) {
    this.width = width
    this.height = height
    this.color = color
  }

  draw() {
    console.log(`drawing ${this.color} color of`)
  }
  getArea() {
    return this.width * this.height
  }
}

class Rectangle extends Shape {}

const rectangle = new Rectangle(20, 20, "Pink")
rectangle.draw()
console.log(rectangle.getArea())

//@overriding
class Triangle extends Shape {
  draw() {
    super.drow()
    console.log("finish draw triangle!")
  }
  getArea() {
    return (this.width * this.height) / 2
  }
}
const triangle = new Triangle(40, 40, "Blue")
triangle.drow()
console.log(triangle.getArea())

// instanceof using
console.log(rectangle instanceof Rectangle) //return true
console.log(triangle instanceof Rectangle) //return false
console.log(rectangle instanceof Shape) //return true
console.log(rectangle instanceof Object) //return true
```

**More**

JavaScript Reference [https://developer.mozilla.org/en-US/d...](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference)
