---
title: "깃 사용법"
date: 2021-11-29 22:50:28 -0400
categories: Starting
---


Git

git 사용 이유 : 지금은 개인 코드 관리 위해, 이후 공동 개발을 위함

Local 영역에선 개인 코드 작성
Repository 영역에서 커밋을 통한 수정본 저장

저장소 생성 

git init

Or 

git clone (git Repository URL) (이미 레포지토리가 깃 허브에 있는 경우)



로컬 저장소에서 코드를 작성 한 후 git add 를 통해 staging 영역에 추가한다.
git add . 
(로컬 저장소의 수정 된 파일을 모두 스테이징 영역에 추가)

현재 add 한 내용 확인

git status 

commit

git commit -m "커밋 내용"


커밋 이후 푸시

git push

왜 안될까

vscode 의 기본 브랜치가 master 로 설정 되어 있어서 
깃 푸시를 메인 브랜치로 하려고 하면 오류가 나왔다.

그래서 브랜치를 master 에서 main 으로 바꿔주는 과정이 필요하다.

$ git branch -M [되고싶은 branch name]
$ git branch -m [현재 branch name] [바꾸고싶은 branch name]

브랜치 명을 master 에서 메인으로 바꾸고 푸시하면 된다

그런데 또 오류


힌트: 현재 브랜치의 끝이 리모트 브랜치보다 뒤에 있으므로 업데이트가
힌트: 거부되었습니다. 푸시하기 전에 ('git pull ...' 등 명령으로) 리모트

... 

git push origin main --force 로 강제로 푸시하여서 해겷하였다.
한 번 force 로 푸시하고 난 후 부터는 일반적인 푸시 명령어로 푸시가 가능했다.

