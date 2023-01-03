## 깃에서 변경한 내용을 되돌리는 방법

1.  git reset : 브랜치가 예전의 커밋을 가리키도록 이동시키는 방식으로 변경 내역을 되돌린다. (커밋하지 않은 것처럼 예전 커밋으로 브랜치를 옮기는 것)

    → 각자의 컴퓨터에서 작업하는 로컬 브랜치의 경우 reset을 잘 쓸 수 있지만, 다른 사람이 작업하는 리모트 브랜치에는 쓸 수 x

    ex) main 브랜치가 가리키던 커밋을 c1으로 다시 옮기기

    ![1](https://user-images.githubusercontent.com/64428916/210367002-7c8dc54f-6e38-4c59-b7ae-a074b7fad37b.png)

    ```bash
    git reset HEAD~1
    ```

2.  git revert : 변경분을 되돌리고 되돌린 내용을 **다른 사람들과 공유하기 위해서 git revert를 써야 한다.**

    ex) 로컬 브랜치와 remote 브랜치 다음과 같이 변경하기

    ![2](https://user-images.githubusercontent.com/64428916/210367006-51c4723b-c1a5-48ac-91d1-2f997847fb32.png)

    ![3](https://user-images.githubusercontent.com/64428916/210367011-d3786310-8dd0-41e1-9f41-1a347c42570c.png)

    ```bash
    git reset HEAD^
    git switch pushed
    git revert c2
    ```
