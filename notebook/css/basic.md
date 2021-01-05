# 계단식, 우선순위, 상속성

## notice

CSS적용을 위한 HTML파일

```html
<div class="parent">
  <h1 id="foo" class="boo" title="hoo">This is my heading.</h1>
</div>
```

## 계단식 (cascade)

CSS 의미에서 알 수 있듯이 마지막에 나오는 규칙이 사용 될 것입니다.

```css
h1 {
  color: red;
}
h1 {
  color: blue;
}
/* color blue */
```

## 우선 순위(Specificity)

동일한 요소에 적용될 수 있는 경우, 브라우저가 어떤 규칙을 적용할 지 결정하는 방법입니다.

```css
#foo {
  color: red;
}
h1 {
  color: blue !important;
}
.boo {
  color: pink;
}
h1[title^="ho"] {
  color: green;
}
/* color blue */
```

**우선 순위**

0. !important
1. id
2. class, attribute
3. tag
4. \*

## 상속 (Inheritance)

부모 요소에서 설정된 일부 CSS 속성 값은 자식 요소에 의해 상속되며, 일부는 그렇지 않습니다.

```css
.parent {
  color: blue;
}
/* h1 color blue */
```

More

- [Link MDN](https://developer.mozilla.org/ko/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance)
- [Selector game](https://flukeout.github.io/)
