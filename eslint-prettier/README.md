# ESLint

(참고) https://eslint.org/docs/latest/use/core-concepts/

- Javascript 코드에서 잠재적인 버그(런타임 버그, 권장 사례 미준수, 스타일 이슈...)를 찾아내고 보고하는 도구
- 코드의 일관성을 높이고 버그를 방지하는 것이 목적
- "규칙 기반" 코드 검사
- 모든 규칙은 플러그인 방식으로 구성되어 필요에 따라 추가하고 변경 가능

### Rules

- 코드가 특정 기대 사항을 충족하는 지 검증
- 기대 사항을 충족하지 않을 경우 어떻게 처리할 지 정의
- 위반 사항에 대한 자동 수정 제공
  - `--fix` 커맨드 옵션 사용, 편집기 확장

### Configuration Files

- ESLint의 설정을 정의하는 공간
- ESLint의 설정: 내장 규칙, 규칙 적용 방식, 플러그인, 공유 설정...
  - 플러그인: 규칙, 설정, 프로세서, 환경 등을 포함하는 npm 모듈<br/> 커스텀 규칙을 포함할 수 있고 `React`, `Angular` 등 라이브러리나 프레임워크를 지원하는 데 사용<br/>
    ex) `eslint-plugin-react`
  - 공유 설정: 대개 내장 규칙을 사용해 스타일 가이드를 강제하는 데 사용<br/>
    ex) `eslint-config-airbnb`, `eslint-config-prettier`

### Parsers

- ESLint가 코드를 이해할 수 있도록 코드를 추상 구문 트리(Abstract Syntax Tree)로 변환해 주는 도구
- 기본적으로 표준 JS와 호환되는 `Espree` 라는 내장 파서 사용
- 표준 구문을 넘어서거나 다른 언어(Typescript)를 사용할 때는 커스텀 파서가 필요함
- 커스텀 파서는 ESLint가 비표준 코드나 다른 언어의 구문을 이해할 수 있게 함
  - ex) `@typescript-eslint/parser`

### Custom Processors

- 다른 종류의 파일에서 JS 코드를 추출하여 파일을 검사할 수 있도록 도와주는 도구
- ex) `eslint-plugin-markdown`: markdown 문서 안에 있는 JS 코드 블록을 검사할 수 있게 해주는 프로세서

<br/><br/>

# Prettier

(참고) https://prettier.io/docs/en/

- 코드 "포맷팅" 도구
- 코드의 모양을 자동으로 정리해줌
- 지원하는 언어, 형식: `JavaScript`, `TypeScript`, `JSX`, `Angular`, `Vue`, `CSS`, `HTML`, `JSON`, `YAML`, `Markdown` ...
- 코드의 기존 스타일을 무시하고 사용자가 정의한 일관된 스타일을 따르도록 보장

### Option Philosophy

https://prettier.io/docs/en/option-philosophy

- Prettier는 몇 가지 옵션을 제공하지만 앞으로 더 많은 옵션을 추가하지 않을 것.
- 왜? Prettier는 코드 포맷팅에 대한 논쟁을 끝내기 위해 설계됨.<br/>옵션이 많아지면 오히려 어떤 옵션을 사용할지에 대한 논쟁이 생겨 본래 목적에서 벗어남.
- 기술적 이유로 꼭 필요한 경우에는 옵션이 추가될 수 있지만 포맷팅 관련 옵션은 변경 X

### Options

| **옵션**                     | **설명**                                          | **기본값** | **옵션 값**                           |
| ---------------------------- | ------------------------------------------------- | ---------- | ------------------------------------- |
| `printWidth`                 | 한 줄의 최대 길이                                 | 80         | -                                     |
| `tabWidth`                   | 탭 문자를 공백으로 대체할 때 공백 개수            | 2          | -                                     |
| `useTabs`                    | 들여쓰기에 탭 문자를 사용할지 여부                | false      | `true`, `false`                       |
| `semi`                       | 문장 끝에 세미콜론을 추가할지 여부                | true       | `true`, `false`                       |
| `singleQuote`                | 문자열에 싱글 쿼트를 사용할지 여부                | false      | `true`, `false`                       |
| `trailingComma`              | 마지막 요소 뒤에 쉼표를 추가할지 여부             | none       | `none`, `es5`, `all`                  |
| `bracketSpacing`             | 객체 리터럴의 괄호 안에 공백을 추가할지 여부      | true       | `true`, `false`                       |
| `jsxBracketSameLine`         | JSX의 닫는 괄호를 같은 줄에 배치할지 여부         | false      | `true`, `false`                       |
| `arrowParens`                | 화살표 함수의 매개변수가 하나일 때 괄호 사용 여부 | always     | `always`, `avoid`                     |
| `proseWrap`                  | Markdown 문서의 줄 바꿈 방식                      | preserve   | `always`, `never`, `preserve`         |
| `htmlWhitespaceSensitivity`  | HTML의 공백 민감도 설정                           | css        | `css`, `strict`, `ignore`             |
| `endOfLine`                  | 파일의 줄 끝 스타일 설정                          | auto       | `auto`, `lf`, `crlf`, `cr`            |
| `quoteProps`                 | 객체의 속성 이름에 대해 따옴표를 사용할지 여부    | as-needed  | `as-needed`, `consistent`, `preserve` |
| `embeddedLanguageFormatting` | 코드 안의 내장 언어의 포맷팅 여부                 | auto       | `auto`, `off`                         |
