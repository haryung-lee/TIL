## 인터렉티브 리베이스

- 리베이스할 일련의 커밋들을 검토할 수 있는 방법
- rebase 명령어 + -i 옵션

> 문제 1)

![6](https://user-images.githubusercontent.com/64428916/210367642-6dc66355-e41a-47d3-be51-a4306b3fc537.png)

![7](https://user-images.githubusercontent.com/64428916/210367647-535ee93b-37b3-4929-a1ce-1613c786af6f.png)

```bash
git rebase -i
이후 pick 이용해 커밋 순서 재정렬 & 불필요한 커밋 삭제
```
