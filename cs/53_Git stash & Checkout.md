## Git Stash & Git Checkout

> 새 브런치로 만들어서 갈아타야할 때, 이러한 현상이 있다면 = Git Stash 사용하기

<br />

![](https://images.velog.io/images/finelinefe/post/21ea4efe-c110-4a8d-aba9-72b9509cf2f9/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-02-19%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%201.43.42.png)

기존에 현재 브랜치인 test/question 브랜치에서 dev 브랜치를 pull 받아야 할 상황이 생겼다.

checkout 명령어를 사용했지만 기존 작업에서 변경된 부분이 있어 선 커밋을 하고 바꿀 수 있는 상태. 이때 임시로 stash 기능을 사용하면 된다.

그 이후 dev로 checkout 하면 전환이 되고 이때 pull 받으면 된다.

- git stash
- git checkout dev
- git pull origin dev

<br />
