---
layout: single
title: "git 예제 연습하기"
date: 2021-03-12 12:37:25 +0900
---

# 깃의 명령어 

1. 기본 설정

git config 옵션

**옵션**
user.name 사용자이름 : 사용자 이름 설정
user.email 사용자 이메일 : 사용자 메일 주소 설정
--global : 전역 설정
-- list : 설정 목록 확인



1. 현재 디렉토리를 새로운 git 저장소로 설정 

git init


2. 저장소 복사하기(동시에 origin 저장소를 생성)

git clone git_path(URL)


3. 새로운 원격 저장소 추가하기

gir remote add 원격저장소 저장소URL


4. 변경사항이 있는 파일을 스테이징 하고 커밋하기

git add .

**옵션**
-A, --all: 변경된 모든 파일 추가


git commit -m "message"

**옵션**
-m "message": 커밋 메세지와 함께 커밋
-a: 자동으로 add를 진행한 후 커밋
-v: 커밋 메세지에 diff의 내용 포함


5. 브랜치 목록 보기

git branch #local 브랜치 목록 보기

git branch -r #원격 브랜치 목록 보기

git branch -a #모든 브랜치 목록 보기(로컬+원격)


6. 브랜치 생성하기

git branch [new branch_name]

git branch [new branch_name]<위치> #특정 위치에 브랜치 생성하기


**옵션**
-v : 각 브랜치의 마지막 커밋 메세지를 보여줌
-merged : merge된 브랜치 목록 확인
-no-merged : merge하지 않은 브랜치 목록 확인
-d : 브랜치 삭제하기
-D : 브랜치 강제 삭제


7. 병합하기

git merge <branch_name>

git merge - -no-commit <branch_name> #커밋하지 않고 합치기

git cherry-pick <commit_name> #선택하여 합치기

git cherry-pick -n <commit_name> #커밋하지 않고 선택하여 합치기

git branch -d <branch_name> #브랜치 삭제하기


8. 이력

git log #모든 이력 보기

**옵션** 
-p : 변경사항 확인
--oneline: 커밋 메세지만 한 줄씩 표시
--all : 모든 브랜치 로그 표시
--graph : 브랜치 트리 그래프 표시


git log - -since="기간" #특정 기간 동안의 커밋 이력 보기

git log - -before="시점" #특정 시점까지의 커밋 이력 보기


9. 차이점 보기

git diff #현재 작업 트리와 인덱스간의 차이점

**옵션** 

-A, --all: 변경된 모든 파일 추가 


10. 변경 사항 가져오기

git fetch #origin 저장소에서 합치지 않고 지역 브랜치로 변경사항 가져오기

git fetch <원격저장소> #원격저장소에서 합치지 않고 지역 브랜치로 변경 사항 가져오기


11. 합치기

git pull #origin저장소에서 변경 사항을 가져와 현재 브랜치에 합치기




12. 저장소에 업데이트하기

git push 


13. 제거하기

git remote rm <원격 저장소URL>

**옵션**
--cached : 파일의 staging area에서 제외
-f, --force : 삭제하려는 파일의 내용이 브랜치 끝 부분에서의 내용과 다를 경우 강제 삭제
--ignore-unmatch : 삭제하려는 파일이 없을 때 발생하는 에러 무시


git clean #working directory의 필요 없는 파일 삭제


14. 상태 확인하기

git status


15. 바로 전 커밋으로 돌아가기

git reset #직전의 add이전 상태로 staging area 되돌림

