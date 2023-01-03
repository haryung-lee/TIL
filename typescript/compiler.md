## 컴파일러

- 코드 작성 → 컴파일러를 통해 파싱하여 abstract syntax tree(AST)로 변환 → bytecode로 변환 → 런타임을 통해 바이트코드 입력해 평가하고 결과 얻음
- 과정
  1. 프로그램이 AST로 파싱된다.
  2. AST가 바이트코드로 컴파일된다.
  3. 런타임이 바이트코드를 평가한다.
- 타입스크립트는 컴파일러가 코드를 바이트코드 대신 JS 코드로 변환한다.
- TS 컴파일러는 AST를 만들어 결과 코드를 내놓기 전에 타입 확인을 거친다.
- 보통 JS 컴파일러와 런타임은 엔진이라는 하나의 프로그램으로 합쳐진다. ex) 크롬 v8