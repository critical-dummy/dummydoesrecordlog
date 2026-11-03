# Web platform study

이 디렉터리는 HTML, CSS, JavaScript를 다시 기초부터 검토하고 실제 브라우저에서 확인한 결과를 남기는 작업 공간이다.

학습 순서는 언어별 문법 암기가 아니라 브라우저가 문서를 처리하는 순서와 각 기술의 책임을 기준으로 잡는다.

1. HTML 문서 구조와 의미
2. CSS의 cascade, formatting context, box model, layout
3. JavaScript 언어와 DOM API의 구분
4. 브라우저의 parsing, style, layout, paint, compositing
5. 접근성, 반응형 동작, 성능, 표준 적합성

## 규칙

- 명세와 브라우저 동작을 구분한다. 명세가 정의하는 것과 특정 브라우저 구현의 세부 사항을 같은 사실처럼 쓰지 않는다.
- MDN은 설명 자료로 활용하되, 규범적 동작은 WHATWG, W3C, Ecma International 등의 명세를 우선 확인한다.
- 코드를 추가할 때는 그 코드가 해결하는 구체적인 문제를 기록한다.
- 데모가 작동한다는 사실만으로 접근성, 호환성, 성능까지 검증했다고 주장하지 않는다.
- 최적화는 측정한 병목을 대상으로 한다.
- 실험 결과와 아직 확인하지 못한 가설을 분리한다.

## 현재 실습 사이트

- `index.html`: 학습 노트의 첫 페이지
- `site.css`: 문서의 읽기 흐름과 반응형 표현
- `site.js`: 읽기 영역 폭을 바꾸는 작은 DOM 상호작용

실습 사이트는 프레임워크나 빌드 도구 없이 정적 파일로 구성한다. 현재 단계에서 별도 도구가 필요하지 않기 때문이다.

## 진행 기록

### 2026-11-03 — 시작

- 저장소의 기존 파일을 확인했다. 기존 `log1`, `log2`는 변경하지 않는다.
- WHATWG HTML Living Standard, MDN의 CSS box model 및 browser rendering 문서, Ecma International의 ECMAScript 표준을 1차 학습 출처로 선정했다.
- HTML 문서 구조와 브라우저 렌더링을 소개하는 정적 실습 페이지를 작성했다.
- 이 단계는 기초 자료 조사와 첫 번째 구현이다. 전체 학습 완료를 뜻하지 않는다.

## 주요 참고 자료

- [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/)
- [MDN: HTML basics](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content)
- [MDN: CSS box model](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Box_model)
- [MDN: CSS cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Cascade)
- [MDN: JavaScript guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
- [ECMA-262](https://tc39.es/ecma262/)
- [DOM Standard](https://dom.spec.whatwg.org/)
- [MDN: How browsers work](https://developer.mozilla.org/en-US/docs/Web/Performance/Guides/How_browsers_work)
