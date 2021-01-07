# ==(equality) and ===(identity)

타입변환의 유/무를 확인 할 수 있습니다.

`== 타입변환(O), === 타입변환(X)`

**Example**

```js
1 == "1" // 1: number = 1: number true
1 === "1" // 1: number ≠ 1: string fales
null == undefined // true
null === undefined // false
```

안전한 타입 체크와 더 좋은 코드를 위해 엄격한 **동등비교 연산자(===)** 를 사용하는 것이 바람직합니다.

**More**

[Link MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Equality_comparisons_and_sameness)
