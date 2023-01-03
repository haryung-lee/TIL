## Git 체리-픽 (Cherry-pick)

- 현재 위치(HEAD) 아래에 있는 일련의 커밋들에 대한 복사본을 만든다.
- `git cherry-pick <Commit1> <Commit2> <…>`

> 문제 1)

![4](https://user-images.githubusercontent.com/64428916/210367337-314e8e0a-1d3b-45e9-9c3c-806d31f8777e.png)

![5](https://user-images.githubusercontent.com/64428916/210367346-a7525d0a-687f-43ce-a244-ea502670ea84.png)

```bash
git cherry-pick c3 c4 c7
```

> 문제 2)

![10](https://user-images.githubusercontent.com/64428916/210368255-d2710101-5c5b-4d8a-9d07-0b7e8abeda80.png)

![11](https://user-images.githubusercontent.com/64428916/210368249-4fb0e11e-46b1-41fe-9a75-5fa0b7b25fc0.png)

```bash
git checkout main
git cherry-pick c2
git checkout c1
git cherry-pick c2 c3
git branch -f main HEAD
```
