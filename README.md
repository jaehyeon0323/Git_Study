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
  
