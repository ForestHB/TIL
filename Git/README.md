## Git 명령어
  - git  
      - git branch  
        현재 작업중인 branch를 나타냄
      - git branch a  
        a라는 이름의 branch를 생성
      - git checkout a  
        a라는 이름의 branch로 이동
      - git log --branch  
        branch 작업 기록을 나타냄
        - --decorate  
          ref name을 출력
        - --graph  
          line 형태의 그래프를 같이 출력
          - --oneline  
            line을 최소한으로 출력
      - git merge a  
        a라는 이름의 branch를 현재 branch에 합침
      - git branch -d a  
        a라는 이름의 branch를 삭제
      - git fetch  
        The git fetch command downloads commits, files, and refs from a remote repository into your local repo.  
        Fetching is what you do when you want to see what everybody else has been working on.  
      - git pull  
        he git pull command is used to fetch and download content from a remote repository and immediately update the localrepository to match that content.   
        Merging remote upstream changes into your local repository is a common task in Git-based collaboration work flows.  
        The git pull command is actually a combination of two other commands, git fetch followed by git merge.
  - reset
      - git reset --hard HEAD
        가장 최신의 커밋 상태로 되돌림
  - stash  
    작업중에 다른 branch로 checkout할 경우, 다른 branch에 영향을 주게 되므로 이것을 숨기는 명령어.
    - git stash [save] : 삭제하지 않고 저장된 상태로 숨김
    - git stash apply : stash로 숨겨진 파일을 복원
    - git stash list : stash로 숨겨진 파일들의 리스트

## Concepts
- branch
  개발을 하다보면 하나의 소스 코드를 여러개의 버전으로 나누어 관리해야 하는 경우가 생기는데,
  이때 하나의 소스 코드를 통째로 복사하여 기존의 코드와 독립적으로 작업할 수 있는 것을 branch라고 한다.
  - remote branch  
    remote(원격) 저장소에 존재하는 branch를 말하는데,  
    remote branch또한 로컬에 존재하지만, 임의로 옮기거나 할 수 없고,  
    remote repository와 통신하면서 자동으로 업데이트된다.  

## Link  
  - [Learn Git with Bitbucket Cloud](https://www.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud)  
  - [Git Branch](https://git-scm.com/book/ko/v1/Git-%EB%B8%8C%EB%9E%9C%EC%B9%98-%EB%A6%AC%EB%AA%A8%ED%8A%B8-%EB%B8%8C%EB%9E%9C%EC%B9%98)
