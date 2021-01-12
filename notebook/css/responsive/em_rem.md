# em and rem

반응형 웹페이지를 만들기 위해 고정값인 px 보다는 반응형 단위를 사용합니다.
%, vw, vh, ... 단위가 더 있으며 그 중에서 비슷해 보이지만 다른 em, rem을 설명합니다.

## Difference

`em`의 가까운 부모의 크기를 기준으로, `rem` html(루트) 크기를 기준으로합니다.

## How to use

```html
<div class="parent">
  <span>item</span>
  <div class="parent1">
    <span>item</span>
    <div class="parent2">
      <span>item</span>
    </div>
  </div>
</div>
```

### em

```css
body {
  font-size: 16px;
}

.parent,
.parent1,
.parent2 {
  font-size: 2em;
}
```

### rem

```css
html {
  font-size: 16px;
}

.parent,
.parent1,
.parent2 {
  font-size: 2rem;
}
```

**more**

[Link youtube](https://www.youtube.com/watch?v=S5uMXoGogkk)
