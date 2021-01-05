# Block format context, Block context

블록 레벨 요소를 렌더링 하는데 사용하는 CSS의 비주얼 서식 모델들 입니다.
(✅ 표시는 알아두면 좋은 방식입니다.)

## Block format context

부모요소가 자식요소를 어디까지 포함할 것인지 입니다.
다음중 하나에 의해 생성 됩니다.

- [ ] 루트 또는 이를 포함하는 요소
- [x] float(float이 none이 아닌 요소)
- [x] 절대위치로 지정된 요소(position: absolute or fixed)
- [x] 인라인블록(display: inline-block)
- [ ] 테이블 셀(display: table-cell)
- [ ] 테이블 캡셥(display: table-caption)
- [x] overflow가 visible이 아닌 요소
- [ ] flex box(disblay: flex or disblay: inline-flex)

More

- [Link Mdn](https://developer.mozilla.org/ko/docs/Web/Guide/CSS/Block_formatting_context)
- [Link Youtube](https://www.youtube.com/watch?v=AteI3GCambQ)

## Block context

자식요소가 자신을 포함하는 부모요소를 찾는법 입니다.
컨테이닝 블록은 가장 가까운 블록 레벨, 조상의 콘텐츠 영역이거나 항상 그런 것은 아닙니다. 요소의 컨테이닝 블록을 결정하는 요인을 살펴보겠습니다.

`사용자 에이전트(브라우저 등)는 문서를 그릴 때 모든 요소에 대해 상자(박스)를 생성합니다. 컨테이닝 블록의 식별 과정은 position 속성에 따라 완전히 달라집니다.`

![render box](https://mdn.mozillademos.org/files/16558/box-model.png)

### 컨테이닝 블록 식별

- [ ] position 속성이 static, relative, sticky 중 하나이면, 컨테이닝 블록은 가장 가까운 조상 블록 컨테이너(block, list-item...), 또는 가장 가까우면서 서식 맥락을 형성하는 조상 요소(table, flex, grid...)의 콘텐츠 영역 경계를 따라 형성됩니다.
- [x] position 속성이 absolute인 경우, 컨테이닝 블록은 position 속성 값이 static이 아닌(fixed, absolute, relative, sticky) 가장 가까운 조상의 내부 여백 영역입니다.
- [x] position 속성이 fixed인 경우, 컨테이닝 블록은 뷰포트나 페이지 영역(페이지로 나뉘는 매체인 경우)입니다.

More

- [Link Mdn](https://developer.mozilla.org/ko/docs/Web/CSS/All_About_The_Containing_Block)
