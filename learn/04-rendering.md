# 브라우저 렌더링 과정

브라우저는 HTML과 CSS를 해석하고, 스타일과 레이아웃을 계산한 뒤 화면에 그린다. 개념적으로 HTML parsing 및 DOM 구성, CSS parsing 및 CSSOM 구성, style calculation, layout, paint, compositing 단계를 구분할 수 있다.

이 목록은 학습을 위한 모델이다. 실제 브라우저 엔진은 병렬 처리, 증분 업데이트, 캐시, 별도 스레드 및 GPU 합성 등을 사용한다. 모든 DOM 변경이 항상 전체 파이프라인을 처음부터 다시 수행하는 것은 아니다.

## Layout과 paint

요소의 크기나 위치에 영향을 주는 변경은 layout을 유발할 수 있다. 색상처럼 기하학적 크기에 영향을 주지 않는 변경은 layout 없이 paint만 다시 필요할 수 있다. 정확한 비용은 속성, 문서 상태, 브라우저 구현에 따라 달라진다.

성능을 추측만으로 최적화하지 않는다. 먼저 성능 도구에서 실제 작업과 병목을 측정한다.

## 실습

1. 개발자 도구의 Performance 패널을 연다.
2. 페이지를 새로고침해 초기 로딩의 주요 작업을 관찰한다.
3. DOM을 바꾸는 작업과 CSS 표현만 바꾸는 작업을 각각 기록한다.
4. style recalculation과 layout 관련 이벤트가 어떻게 달라지는지 살핀다.
5. 브라우저와 버전에 따라 기록이 다를 수 있으므로 환경을 함께 적는다.

## 남은 공부

- preload scanner와 resource discovery
- parser-blocking, render-blocking, defer, async, module
- style recalculation과 invalidation
- layout thrashing
- paint invalidation과 compositing layers
- requestAnimationFrame과 event loop의 관계
- Core Web Vitals 및 실제 사용자 측정

## 출처

- [MDN: How browsers work](https://developer.mozilla.org/en-US/docs/Web/Performance/Guides/How_browsers_work)
- [MDN: Critical rendering path](https://developer.mozilla.org/en-US/docs/Web/Performance/Guides/Critical_rendering_path)
- [Chromium: The Rendering Critical Path](https://www.chromium.org/developers/the-rendering-critical-path/)
