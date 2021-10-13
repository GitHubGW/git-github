## Git & Gitbub

#### Git

- 깃은 Distributed Version Controll System으로 파일들을 트래킹하는 방식이다.
- 깃은 모든 파일들의 변경사항들을 추적하기 때문에 사용자가 어떤 파일들을 트래킹 하고 싶을 때 사용할 수 있다.
- 언제, 누가, 어떤 것이 바꼈는지 등을 상세하게 추적할 수 있다.
- 깃은 파일들을 단순히 텍스트로 읽지 않고, 바이너리 코드인 0과 1로 읽는다.
- 그렇기 때문에 텍스트 파일뿐만 아니라 이미지, 엑셀, 음악 파일등 대부분의 파일들을 읽을 수 있다.

#### Github

- 깃허브는 우리가 작업한 깃 파일(git 변경사항)들을 올리는 곳이다.
- 우리가 작업한 히스토리 파일들을 업로드하고 공유하기 위한 곳이다.
- 깃허브는 여러 Cloud Git Provider중 하나로, GitLab이나 Bitbucket등이 있다.

#### Repository

- 리포지토리는 기본적으로 사용자의 파일들이 위치한 곳이고 깃이 주시하고 있는 폴더이다.
- 그래서 그 파일 안에 있는 모든 것은 git에 의해 주시된다.
- 리포지토리는 기본적으로 .git이라는 폴더를 가지게 되고, 이 폴더에는 깃에 관련된 명령어나 파일, 히스토리들이 있다.
- 이 파일이 있기 때문에 깃이 해당 리포지토리를 추적할 수 있게 되는 것이다.

#### Commit

- 커밋은 기본적으로 작업에 대한 기록이다. 
- 작업중인 깃 폴더에 어떤 변경사항이 있을 때 그것을 기록하고 싶을 때 사용한다.

#### Area

- 깃 area는 기본적으로 working directory, staging area, git directory(local repository) 3단계로 나눠져 있다.
- 첫 번째 working directory는 현재 우리가 작업하고 있는 폴더에서 어떤 변경사항이 생기면 알아차리는 곳이다.
- working directory에서 git add를 하게 되면 staging area로 가게 된다.
- 두 번째 staging area는 변경사항이 있는 파일들을 선택해 커밋할 수 있도록 지정하는 곳이다.
- staging area에서 git commit을 하게 되면 git directory(repository)로 가게 된다.
- 세 번째 git directory(local repository)는 파일들이 커밋되어진 곳으로, 파일들의 수정사항에 대한 스냅샷을 가지고 있는 곳이다.
- git directory(local repository)에는 언제, 누가, 어떤 것을 수정했는지에 대한 히스토리를 가지고 있는 곳이다.
- git direcotry에서 git push를 하게 되면 remote repository로 올라가게 된다.
- git pull을 하게 되면 remote repository에서 local repository로 받아오게 된다.