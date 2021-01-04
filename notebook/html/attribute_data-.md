# Attribute data-

HTML5의 신규 속성(attribure)인 `사용자데이터속성` 입니다.

특정 요소와 연관되어 있지만 확정된 의미는 갖지 않는 데이터에 대한 확장 가능성을 염두에 두고 디자인되었습니다.

## How to use

```HTML
<!-- data-(name)="", (name) is not problem any words -->
<h1 data-title-number="1" class="title">Hello HTML5</h1>
```

## JavaScript 에서 접근하기

dataset 객체를 통해 data 속성을 가져오기 위해서는 속성 이름의 data- 뒷 부분을 사용합니다.`대시들은 camelCase로 변환되는 것에 주의해야 합니다.`

```javascript
const title = document.querySelector(".title")
console.log(title.dataset.titleNumber) // "1"
```

## CSS 에서 접근하기

순수 HTML 속성이기 때문에 CSS에서도 접근할 수 있습니다.

속성선택자로 접근하기

```CSS
.title[data-title-number='1'] {
  color: red
}
```

### Notice😢

인터넷 익스플로러11+ 은 표준을 지원하지만, 이전 버전들은 dataset을 지원하지 않습니다. IE 10 이하를 지원하기 위해서는 대신 getAttribute()를 통해 데이터 속성을 접근해야 합니다.

More)

- [Link MDN](https://developer.mozilla.org/ko/docs/Learn/HTML/Howto/%EB%8D%B0%EC%9D%B4%ED%84%B0_%EC%86%8D%EC%84%B1_%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0)
