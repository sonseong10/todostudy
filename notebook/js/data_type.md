# JavaScript에는 7 가지 기본 데이터 유형

- `number`

  모든 종류의 숫자 : 정수 또는 부동 소수점, 정수는 ± 2^53로 제한됩니다 .

> `bigint`
>
> > 임의 길이의 정수입니다.
>
> ```js
> // the "n" at the end means it's a BigInt
> // 현재 BigInt는 Firefox / Chrome / Edge에서는 지원되지만
> // Safari / IE에서는 지원되지 않습니다.
> const bigInt = 1234567890123456789012345678901234567890n
> console.log(typeof bigInt) //bigint
> ```

- `string`

  문자열. 문자열에는 0 개 이상의 문자가있을 수 있으며 별도의 단일 문자 유형은 없습니다.

  ```js
  const ar = "ar"
  const char = "ch" + ar
  console.log("char") // char
  console.log(char) // char
  console.log(`${char}`) // char //``=백틱
  ```

- `boolean`

  false: 0, null, undefined, NaN, ""

  true: other then

- `null`

  알 수없는 값의 경우 – 단일 값을 가진 독립형 유형

- `undefined`

  할당되지 않은 값의 경우 – 단일 값이 있는 독립형 유형

- `object`
  Key와 Value 쌍으로 더 복잡한 데이터 구조를 위한 용.
  function, Array ...

  ```js
  const objectname = { key : value }; // object
  function [functionname]([parameter]){ }; //[] = Can be omitted
  const num = [1,2,3] // Array
  ```

- `symbol` (+ES6)

  고유 식별자 용.

  ```js
  const symbol1 = Symbol("id")
  const symbol2 = Symbol("id")
  console.log(symbol1 === symbol2) // false
  const symbol3 = Symbol.for("id")
  const symbol4 = Symbol.for("id")
  console.log(symbol3 === symbol4) // true

  console.log(`${symbol1.descrription}`) // id
  ```

  number - special numeric values\*

  ```js
  const infinity = 1 / 0
  const negativeInfinity = -1 / 0
  const nan = "String" / 1
  console.log(`${infinity}, ${negativeInfinity}, ${nan}`)
  ```

> +α JS Dynamic typing

```js
let text = "hello"
console.log(typeof text) // String
console.log(text.charAt(0)) // h
text = 1
console.log(typeof text) // Number
text = "6" / "3"
console.log(typeof text) // Number
console.log(text.charAt(0)) // Type error
```
