최근 프로젝트를 진행하면서 http 통신 관련 라이브러리로 axios(XMLHTTPRequset기반)가 아닌 ky(fetch api기반)를 채택했다.

그 이유는

1. next의 edge runtime에서는 fetch만 지원 ([공식문서 참고](https://nextjs.org/docs/app/building-your-application/rendering/edge-and-nodejs-runtimes))
2. 용량이 훨씬 가벼움
   ky: 137KB, axios: 2.02MB (install 기준, 약 15배). axios가 아무래도 XMLHTTPRequest기반이다 보니, fetch에서 제공해주는 기능들을 추가하려고 해서 번들 사이즈가 굉장히 커진것.

velopert님도 cloudflare로 배포할 때 axios에서 ky로 바꾼 적이 있음 (XMLHTTPRequest 지원 안해서)
관련영사는 [여기](https://www.youtube.com/watch?v=DTZ5EzHAXI8)

추가)

- axios 대체제로 fetch 기반의 [redaxios](https://www.npmjs.com/package/redaxios)라는것도 있음. axios 최소환으로 호환되도록 만들었다고 한다.
- 원래 fetch는 웹 API에 속해있어서 웹이 아닌 단순 런타임 환경에서 JS를 이용하기 위한 Node.js 환경에서는 fetch를 사용할 수 없었다. 하지만 Node.js 18버전으로 업데이트 되면서 fetch를 사용할 수 있게 됐다.
