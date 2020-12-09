### 리베이스란?
기존의 커밋 풀 방식에서 생성되는 여러개의 커밋메시지는 자칫 복잡하고 혼란스러움을 줄 수 있다. 다수의 작업자들이 함께하는 프로젝트의 경우에는 더 그렇다. 다수 브랜치가 양산하는 커밋 히스토리를 정리하고자 할 때 리베이스를 진행한다.
```
1) git add .
2) git commit -m "커밋 메시지 입력"
3) git rebase -i main
4) 리베이스 후 conflict 있으면 수정 진행 / 없으면 다음단계 진행
5) git add .
6) git rebase --continue
7) git push origin feature/브랜치이름 --force
```
<br />

### 스쿼시란?
리베이스를 하면서 여러개의 커밋 메시지를 하나로 통합하는데 이것을 git squash라고 한다.<br />
```
pick 커밋메시지 ex1 Task 1
pick 커밋메시지 ex1 Task 2
pick 커밋메시지 ex1 Task 3

Rebase nnnn..nnnn onto nnnnn
Commands:
p, pick = use commit
r, reword = use commit, but edit the commit message
e, edit = use commit, but stop for amending
s, squash = use commit, but meld into previous commit
f, fixup = like "squash", but discard this commit's log message
x, exec = run command (the rest of the line) using shell

These lines can be re-ordered; they are executed from top to bottom.

If you remove a line here THAT COMMIT WILL BE LOST.

However, if you remove everything, the rebase will be aborted.

Note that empty commits are commented out

```
<br />

커밋 히스토리의 상단 메시지 하나만 pick 상태로 두고 나머지는 squash 또는 s 로 변경한다. 이것을 스쿼시라고 한다.

<br />

```
pick 22222 Task 1 <br />
s 11111 Task 2 <br />
s 33333 Task 3 <br />
```
<br />
그 후 push를 할 때에는 force(-f) 옵션을 추가하여 push를 해야한다. 이유는 이렇게 할 경우 다른 브랜치라고 생각하기 때문에 일반 push가 적용되지 않기 때문이다.
