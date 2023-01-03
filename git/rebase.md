## 리베이스

- 커밋들을 모아서 복사한 뒤, 다른 곳에 떨궈 놓는다.
- 리베이스를 하면 커밋들의 흐름을 보기 좋게 한 줄로 만들 수 있다.

> 문제 1)

![1](https://user-images.githubusercontent.com/64428916/210365083-89d5da7f-cc8a-4478-be5d-c6152e1329b5.png)

![2](https://user-images.githubusercontent.com/64428916/210365081-c2b42ec9-7b57-42c4-9cc9-2133b6ee219f.png)

```bash
git branch bugFix
git checkout bugFix
git commit
git checkout main
git commit
git checkout bugFix
git rebase main
```

> 문제 2)

![8](https://user-images.githubusercontent.com/64428916/210368062-e36ee848-5997-4387-8e9c-34a125ef7e54.png)

![9](https://user-images.githubusercontent.com/64428916/210368070-c40df82c-966c-41a2-a83e-a47dab850d3d.png)

```bash
git rebase -i HEAD~2
git commit --amend
git rebase -i HEAD~2
git branch -f main HEAD
```

> 문제 3)

![12](https://user-images.githubusercontent.com/64428916/210368450-c1cd1ddc-ef6e-4f89-bf47-8ea7706fdfa9.png)

![13](https://user-images.githubusercontent.com/64428916/210368443-aba8491e-9510-4ed4-83df-99814675cc70.png)

```bash
git rebase main bugFix
git rebase bugFix side
git rebase side another
git rebase another main
```
