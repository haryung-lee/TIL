## 상대 참조

- 커밋들을 해시로 구분하고 사용하는 것이 아주 편하지는 않을 것이다.
  - 해시 값을 보기 위해 `git log` 명령어를 쳐야하는 등
- 상대 참조로 기억할 만한 지점에서 출발해서 이동하여 다른 지점에 도달해 작업을 할 수 있다.
- 한번에 한 커밋 위로 움직이는 `^`
- 한번에 여러 커밋 위로 올라가는 `~<num>`
- `~` (틸드) 연산자 : 올라가고 싶은 부모의 갯수가 뒤에 숫자로 온다.
- -f 옵션을 넣으면 강제로 옮길 수 있다.

> 문제 1) bugFix의 부모 커밋을 체크아웃 하기

![4](https://user-images.githubusercontent.com/64428916/210366093-5ffa20f3-7b5c-4dc9-855b-b54bf42d4aa7.png)

![5](https://user-images.githubusercontent.com/64428916/210366102-032d88f2-3b35-4745-b31d-25f9421b64f6.png)

```bash
git checkout bugFix^
```

> 문제 2)

![6](https://user-images.githubusercontent.com/64428916/210366114-e2ac5190-4601-4b2d-9828-0694808a6b72.png)

![7](https://user-images.githubusercontent.com/64428916/210366118-b42876f6-1159-4ca5-9921-e76dedbc7a5f.png)

```bash
git checkout HEAD~4
```

> 문제 3) main 브랜치를 HEAD 위로 3개 올리기

![8](https://user-images.githubusercontent.com/64428916/210366379-62aee19d-065a-431f-a164-6136bd761e76.png)

![9](https://user-images.githubusercontent.com/64428916/210366385-ebb84627-3a2e-46ac-a6a8-6746c0f23bcd.png)

```bash
git branch -f main HEAD~3
```

> 문제 4) 아래 그림의 커밋이 다음과 같이 변하려면?

![10](https://user-images.githubusercontent.com/64428916/210366609-b4b37477-c759-4633-b758-2110ac20d3a8.png)

![11](https://user-images.githubusercontent.com/64428916/210366605-bc20a76a-9f98-4df0-b894-ff8b32d5b769.png)

```bash
git checkout c6
git branch -f main HEAD
git branch -f bugFix HEAD~4
git checkout c1
```
