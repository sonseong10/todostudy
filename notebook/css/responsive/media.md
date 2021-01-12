# @media

웹 브라우저가 리사이징 되거나 장치 환경(테블릿, 모바일 ...)이 일치하는 경우에만 CSS를 적용할 수 있는 방법을 제공합니다.

`반응형 웹을 제작하기 위해 필수입니다.`

## Hoe to use

```css
@media media-type and (media-feature-rule) {
  /* CSS rules go here */
}
```

### 미디어 쿼리 구문의 구성 요소

- 여기 코드가 어떤 미디어를 위한 것인지 브라우저에 알려주는 미디어 유형(예를 들어, 인쇄 또는 화면).
- 괄호로 묶은 CSS 규칙이 적용되기 위해 전달되어야 하는 규칙 또는 조건문 격인 미디어 표현식.
- 조건문을 통과하고 미디어 유형이 올바른 경우 적용되는 CSS 규칙 집합.

## 분기점을 선정하는 방법

모든 상황에 맞는 디자인을 만들기 위해 무분별하게 사용할경우 오히려 독이 될 수 있으며 대표적인 분기점을 만들어야 합니다. 미디어 쿼리가 도입되는 지점을 **breakpoints**라고 합니다.

### Example

breakpoints 기준의 한 예시 일뿐 정답이 아님을 알아야 합니다.

|  Kind   | Breakpoint |
| :-----: | :--------: |
| Desktop |   1024px   |
| Tablet  |   760px    |
|  Phone  |   320px    |

**More**

[Link MDN](https://developer.mozilla.org/ko/docs/Web/CSS/@media)
