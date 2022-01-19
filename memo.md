# Git & GitHub

## Git

- 깃은 Distributed Version Controll System으로 파일들을 추적하는 방식이다.
- 깃은 모든 파일들의 변경사항들을 추적하기 때문에 사용자가 어떤 파일들을 추적하고 싶을 때 사용할 수 있다.
- 언제, 누가, 어떤 것이 바꼈는지 등을 상세하게 추적할 수 있다.
- 깃은 파일들을 단순히 텍스트로 읽지 않고, 바이너리 코드인 0과 1로 읽는다.
- 그렇기 때문에 텍스트 파일뿐만 아니라 이미지, 엑셀, 음악 파일등 대부분의 파일들을 읽을 수 있다.

## Github

- 깃허브는 우리가 작업한 깃 파일(git 변경사항)들을 올리는 곳이다.
- 우리가 작업한 히스토리 파일들을 업로드하고 공유하기 위한 곳이다.
- 깃허브는 여러 Cloud Git Provider중 하나로, GitLab이나 Bitbucket등이 있다.

## Repository

- 리포지토리는 기본적으로 사용자의 파일들이 위치한 곳이고 깃이 주시하고 있는 폴더이다.
- 그래서 해당 폴더 안에 있는 모든 파일들은 git에 의해 주시된다.
- 리포지토리는 기본적으로 .git이라는 폴더를 가지게 되고, 이 폴더에는 깃에 관련된 명령어나 파일, 히스토리들이 있다.
- 이 .git폴더가 작업 중인 폴더 내부에 있기 때문에 깃 명령어를 사용할 수 있고, 깃이 해당 폴더의 변경사항들을 추적할 수 있는 것이다.

## Commit

- 커밋은 기본적으로 작업에 대한 기록이다.
- 작업중인 폴더에 어떤 변경사항이 있을 때 그것을 히스토리로 기록하고 싶을 때 사용한다.

## Area

- 깃 area는 기본적으로 working directory(unstage area), staging area, git directory(local repository) 3단계로 나눠져 있다.
- 첫 번째 working directory는 현재 우리가 작업하고 있는 폴더에서 어떤 변경사항이 생기면 알아차리는 곳이다.
- working directory에서 git add를 하게 되면 staging area로 가게 된다.
- 두 번째 staging area는 변경사항이 있는 파일들을 선택해 커밋할 수 있도록 지정하는 곳이다.
- staging area에서 git commit을 하게 되면 git directory로 가게 된다.
- 세 번째 git directory는 파일들이 커밋된 곳으로, 파일들의 변경사항에 대한 스냅샷을 가지고 있는 곳이다.
- git directory에는 언제, 누가, 어떤 것을 수정했는지에 대한 히스토리를 가지고 있는 곳이다.
- git direcotry에서 git push를 하게 되면 remote repository인 원격 저장소로 올라가게 된다.
- git pull을 하게 되면 remote repository인 원격 저장소에서 local repository인 로컬 저장소로 받아오게 된다.
- ![](https://www.gyanblog.com/static/5a95f868558c38cd23ec6168393674b8/0a47e/git_lifecycle_2.png)

## Branch

- 브랜치는 현재 main브랜치의 마지막 커밋으로부터 다른 타임라인을 가지게 될 부분이다.
- 브랜치를 생성하게 되면 해당 브랜치는 메인 브랜치의 마지막 커밋까지의 내용을 가지고 있게 된다.
- 그래서 그 후 새로운 변경사항이 생기게 되면 그 변경사항을 메인 브랜치에 merge를 통해 합칠 수 있게 된다.
- 또는 메인 브랜치에 변경사항이 생기면 Update를 통해 메인 브랜치의 변경사항을 가져와서 업데이트할 수 있다.
- 그리고 기능 개발이 끝났다면 나중에 해당 브랜치를 메인 브랜치에 merge하고, 삭제할 수 있다.
- ![](https://www.nobledesktop.com/image/gitresources/git-branches-merge.png)

## Conflit

- Conflit는 각각의 브랜치에서 작업한 코드가 동일한 라인에서 변경사항이 발생했을 때 생기는 충돌 문제이다.
- 예를들어 메인 브랜치와 또 다른 브랜치에서 같은 라인에서 코드를 수정한 후, merge하려고 할 때 충돌이 생기게 된다.
- 충돌이 생기면 해당 두 브랜치를 비교해 어떤 브랜치의 변경사항을 적용할 것인지 선택해서 merge할 수 있다.

## Fork

- Fork는 git의 기능이 아닌 github의 기능으로, 해당 리포지토리의 전체를 자신의 계정에 복사해서 가져온다.
- 포크를 활용하는 방법은 보통 팀으로 작업할 때 메인 프로젝트 리포지토리가 있다면, 그 메인 프로젝트를 자신의 리포지토리로 포크해와서 작업한 후, 작업이 끝나면 메인 프로젝트 리포지토리에 작업한 변경사항들을 pull request(pull해서 가져가라고 요청)하게 된다.
- 그렇게 되면 메인 프로젝트 리포지토리에는 다른 사용자가 Open a pull request한 것을 확인할 수 있고, 해당 코드를 현재 프로젝트에 병합하거나 취소할지 결정할 수 있다.
- 작업이 끝나면 pull request를 하고 난 후에는 포크한 리포지토리를 삭제할 수 있다.
- 정리하자면 해당 메인 리포지토리를 포크해서 리포지토리 복사본을 가져온 후, 작업을 하고 그 변경사항을 pull request요청한다.

## Upstream Branch

- Upstream Branch는 fork해온 베이스 저장소의 마스터 브랜치와 연결되어 있는 브랜치이다.
- 우리가 메인 리포지토리에서 포크를 해온 후 작업을 할 때, 만약 메인 리포지토리의 코드가 업데이트 되어서 포크해서 작업중인 코드가 오래된 경우, upstream 브랜치를 통해 메인 리포지토리의 최신 코드를 현재 리포지토리로 fetch해올 수 있다.
- 메인 리포지토리의 메인 브랜치를 fork하게 되면 기본적으로 그 메인 리포지토리의 메인 브랜치와 연결되어있는 upstream 브랜치가 만들어지고, 이 브랜치를 통해 메인 리포지토리의 변경사항을 fetch해서 가져올 수 있다.
- Github Desktop에서 fetch origin을 클릭해서 upstream 브랜치에 최신 코드를 fetch해서 가져온 후, upstream 브랜치의 코드를 현재 브랜치에 병합한다.

## 오픈 소스 프로젝트에서 협업하는 방법

- 오픈 소스 프로젝트나 팀에서 협업하는 전체적인 과정에 대해 정리했다.
- 1. 깃허브 리포지토리에서 fork해온다.
- 2. 리포지토리를 local에 clone해온다.
  - `git clone https://github.com/user/repo.git`
- 3. 베이스 저장소를 가르키는 upstream이라는 remote를 추가한다.
  - `git remote add upstream https://github.com/user/repo.git`
- 4. 새로운 new_feature라는 브랜치를 생성 후, 해당 브랜치로 이동한다.
  - `git checkout -b new_feature`
- 5. new_feature브랜치에서 기능 개발을 한다.
- 6. remote(베이스 저장소)로부터 새로운 변경사항을 pull해온다.
  - `git checkout master`를 통해 master브랜치로 이동한다.
  - `git pull upstream master`를 통해 upstream의 master브랜치로부터 변경사항을 pull해온다.
  - `git checkout new_feature`를 통해 기능 개발중인 new_feature브랜치로 이동한다.
  - `git merge master`를 통해 master브랜치로부터 merge한다.
  - `git push origin new_feature`를 통해 원격 저장소에 변경 사항을 푸시한다.
- 7. pull request를 통해 변경 사항을 upstream 리포지토리(베이스 저장소)에 병합한다.
- 8. pull request가 수락되면, 변경 사항을 origin(포크된 리포지토리)으로 가져온다.
  - `git checkout master`를 통해 master브랜치로 이동한다.
  - `git pull upstream master`를 통해 upstream의 master브랜치로부터 변경사항을 pull해온다.
- 9. 로컬과 깃허브에 존재하는 new_feature브랜치를 삭제한다.
  - `git branch -d new_feature`를 통해 로컬에서 new_feature브랜치 삭제
  - `git push origin --delete new_feature`를 통해 로컬에서 new_feature브랜치를 삭제한 내용을 푸시한다.
- https://www.tomasbeuzen.com/post/git-fork-branch-pull
- ![](https://www.tomasbeuzen.com/post/git-fork-branch-pull/featured_hud478d74d48d19bfd1c1c03fc398c8033_312322_720x0_resize_lanczos_3.png)

## Issue

- 이슈는 Git의 기능이 아닌 GitHub, GitLab, Bitbucket등에서 사용하는 기능으로 문제점들을 다루고 관리하기 위한 프로젝트 관리 시스템이다.
- 프로젝트 중 아직 하지 않은 부분이나 또는 발견한 문제나 버그같은 것을 이슈를 생성해 기록하는 곳이다.
- 주로 해당 프로젝트를 오픈 소스의 환경에서 작업할 때, 여러 테스터들이 문제를 찾아서 이슈를 적게 된다.
- 혼자서 일하거나 작은 회사에서 일할 때, 매번 문제점이나 버그를 발견할 때마다 새로운 이슈를 생성한다.
- 그리고 Pull request를 만들 때, 해당 이슈를 해결하기 위함이라고 기록하면 된다.
- 보통 큰 회사에는 큰 저장소가 있고 많은 테스터들, 소프트웨어 관리자들, 기술 리더들이 이슈를 만드는데 이슈들 중 일부가 Pull request를 통해 해결된다.

## Milestone

- Milestone은 버전을 올릴 때 필요한 것들을 따로 리스트로 모아두는 것으로, 프로젝트에서 해결하거나 달성해야 할 이슈들을 모아서 그 프로젝트의 진척을 보기 위해 사용되는 기능이다.
- 프로젝트의 최종 목표점이나 완성을 의미하는 것은 아니고, 프로젝트가 진행되는 동안 달성되어야 하는 특정한 목표라고 이해하면 될 것 같다.
- 마일스톤은 프로젝트의 기간에 영향을 주지는 않지만, 꼭 달성해야만 하는 주요한 목표가 성공에 도달하도록 초점을 맞춘다.
- 예를 들면 새롭게 추가될 특정 기능이나 새로운 버전업 등이 마일스톤이 될 수 있다.
- 마감일을 설정 후, 해당 기간 동안 수행할 이슈들을 등록해 놓으면 해결된 이슈와 미해결된된 이슈를 구분해서 볼 수 있고, 해결된 이슈들을 카운트하여 프로젝트의 진행사항을 퍼센트로 보여주는 기능이다.
- 마일스톤 안에 있는 모든 이슈들이 해결되면 마일스톤이 달성되게 된다.

## Checkout

- git checkout 커밋ID: checkout을 사용하면 과거의 커밋으로 돌아갈 수 있다.
- 과거의 커밋으로 돌아가게 되면 HEAD가 과거의 커밋 위치로 바뀌게 된다.
- HEAD는 현재 작업중인 브랜치를 가르킨다.
- git checkout main: 과거로 돌아간 상태에서 checkout을 통해 다시 현재 main 브랜치로 돌아올 수 있다.

## Hard Reset

- Hard Reset은 커밋 기록과 작업한 파일의 변경 사항 모두를 삭제하면서 과거의 커밋으로 돌아간다.
- git reset HEAD^ --hard: 이전 커밋으로 돌아가는 동시에 커밋과 파일의 변경사항 모두 삭제한다. (--hard는 삭제하는 명령어이다.)
- HEAD뒤에 ^을 붙이면 이전 커밋으로 돌아가고, ^^을 붙이면 더 이전 커밋으로 돌아간다.

## Mixed Reset

- Mixed Reset은 커밋 기록만 삭제하고, 작업한 파일의 변경 사항은 그대로 유지하면서, 과거의 커밋으로 돌아간다.
- git reset HEAD^: 이전 커밋으로 돌아가지만 커밋을 삭제하지 않고, 파일을 untracked(깃에 의해 추적되지 않은 상태)로 이동시킨다.
- untracked는 git add를 하기 전의 상태인 working directory를 의미한다.
- 즉, 커밋은 되돌아가지만 hard reset가 다르게 파일을 삭제하지는 않는다.
- hard reset은 이전 커밋으로 돌아가고 파일 또한 삭제해버린다.
- 그래서 아직 완료되지 않은 파일을 커밋한 경우, Mixed Reset을 사용해서 파일의 변경 사항은 그대로 유지한 채, 커밋만 되돌려서 파일을 수정한 후 다시 커밋할 수 있다.

## Soft Reset

- Soft Reset은 Mixed Reset과는 다르게 이전 커밋으로 돌아가지만, 변경한 파일을 unstage area(working directory)가 아닌 staging area에 추가시킨다.
- git reset HEAD^ —soft: 이전 커밋으로 돌아가지만 커밋을 삭제하지 않고, 파일을 staging area(깃에 의해 추적되고 있는 상태)로 이동시킨다.
- staging area로 이동시키기 때문에 현재 작업 중인 파일과 구분할 수 있다.
- 대부분의 경우에는 Hard Reset으로 되돌려서 아예 처음부터 다시 시작하거나 Mixed Reset으로 되돌린 후 작업하는 경우가 많다. ## Branch 생성
- git checkout -b 브랜치명 또는 git switch -c 브랜치명을 실행해 Reset을 통해 이전 커밋으로 되돌아간 후 브랜치를 생성할 수 있다.
- git reset HEAD^ —soft: 이전 커밋으로 돌아가지만 커밋을 삭제하지 않고, 파일을 staging area(깃에 의해 추적되고 있는 상태)로 이동시킨다.
- staging area로 이동시키기 때문에 현재 작업 중인 파일과 구분할 수 있다.
- 대부분의 경우에는 Hard Reset으로 되돌려서 아예 처음부터 다시 시작하거나 Mixed Reset으로 되돌린 후 작업하는 경우가 많다.
- git checkout 브랜치명: 현재 브랜치에서 해당 브랜치로 이동할 수 있다.
- git push origin 브랜치명: main브랜치 외에도 새로 생성한 브랜치 또한 푸시할 수 있다.
- 푸시하게 되면 기본 main브랜치 외에 여러 브랜치들로 나누어서 생성하게 된다.

## Branch 삭제

- 브랜치 생성 후, 브랜치에서 개발이 다 끝나고 메인 브랜치에 병합 후에 더 이상 브랜치를 사용하지 않을 때는 삭제해주는 것이 좋다.
- 브랜치는 자주 만들어서 작업하는 것이 좋지만, 메인 브랜치를 제외한 서브 브랜치들은 저장소에 남아 있지 않는 것이 좋다.
- 그래서 작업이 다 끝나고 메인 브랜치에 병합을 완료했다면, git branch -d 브랜치명을 통해 로컬저장소에서 브랜치 삭제해준다.
- 그리고 로컬 저장소 뿐만 아니라 원격 저장소에도 git push origin :브랜치명을 통해 삭제해준다.
- git push origin :브랜치명대신 git push origin -d 브랜치명을 통해 삭제할 수도 있다.

## Commit 수정

- Commit Amend는 가장 마지막 커밋을 수정할 때 사용할 수 있다.
- 만약 마지막 커밋에 빠뜨리거나 추가하지 않은 변경사항이 있다면 git add후, git commit —amend -m “커밋 메시지”를 통해 마지막 커밋의 커밋 메시지를 수정하고, 현재 변경사항들을 마지막 커밋에 추가한다.
- git commit —-amend —-no-edit은 마지막 커밋의 메시지를 수정하지 않고, 현재 변경사항들을 마지막 커밋에 추가한다.
- 작업이 다 끝나고 메인 브랜치에 병합을 완료했다면, git branch -d 브랜치명을 통해 로컬저장소에서 브랜치 삭제할 수 있다.
- 그리고 로컬 저장소 뿐만 아니라 원격 저장소에도 git push origin :브랜치명 또는 git push origin 브랜치명 -D를 통해 삭제할 수 있다.

## Commit 내리기

- git rm 폴더명 -r --cached를 통해 이미 staging area에 올린 폴더를 다시 unstage area로 내릴 수 있다.
- 폴더를 내리고 싶을 땐 -r을 붙여주면 되고, 이미 staging area에 올라갔다면 뒤에 --cached를 붙여줘야 한다.
- git restore --staged와 비슷하다.

## Origin, Remote

- Origin은 원격 저장소를 의미하는 것으로 GitHub, GitLab, Bitbucket 저장소를 의미한다.
- GitHub에서는 리포지토리를 만들면 기본적으로 origin으로 설정된다.
- 원격 저장소를 더 추가하고 싶다면 git remote add 원격저장소명 원격저장소URL을 통해 추가적으로 원격 저장소를 연결할 수 있다.
- 반대로 git remote remove 원격저장소명 원격저장소URL을 통해 현재 연결되어 있는 원격 저장소의 연결을 해제할 수 있다.
- git remote add를 통해 github뿐만 아니라 gitlab, bitbucket등에도 원격 저장소를 연결해서 코드를 깃허브와 깃랩, 비트버킷 등에 올리고 관리할 수도 있다.

## Clone

- git clone URL을 통해 원격 저장소의 리포지토리를 로컬에 가져올 수 있는데 URL뒤에 폴더명을 따로 지정해주면 해당 폴더에 가져올 수 있다.
- 만약 회사에서 협업을 하거나 또는 다른 사람의 리포지토리에 기여를 하고 싶다면, 해당 리포지토리를 자신의 깃허브에 fork해온 후, 클론을 통해 자신의 로컬에 가져와서 작업을 한 후, 변경사항을 커밋, 푸시한다.
- 푸시를 하게 되면 fork해온 리포지토리에 작업한 변경사항들이 올라가게 되는데, 해당 리포지토리에 변경사항을 Pull request를 통해 요청하게 되면, 해당 리포지토리에서 그 변경사항을 확인해서 반영하게 된다.
- 단, fork하지 않은 리포지토리를 클론하게 되면, 파일들을 로컬에 가져올 수는 있지만, 작업한 내용을 업로드해서 Pull request를 요청하지는 못한다.

## HEAD

- git log를 통해 커밋 히스토리와 현재 HEAD가 가르키는 곳을 확인할 수 있다.
- (HEAD -> main, origin/main): HEAD -> main은 현재 로컬에 올라간 커밋이고, HEAD -> origin/main은 깃허브 서버에 올라간 커밋이다.
- HEAD가 main, origin/main을 가르키고, main과 origin/main이 같은 선상에 있기 때문에 현재 로컬에서 커밋한 것이 깃허브 서버에도 동일한 커밋을 가지고 있다는 의미이다.

## VSCode Git

- VSCode에서 파란색 줄은 수정된 부분을 의미하고, 초록색 줄은 새로 추가된 부분을 의미한다.
- M: modified(수정된 파일)
- U: untracked(아직 깃에 의해 추적되지 않은 파일)
- A: added(새로 추가된 파일)

## Git CLI

- git log: 커밋 히스토리 확인
- git status: 깃 상태 확인
- git add 파일명: 하나의 변경된 파일을 staging area로 이동
- git add .: 현재 폴더에 변경된 모든 파일들을 staging area로 이동
- git restore --staged 파일명 또는 폴더명: 하나의 변경된 파일 또는 폴더를 staging area에서 다시 unstage area로 이동
- git restore --staged .: 변경된 모든 파일들을 staging area에서 다시 unstage area로 이동
- git rm 폴더명 -r —cached: 이미 staging area에 올린 폴더를 다시 unstage area로 내리기
- git commit -m "커밋 메세지": 커밋하기
- git commit -am "커밋 메세지": git add와 git commit -m을 동시에 하기 (단, 파일을 처음 생성 후, 커밋하는 경우는 불가)
- git commit —-amend -m “커밋 메시지”: 새롭게 추가된 변경사항을 마지막 커밋에 같이 추가해서 커밋한다.
- git commit —-amend --no-edit: 새롭게 추가된 변경사항을 마지막 커밋에 같이 추가해서 커밋한다. (마지막 커밋의 메세지를 유지한 채)
- git push origin 브랜치명: 원격 저장소의 브랜치명으로 푸시 (새로 만든 브랜치명도 포함)
- git push origin main -f: 원격 저장소의 main브랜치에 강제로 푸시
- git push -u origin +main: 충돌을 무시하고 강제로 원격 저장소 main브랜치에 푸시
- git checkout 커밋ID: 입력한 커밋ID에 해당하는 과거의 커밋 시점으로 돌아가기
- git checkout main: 과거의 커밋에서 다시 main브랜치로 이동
- git reset HEAD^: 커밋 기록만 삭제하고, 작업한 파일의 변경 사항은 그대로 유지하면서, working directory로 이동
- git reset HEAD^ --hard : 커밋 기록과 작업한 파일의 변경 사항을 삭제하면서 과거의 커밋으로 돌아가기
- git reset HEAD^ —-soft: 커밋 기록만 삭제하고, 작업한 파일의 변경 사항은 그대로 유지하면서 staging area로 이동
- git branch: 전체 브랜치 확인
- git branch 브랜지명: 브랜치 만들기
- git checkout 브랜치명: 해당 브랜치로 이동
- git switch -c 브랜치명: 새로운 브랜치를 생성 후, 이동 (=git checkout -b 브랜치명)
- git checkout 커밋id -b 브랜치명: 과거 커밋으로 checkout 후, 새로운 브랜치 생성 후, 이동
- git branch -d 브랜치명: 로컬 저장소에서 브랜치 삭제
- git push origin :브랜치명: 원격 저장소에서 브랜치 삭제 (=git push origin -d 브랜치명)
- git checkout -t 브랜치명: 원격 저장소에 있는 브랜치를 로컬로 가져오기
- git remote -v: Remote 목록 확인
- git remote add 원격저장소명 원격저장소URL: 원격 저장소 연결
- git remote remove 원격저장소명 원격저장소URL: 원격 저장소 연결 제거
- git remote rename 원격저장소명 바꿀 원격저장소명: 원격 저장소 이름 변경
- git clone URL: 원격 저장소의 리포지토리를 로컬에 복사
- git clone URL 폴더명: 원격 저장소의 리포지토리를 로컬에 지정한 폴더에 복사
