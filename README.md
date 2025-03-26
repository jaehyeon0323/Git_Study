# Git_Study
Git repository 내용 공부용

git commit:
  git 저장소에 디렉토리에 있는 모든 파일에 대한 스냅샷을 기록(디렉토리 전체를 복사, 붙여넣기 하는 것과 유사)

git branch:
  특정 commit을 참조, 메모리나 디스크 공간에 부담이 거의 없음, 하나의 commit과 그 부모 commit을 포함하는 작업 내
  *checkout: git branch [이동할곳] _ git branch를 이동하는 명령어

git Merge:
  git branch를 합치는 명령어

git Rebase:
  commit을 모아서 다른 곳에 떨구는 것, 로그이력 간결화

HEAD
  현재 checkout된 commit을 가르킴(작업중인 commit, 항상 가장 최근 commit):라벨

상대 참조(Relative Ref)
  ^(캐럿): 작업 중인 commit의 부모로 HEAD가 한단 checkout됨 ex.git checkout main^ / git checkout C4^
  ~(틸드): 작업 중인 commit의 부모로 HEAD가 여러단계 checkout됨 ex.git checkout main~4 / git checkout C4~4
  *branch 강제 이 하기: -f ex.git branch -f main HEAD~3

작업내용 되돌리기(git reset, git revert)
  git reset: 예전 commit을 가리키도록 이동(히스토리를 고쳐쓴다, 애초에 commit하지 않은 것 처럼 예전 commit으로 branch를 옮기는 것)
  git revert: 변경분을 공유하기 위한 방식(수정된 commit이 생성됨)
  
git cherry-pick
  사용법: git cherry-pick <Commit1> <Commit2> <...>
  현재 위치(HEAD) 아래에 있는 일련의 commit들에 대한 복사본을 만듦

Interactive Rebase
  rebase명령어를 사용 할 대 -i 옵션을 같이 사용 하는 것
  대화창에서 할 수 있는 것
    1)적용할 commit들의 순서를 UI를 통해 바꿀 수 있다
    2)원하지 않는 commit들을 뺄 수 있다. pick을 이용해 지정할 수 있다.
    3)commit을 스쿼시(squash)할 수 있다. 합칠 수 있다

git 기능들
  git rebase -i
  git cherry-pick
  git commit --amend: 커밋 내용 정정

Git tag
  사용법: git tag v1 C1
  특정 commit들을 branch로 참조하듯 영구적인 mailestone(이정표)으로 표시

Git describe
  사용법: git describe <ref>
  commit 히스토리에서 앞 뒤로 여러 commit을 이동하고 나서 commit 트리에서 방향 감각을 다시 찾는데 도움
  <tag>_<numCommits>_g<hash>

# Git Remote(원격)
  git clone:
    원격 저장소에 있는 내용을 로컬에 복사, 생성 할 때 사용하는 명령어

  git fetch:
    1)원격 저장소에는 있지만 로컬에니느 없는 커밋들을 다운
    2)우리의 원격 브랜치가 가리키는 곳을 업데이트
    로컬을 변경하진 않

  git pull
    

