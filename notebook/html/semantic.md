# Semantic Markup

시맨틱(Semantic)이란 "의미론적인" 의 뜻을 가지며 마크업(Markup)이란 HTML 태그로 문서를 작성하는 것을 말한다.
`즉, 시맨틱 마크업이란 의미를 잘 전달하도록 작성하는 것을 말한다.`

**Why should it be used?**

1. 유지보수를 위하여 사용해야 합니다.
2. 직관적인 의미를 보여주기 위하여 사용해야 합니다.
3. 올바른 레이아웃 구성해야 합니다.
4. 검색 엔진(SEO)은 페이지의 검색 랭킹에 영향을 줄 수 있는 중요한 키워드로 간주합니다.

```html
<!-- bad -->
<div>
  <div>
    <div>
      <div>
        <b>item1</b>
      </div>
      <div class="item">item2</div>
    </div>
  </div>
</div>
```

```html
<!-- good -->
<header>
  <nav>
    <ul>
      <li>
        <strong>item1</strong>
      </li>
      <li>item2</li>
    </ul>
  </nav>
</header>
```

### 내가 생각하는 Semantic Markup

```
<title>은 최대한 변경을 자제
레이아웃 구성은
 <header>, <footer>, <article>, <section>, <main> 그리고 <nav>사용
<b>, <i> 태그 대신 <strong>, <em> 사용
한 페이지당 필수적으로 <h1> 태그 1회만 사용
리스트를 구성할때 <ul>, <ol> 그리고 <dl> 사용 등등...
```

### Result😎

의미적으로 대체가능한 태그가 있는지 사용전에 생각하는 습관이 필요 합니다.

More

[Link, Semantics MDN](https://developer.mozilla.org/en-US/docs/Glossary/Semantics)
