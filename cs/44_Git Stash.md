## Git Stash

> 현재 작업중인 브랜치에서 다른 브랜치로 이동할 경우 임시로 올려놓고 브랜치를 바꿀 수 있다. 일반적으로 git add나 commit 메세지를 남긴 후에 다른 branchf로 checkout이 가능한데 **git stash**는 이러한 점을 해결한다.

1) git stash save 브랜치이름
2) git stash list <- 해당 브랜치의 n 확인
3) git stash apply stash@{n} <- 해당 이력 저장

<br />
