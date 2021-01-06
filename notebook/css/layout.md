# Layout

다양한 이유(웹페이지 의 목적성, 디자인 요소 등)에 따라서 요소의 구성, 배치가 달라집니다.

기본적인 배치를 위해 그리드 레이아웃(그리드 시스템)을 사용 합니다.
그리드 레이아웃을 구현하기 위해 열(Columns)의 개수에 따라 12단/16단/24단 그리드라고 부르기도 합니다. 여기서는 따로 반응형을 설명하지 않습니다.

## Float grid system

- 장점 : 크로스브라우징 이슈를 예방 할 수 있습니다.
- 단점 : Float 사용으로 레이아웃이 망가질 수있으며 clearfix를 해야합니다.

**Code & Preview**

![float_layout](https://user-images.githubusercontent.com/68719427/103722122-9edf4d80-5012-11eb-924b-09d349fb3435.png)

Link [jsfiddle](https://jsfiddle.net/sonseong10/znLpbmtw/118/)

## Flexbox grid system

- 장점: 쉽게 정렬할 수 있고 반응형 제작도 편리해 집니다.
- 단점: IE하위 버전등 모든 웹 브라우저에서 작동 하진 않습니다.`크로스브라우징 이슈`

**Code & Preview**

![flex_layout](https://user-images.githubusercontent.com/68719427/103722533-8c194880-5013-11eb-8ec5-e4c0b01efcc7.png)

Link [jsfiddle](https://jsfiddle.net/sonseong10/04rc5eos/297/)

## Grid layout system

- 장점: 너비를 계산하지 않고 열/행의 너비 및 높이와 각 항목의 비율을 지정합니다.
- 단점: IE하위 버전등 모든 웹 브라우저에서 작동 하진 않습니다.`크로스브라우징 이슈`

**Code & Preview**

![grid_layout](https://user-images.githubusercontent.com/68719427/103723232-ef57aa80-5014-11eb-9544-38e652a3fe93.png)

Link [jsfiddle](https://jsfiddle.net/sonseong10/vzsxter6/99/)

**More**

- [Link Site](http://designbase.co.kr/webdesign-4/)
- [Link MDN](https://developer.mozilla.org/ko/docs/Learn/CSS/CSS_layout)
- [Link youtube](https://www.youtube.com/watch?v=eprXmC_j9A4)
