# javascript

### 자바스크립트 엔진

- 자바스크립트 코드를 해석하고 실행하는 역할.
- 자바스크립트 코드를 기계어 코드로 변환.
- 추가 기능 없이 `ECMA-262`를 구현하기 때문에 `ECMAScript` 엔진이라고도 한다.
  - `ECMAScript`만 구현하고 호스트에 의해 확장되도록 되어 있어 다양한 런타임 환경에서 사용할 수 있다.
- `V8`: Chromium 프로젝트 (Node.js, Deno, Edge, Opera)
- `SpiderMonkey`: Firefox
- `JavaScriptCore`: Safari, Bun

### 자바스크립트 런타임

- ECMAScript의 호스트로 자바스크립트 코드를 실행할 수 있는 "환경"을 제공한다.
- "자바스크립트 엔진을 내장"하고 추가 기능을 정의하여 코드 실행을 지원한다.
  - 추가 기능: 콜스택, 이벤트 루프, 웹 API(DOM, History ...), 파일 시스템, 프로세스 관리...
  - 추가할 수 있는 기능에 대한 규칙이 없어 Node.js, Deno, Bun은 모두 다른 파일 시스템을 구현한다.
- `Chrome`, `Firefox`, `Edge`, `Safari`, `Node.js`, `Deno`, `Bun` ...
