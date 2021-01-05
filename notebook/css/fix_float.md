# Fix float

## Cause of occurrence

![float 사전 의미](https://media.vlpt.us/images/im_hyeonji/post/7e85c3d5-04b6-4bfd-87f5-948ff33b8c77/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202020-06-23%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%2010.39.39.png)

자식요소가 `float`속성을 가지게 된다면 부모, 형제요소는 자식의 높이를 감지할 수 없기 때문에를 인식하지 못하게 되지만 안에 텍스트(혹은 인라인 요소들)는 float된 요소가 어디있는지 알 수 있어서 종종 레이아웃이 망가지게 된다.

## 부모요소 overflow 활용하기

- `overflow: auto` 또는 `overflow: hidden` 사용
- 직관적인 방법이 아니여서 좋은 해결법은 아닙니다.

## 빈 요소에 clear 활용하기

- 빈요소를 추가하여 clear 부여하기
- 의미없는 요소를 생성하여 좋은 해결법은 아닙니다.

## 가상요소로 clear 적용

- 의미없는 요소 생산(x)
- 직관적인 해결법

## Code로 확인하기

[Link jsfiddle](https://jsfiddle.net/sonseong10/85dhn9go/24/)
