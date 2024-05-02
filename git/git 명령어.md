### git repository 복제
  1.
    1) git init 
    2) git add ReadMe.txt
    3) git commit
    4) git remote add '원격 저장소명' '원격 저장소 주소'
  2.
    1) git clone '원격 저장소 주소' 

### git commit, push, status
  * staging
    + git add 파일명 (한 개의 파일을 staging 한다.)
    + git add . (파일 전체를 staging 한다.)
    + git status (staging 파일을 확인한다.)
  * commit 
    + git commit -m '커밋내용' (staging 된 파일을 commit 한다.)
    + git log --online --all --graph (commit 내역을 조회한다.)
  * push 
    + git push '원격 저장소명' '브랜치명'
  * status
    + git status (git 상태를 조회한다.)

  ### git branch, remote
  * branch 생성
    + git branch '브랜치명'
  * branch 이동
    + git switch '브랜치명'
  * branch 합치기
    1) git switch '기준 브랜치' (합쳐질 브랜치로 이동한다.)
    2) git merge '합칠 브랜치' (같은 파일을 수정할 경우 conflict)
  * 원격 저장소 확인
    + git remote 
  * 원격 저장소와 연결된 프로젝트 정보 확인
    + git remote -v
  * 원격 저장소 연결 
    + git remote add '원격 저장소명' '원격 저장소 주소'
  * 원격 저장소 삭제
    + git remote remove '원격 저장소명'
