# Git


## 용어



## CLI

### - 브렌치

\* 참고자료 [https://lelecoder.com/52](https://lelecoder.com/52), [https://backlog.com/git-tutorial/kr/stepup/stepup2_3.html](https://backlog.com/git-tutorial/kr/stepup/stepup2_3.html)

```
#1. 현재 작업 브렌치 확인하기
git branch

#2. 새로운 브렌치 생성하기
git branch 브렌치_이름 //새로운 브렌치 생성
git checkout 브렌치_이름 //브렌치 이동

git checkout -b 브렌치_이름 //새로운 브렌치 생성하고, 이동하기

#3. 브렌치 삭제하기
git branch -d 브렌치_이름 //브렌치 삭제하기
```


### - staged 된 파일들만 stash 하기 (Double stash)

\* 참고자료 [https://stackoverflow.com/questions/14759748/stashing-only-staged-changes-in-git-is-it-possible](https://stackoverflow.com/questions/14759748/stashing-only-staged-changes-in-git-is-it-possible)

```
#1. stash 할 피일들을 모두 Stage 상태로 이동

#2. git stash --keep-index 명령어 사용
   (해당 명령어는 staged, unstaged된 모든 변화들을 포함한 stash를 생성사지만,
   워킹 디렉토리에 staged된 변화들을 남겨둠)

#3. git stash push -m "원하는_stash_이름"

#4. 그럼 stash "원하는_stash_이름"은 staged 된 파일들만 가지고 있다
```

\* 만약 stash 하기 전의 unstaged 파일들이 필요하다면, stash(--keep-index 옵션으로 생성된 stash)를 적용하면, "원하는_stash_이름"에 stash된 파일들을 제거할 수 있음
<br>
<br>
<br>

### - 이미 push 한 커밋 메시지 수정하기
