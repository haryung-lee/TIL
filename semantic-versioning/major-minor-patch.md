## MAJOR, MINOR, PATCH

보통 라이브러리를 설치하면 package.json에 아래와 같이 추가되는 것을 볼 수 있다.

```shell
  "dependencies": {
    "@emotion/react": "^11.10.5",
  },
```

![명세](https://user-images.githubusercontent.com/64428916/210973922-8932c46e-c338-4375-b79c-dd3ef44ad9f0.png)

11.10.5 버전을 나타내는 점과 숫자들이 있다. 이들은 명세에 맞춰 업데이트가 된다. 위 사진처럼 [MAJOR, MINOR, PATCH]로 구성된다. 이는 **소프트웨어 릴리즈 버전 넘버에 대한 네이밍 시스템**이다. 이와 같은 버전은 이 package가 어떤식으로 변경되었는가를 이해할 수 있게 해준다.

1. MAJOR Version <br>
   기존 api가 변경 혹은 삭제되었기 떄문에 update하면 동작하지 않을 수 있다는 경고의 의미이다.
2. MINOR Version <br>
   이전 버전과 호환되는 방식으로 API가 추가되었으니 살펴보라는 의미이다.
3. PATCH Version <br>
   이전 버전과 호환되는 버그 수정을 의미한다.
