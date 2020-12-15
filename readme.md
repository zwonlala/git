# Git

## 참고하면 좋을 사이트

- 누구나 쉽게 이해할 수 있는 Git 입문 [https://backlog.com/git-tutorial/kr/contents/](https://backlog.com/git-tutorial/kr/contents/)

## 용어

### HEAD
'현재 사용 중인 브랜체의 선두 부분'
HEAD를 이동하면, 사용하는 브렌치가 변경됨

틸드(~)나 캐럿(^) 기호를 사용하여 현재 커밋으로부터 특정 커밋의 위치를 가리킬 수 있음
- HEAD ~i : HEAD 보다 i 세대 앞 커밋
- HEAD ^i : 브렌치 병합에서 원본이 여럿 있는 경우 몇 번째 원본인지 지정


![ ~와 ^](https://user-images.githubusercontent.com/13375734/102227299-bdc75400-3f2c-11eb-89a6-79289c09f163.png)

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
