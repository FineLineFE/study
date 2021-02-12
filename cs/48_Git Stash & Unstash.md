## Git Stash
![](https://images.velog.io/images/finelinefe/post/cf7d8002-0852-4565-9068-fb3ab39afcfa/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-02-12%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%205.08.20.png)
>  Stash : 1. (안전한 곳에) 넣어 두다[숨기다] 2. 챙겨 둔[숨겨 둔] 양

일반적으로 git 에서 stash는 단어 뜻 그대로 작업 중 작업 내역을 스테이지엔 올리지 않았지만 현재 어떠한 상황으로 인해 워킹 디렉토리를 HEAD로 향하게 해야하는 불가피한 상황속에서 일종의 '북마크' 또는 '책갈피' 역할을 하는 기능이다.



<br />

## Git Unstash
![](https://images.velog.io/images/finelinefe/post/cfcd48a3-ffca-415c-a573-d16c7a4e12ba/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-02-12%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%205.59.25.png)
> Stash의 반대 작업. 하던 작업을 다시 불러온다.

- Git Stash list = Stash한 목록 확인
- Git Stash apply = Stash한 작업물을 불러온다. POP과 다르게 stash list에서 사라지지 않는다.
- 적용 후 git 추가, 커밋메시지 작성. push하면 완료

<br />


## 사용 예 2

![](https://images.velog.io/images/finelinefe/post/4c6dd3c2-5bad-40ff-a525-803a1827b4f2/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-02-12%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%206.44.40.png)

- dev 브랜치에서 특정 피쳐브랜치로 체크아웃 후 사전에 Stash한 작업 목록을 apply
- feature 브랜치 -> dev 브랜치로 merge
- git add -> commit 메시지 작성 후 push

<br />
