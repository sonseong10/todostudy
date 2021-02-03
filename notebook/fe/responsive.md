# Responsive Web

## Responsive Web 탄생

![Responsive-Web-Design](http://www.creativewerkdesigns.com/wp-content/uploads/2016/07/Responsive-Web-Design.png)

과거에는 컴퓨터를 통해 웹을 활용 해왔다면 스마트폰의 등장과 함께 요즘은 디스플레이의 크기가 다양해졌습니다, 다양한 디바이스 버전 별로 따로 페이지를 제작해서 관리했지만, 반응형 웹을 적용할 경우 하나의 소스로 여러개의 디바이스에서도 최적화되어 보여지기 때문에 운영, 유지보수 및 마케팅 비용까지 절감할 수 있다는게 큰 장점입니다.

## 모든 디스플레이 크기를 호환해야 하는가?

정답은 '아니다' 이다. 모든 디스플레이 크기로 코딩을 하게 된다면 파일용량을 책임지지 못 할 것입니다. 'n'px 차이 정도의 여백을 활용 함으로써 크게 3가지의 디스플레이로 디자인을 합니다.

`PC모니터, 태블릿, 스마트폰` 또는 break-point(중단점) 기준으로 그리드 레이아웃을 잡고 디자인합니다.

## Responsive Web 제작 방법

다양한 방법으로 반응형 디자인을 제작 할 수 있습니다.

```html
<link rel="stylesheet" media="screen and (max-width: 768px)" href="style.css" />
```

```css
@media screen and (max-width: 768px) {
  body {
    background-color: lightgreen;
  }
}
```

```js
element.getboundingclientrect()
```

위의 코드는 각각 HTML, CSS, JS로 기초적인 반응형을 만들 수 있거나 이벤트 헨들링 할 수 있습니다.

**More**

[Link MDN html](https://developer.mozilla.org/ko/docs/Web/HTML/Element/link)

[Link MDN css](https://developer.mozilla.org/ko/docs/Web/CSS/@media)

[Link MDN js](https://developer.mozilla.org/en-US/docs/Web/API/Element/getBoundingClientRect)

## Etc

좀더 자세히 정리한 CSS파일은 링크로 확인 바랍니다.

[em_rem](../css/responsive/em_rem.md)

[@media](../css/responsive/media.md)
