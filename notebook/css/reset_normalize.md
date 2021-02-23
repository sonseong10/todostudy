# CSS 통일 시키기

웹 브라우저마다 요소의 Default 스타일이 다릅니다.
우린 초기 작업 시간을 단축하기 위해 다른 스타일을 통일 시켜 진행할 필요가 있습니다.

## Reset CSS

브라우저 간의 차이를 최대한 제거하여, 스타일이 0인 상태를 만들기 위해 사용하는 방법입니다.

> 대표적인 사용법으로는 [meyerweb](https://meyerweb.com/eric/tools/css/reset/)가 있습니다.

**Example**

```css
ul {
  margin: 0;
  padding-left: 0;
}

li {
  list-style: none;
}
```

## Normalize CSS

모든 스타일을 0가 아닌 ≒0으로 요소의 디자인을 어느 정도 보존하며 통일하는 방법입니다.

> 대표적인 사용법으로는 [necolas](https://necolas.github.io/normalize.css/)가 있습니다.

**Example**

```css
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
```

## 결론

두 가지 방식 모두 훌륭한 사용법으로 많은 개발자분이 사용하며 프로젝트의 규모와 성질에 맞게 사용해야 합니다.
