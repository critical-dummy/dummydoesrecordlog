# JavaScript: 언어와 브라우저 API 구분하기

ECMAScript는 JavaScript 언어의 핵심 문법과 의미, 내장 객체 등을 정의한다. DOM, 이벤트, Fetch, Web Storage 같은 기능은 브라우저가 제공하는 Web API다.

브라우저에서 실행되는 JavaScript는 ECMAScript 기능과 호스트 환경이 제공하는 API를 함께 사용한다. Node.js 같은 다른 환경에서는 제공되는 호스트 API가 다르다.

## DOM 조작을 배울 때

- DOM은 JavaScript 언어의 일부가 아니라 문서를 표현하는 플랫폼 API다.
- 요소 조회, 속성 변경, 노드 생성과 제거는 DOM API의 동작이다.
- 이벤트 리스너는 이벤트 대상과 전파 단계에 따라 호출된다.
- 화면의 표현은 CSS에 두고, JavaScript는 상태 변경에 집중할 수 있다.

## script 로딩

외부 classic script의 `defer`는 HTML 파싱과 다운로드를 병행하고 파싱이 끝난 뒤 실행하도록 한다. module script는 기본적으로 지연 실행 특성을 갖는다. 모든 스크립트에 무조건 `defer`를 붙이는 것이 원칙은 아니다. 스크립트가 필요한 시점과 의존 관계를 보고 선택한다.

## 실습

1. 개발자 도구 콘솔에서 `document.querySelector()`로 요소를 조회한다.
2. 이벤트 리스너를 등록하고 클릭 이벤트가 언제 전달되는지 확인한다.
3. `aria-pressed` 같은 상태 속성이 실제 UI 상태와 동기화되는지 확인한다.
4. JavaScript를 끈 상태에서도 문서의 핵심 내용과 링크를 사용할 수 있는지 확인한다.

## 남은 공부

- lexical environment, scope, closure
- primitive와 object, reference semantics
- task queue, microtask queue, event loop
- event propagation: capturing, target, bubbling
- DOM mutation과 MutationObserver
- form submission, modules, fetch, async/await

## 출처

- [ECMA-262](https://tc39.es/ecma262/)
- [MDN: JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
- [DOM Standard](https://dom.spec.whatwg.org/)
- [MDN: script element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script)
