# CSS: cascade와 레이아웃

CSS 규칙은 선택자와 선언으로 구성된다. 여러 규칙이 같은 요소와 속성에 영향을 주면 cascade가 적용할 값을 결정한다. 단순히 '더 구체적인 선택자가 이긴다'로 끝나는 문제가 아니다. origin, importance, cascade layer, specificity, scoping proximity, source order 등 정해진 판단 단계가 있다.

## Box model

CSS 박스는 content, padding, border, margin으로 설명할 수 있다. 기본 `content-box`에서는 지정한 width가 content 영역에 적용된다. `border-box`에서는 지정한 width에 padding과 border가 포함된다. `box-sizing: border-box`는 흔히 쓰이는 선택이지만 CSS의 필수 규칙은 아니다.

## Normal flow

문서의 기본 흐름을 이해하기 전에 Grid나 Flexbox를 무조건 적용하지 않는다. block과 inline의 차이, formatting context, margin collapsing, containing block을 확인한 뒤 필요한 배치 모델을 선택한다.

## 실습

1. 개발자 도구에서 요소의 width와 box model을 확인한다.
2. `box-sizing`을 `content-box`와 `border-box`로 바꿔 실제 크기 차이를 관찰한다.
3. margin을 바꿔 주변 요소와의 간격을 확인한다.
4. 브라우저 창을 좁혀 media query가 적용되는 시점을 확인한다.

## 남은 공부

- cascade origin과 importance의 정확한 우선순위
- cascade layers와 inheritance
- initial, unset, revert, revert-layer
- block/inline formatting context
- Flexbox와 Grid의 sizing 알고리즘
- containing block, stacking context, positioned layout

## 출처

- [MDN: Cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Cascade)
- [MDN: Box model](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Box_model)
- [CSS Cascading and Inheritance Level 5](https://www.w3.org/TR/css-cascade-5/)
- [CSS Display Level 3](https://www.w3.org/TR/css-display-3/)
