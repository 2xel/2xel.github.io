---
layout: post
title: github에 push된 commit 삭제
category: git
tags: git
comments: true
---

# git reset HEAD^
이 명령어는 커밋을 되돌리는 명령어
여기서 그냥 push를 해버리면
```
$ git push origin master
To https://github.com/2xel/2xel.github.io.git

! [rejected] master -> master (non-fast-forward)
error: failed to push some refs to 'https://github.com/2xel/2xel.github.io.git'
To prevent you from losing history, non-fast-forward updates were rejected
Merge the remote changes (e.g. ‘git pull’) before pushing again. See the
‘Note about fast-forwards’ section of ‘git push –help’ for details.
```
다음과 같은 메시지가 떨어진다.  
원격 저장소에 있는 정보가 손실 될 수 있는 작업이라서 리젝트 시킨다.  
우리는 이러한 데이터를 손실시키고 싶다.  
이럴때 사용할 수 있는게 + 다.  
git push origin +master
이렇게 + 를 붙여주면 강제로 덮어 써 준다
