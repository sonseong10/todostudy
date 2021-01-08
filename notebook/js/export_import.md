# Export & import

## 모듈이란

- 여러 파일로 나누어서 작업 할 경우, `파일 사이에 코드를 주고받을 수 있기 때문에 파일을 나눠서 코드를 작성하는 것` 입니다.
- 이때 `파일 간에 주고 받을 수 있는 그 코드 조각, 단위 를 '모듈'`이라고 합니다.
- 모듈은 함수, 배열, 객체, 클래스, 상수 등 사용합니다.

## export

```js
//way1
sayHello =  (name) => console.log(`내 이름은 ${name}이야`);
export sayHello;// sayHello 함수 내보내기
//way2
export sayHello =  (name) => console.log(`내 이름은 ${name}이야`);// 선언과 함께 가능
```

### Example

```js
// 상수 내보내기
export const NAME = `김사람`

// 배열 내보내기
export let oddNumbers = [1, 3, 5, 7, 9]

// 클래스 내보내기
export class Student {
  constructor(name) {
    this.name = name
  }
}
```

### export default(=only one)

작성한 파일 내에서 모듈이 1개인 경우 export 방식 보단 export default 방식으로 내보내는 것을 권장합니다.

```js
export default sayHello = (name) => console.log(`내 이름은 ${name}이야`)
```

### export as(name change)

내보낼 모듈의 이름을 작성한 모듈이 아닌 내가 지정한 이름으로 내보내야 한다면 `export 모듈 as 사용할이름` 형식으로 사용합니다.

```js
sayHello =  (name) => console.log(`내 이름은 ${name}이야`);
export default sayHello as myName;

export {sayHello as hihi, sayBye as goodbye};// 다중 사용 가능
```

## import

내보낸 모듈을 다른 파일에서 사용할 경우 `import { 모듈(들) } from "모듈을 내보낸 파일 경로"`

```js
//basic
import { sayHello } from "./temp.js"
//multiple
import { sayHello, sayGoodBye } from "./temp.js"
//import as
import { sayHello as hi, sayBye as goodbye } from "./temp.js"
```

**More**

[Link youtube](https://www.youtube.com/watch?v=cRHQNNcYf6s)
