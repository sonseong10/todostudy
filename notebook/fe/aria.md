# For all Web users

웹은 다양한 사용자들이 존재합니다. FE 개발자라면 모든 사용자에게 모든 기능을 최대한 지원해야 합니다.

- 발생하는 문제점

> 페이지를 새로고침하지 않고 콘텐츠를 Ajax 방식으로 갱신했을 때 전맹 시각장애인은 어떤 응답을 받을 수 있을까? 갱신 사실을 보조기기에 즉시 알려줄 수 있는 방법이 필요합니다.

## 해결방안

먼저 전맹 시각장애인분들이 어떻게 웹 브라우저를 이용하는지 알아야 합니다.

**Screen reader tool**

- [Nvaccess](https://www.nvaccess.org/)
- [Orca](https://wiki.gnome.org/Projects/Orca)
- [Screen reader tool Top 10](https://usabilitygeek.com/10-free-screen-reader-blind-visually-impaired-users/)

### ARIA

`WAI-ARIA`(Web Accessibility Initiative – Accessible Rich Internet Applications)는 웹 페이지, 특히 동적 콘텐츠, 그리고 Ajax, HTML, 자바스크립트 및 관련 기술로 개발된 사용자 인터페이스 구성 요소의 접근성을 증가시키는 방법에 대해 규정한 [W3C](https://www.w3.org/TR/wai-aria-1.1/)가 출판한 기술 사양입니다.

**Example**

```html
<!-- 닫기 버튼 -->
<button type="button" aria-label="Close Popup">X</button>
```

> ⚠ 보조기기가 이 기술을 처리하는 방법에 대한 의견에는 차이가 있을 수 있습니다. 위에서 제공하는 정보는 그러한 의견 중 하나일 뿐 규범이 아닙니다.

[Code 출처 MDN](https://developer.mozilla.org/ko/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-label_attribute)
