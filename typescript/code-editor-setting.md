## 코드 편집기 설정

- 모든 타입스크립트 프로젝트는 루트 디렉터리에 tsconfig.json이라는 파일이 존재해야 한다.

```json
{
	"compilerOptions": {
		"lib": ["es2015"].
		"module": "commonjs",
		"outDir": "dist",
		"sourceMap": true,
		"strict": true,
		"target": "es2015"
	},
	"include" : [
		"src"
	]
}
```

| 옵션    | 설명                                                                                                                                           |
| ------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| include | TSC가 타입스크립트 파일을 찾을 디렉터리                                                                                                        |
| lib     | TSC가 코드 실행 환경에서 이용할 수 있다고 가정하는 API(ES5의 Function.prototype.bind, ES2015의 Object.assign, DOM의 document.querySelector 등) |
| module  | TSC가 코드를 컴파일할 대상 모듈 시스템(CommonJS, SysyemJS, ES2015 등)                                                                          |
| outDir  | 생성된 자바스크립트 코드를 출력할 디렉터리                                                                                                     |
| strict  | 유효하지 않은 코드를 확이할 때 가능한 엄격하게 검사. 이 옵션을 이용하면 코드가 적절하게 타입을 갖추도록 강제할 수 있음                         |
| target  | TSC가 코드를 컴파일할 자바스크립트 버전(ES3, ES5, ES2015, ES2016 등)                                                                           |

- tslint.json: TSLint 설정을 정의하는 파일
  - 기본값으로 채워진 tslint.json 파일 만드는 명령어
    ```bash
    .node_modules/.bin/tslint -init
    ```
