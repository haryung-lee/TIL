## Error: Computed values are not permitted in an enum with string valued members.ts

최근, TS로 작업하던 중 아래와 같은 에러를 마주쳤다.

![스크린샷 2023-01-27 오후 8 32 09](https://user-images.githubusercontent.com/64428916/215078082-7ac45614-16b7-410e-9a34-e3cf7aead032.png)

구글링 검색 + Github 이슈 찾아보니 단순 리터럴은 가능하지만 `${foo}/boo` 와 같은 사용은 안되더라.
그런데 비교적 최근에 해당 이슈가 [해결되었다](https://github.com/microsoft/TypeScript/pull/50528).

하지만 **v.5.0**에 반영되어서 그 이전 버전에서는 적용되지 않는다........🥲

[playground](https://www.typescriptlang.org/play?ts=5.0.0-dev.20221121#code/MYewdgzgLgBARiAhrAvDA5AMxCdBuAKFElgHMlUNzdCBTMAVwFsYA5cAFQEtaAnANgCSUWkwDivRAAcAFgGEQAE1oQYAbwIwYAWRwRaMNAAMAJGoTIAvgHoz5K0YA0BSwSLgIIADa0AdF5BSAAp2MG4+IRFxSVkFZQgASiA)에서 직접 확인할 수 있다 !
