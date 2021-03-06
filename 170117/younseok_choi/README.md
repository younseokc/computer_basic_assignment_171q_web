형상관리(버전관리)란  

소프트 웨어 형상관리는소프트웨어 개발 및 유지보수 과정에서 발생하는 소스코드, 문서, 인터페이스등 각종 결과물에 대해 형상을 만들고, 이들 형상에 대해 변경을 체계적으로 관리, 제어하기 위한 활동이다. 

아주 단순히 말하면, 프로젝트를 진행하면서 생성하는 소스코드나 그 외 다양한 작업물들을 SVN이나 GIT을 통해 버전관리 시스템을 이용하는 것을 말한다.

형상관리는 원래 하드웨어개발 시에 수많은 부품들을 정리하기 위해 버전과 id번호를 부여하면서 사용되었던 방식이지만 소프트웨어를처음 개발할 당시에는 진공카드나 테이프 혹은 다른 매체를 이용한 물리적인 무언가를 출력해서 개발하는 방식 이였기 때문에 큰 차질없이 형상관리라는단어를 사용했다.

다수의 개발자가 프로젝트에서동일한 기능을 동시에 개발한다고 할 때, 작성된 소스코드와 변경사항을 확인하고 수정하는 협업을 도와주는시스템이라고도 할 수 있다.

 

형상관리 툴의 종류와특징**

대표적인 형상관리 툴엔 SVN,CVS,GIT 이있다.

 

CVS**

CVS는 Concurrent Versions System의 약자로, 소프트웨어 개발 프로젝트에서 파일단위의 모든 작업과 모든 변화를 추적하고 여러 개발자가 협력하여 작업할 수 있도록 한다.

CVS는 오랜 기간에 걸쳐많은 사용자들을 확보한 검증된 버전관리 소프트 웨어이다. CVS의 장점은 Mac OS, 리눅스, 윈도우 전부 사용이 가능하고, 하나의 파일에 대해 동시 작업이 가능하다. 

 

그러나 CVS는 속도가 느리고, 저장소의 파일들의 이름 변경이 불가능하기때문에 파일 자체를 제거하고 다시 추가해야 되는 단점이 있다. 그리고 가장 치명적인 단점으로는 커밋실패 시 롤백이 지원되지 않는다. 

 

SVN

SVN은 Subversion'의 약자로, 버전관리 소프트웨어이다. 명령형 인터페이스에서 사용하는 명령어를 따서 SVN이라고 부른다. SVN은 SVS의 단점을 보안하기 위해 만들어졌다. 

 

다른 사용자와 커밋이잘 엉키지 않으며, 실패 시 롤백 기능을 지원한다. 파일과 디렉토리 삭제, 이동, 이름변경, 복사등을 지원한다. 또한 소스파일 이외의 다른 텍스트 파일이나 이미지 파일 심지어 디렉토리 역시도 버전관리가가능하다. 

 

그러나 SVN은 안정성이 꽤 떨어지는 편이다. 소스코드의 경우엔 안정적이지만그 외의 텍스트나 이미지 파일의 경우 안정성이 떨어지는 편이다. 또한 소스코드 라도 잦은 커밋을 한경우 종종 엉키게 된다. 

 

GIT

GIT 은 리눅스 커널관리를위해 개발한 것이였으나 현재는 다른 곳에서도 널리 사용되고 있는 분산형 버전 관리 시스템이다. 

 

SVN은 로컬 컴퓨터에 저장되는것이 아니라, NAS와 같은 중앙 저장소에 커밋을 한다. 그러나 GIT의 경우엔 자신의 작업물이 우선 로컬 저장소에 저장을 한다. 이로컬에 있는 저장공간은 중앙저장소에 영향을 미치지 않는다. 그리고 로컬 내에서 브랜치를 만들고, 커밋을 하고 롤백 하는 것까지 가능하다. 

 

그렇기 때문에 GIT은 로컬이 아닌 원격 저장소에 백업을 하고 싶으면 머지 하는 방식으로 통합한다. SVN과 CVS를 사용하는 것보다 한 단계가 더 필요한 것이다. 그렇기 때문에 개발자의 프로세스가 좀 더 길어진 것이다. 물론 그만큼안정성을 보장해주지만, 이를 위해 조금은 복잡한 명령어들을 외워야 되기 때문에 거추장스럽다는 의견도있다. 





간단한 터미널 명령어 

    pwd - 현재 경로 표기
    open  .(open과 .은 두번 띄운다.) - 현재 터미널에서 보고 있는 창을 윈도우에서 띄어줌
    rm rf 'directory' - 해당 폴더 삭제
    rm 'filename' - 해당 파일 삭제



GIT Terminal 명령어

    git init : 현재 있는 워킹 디렉토리에 git 폴더 새엇ㅇ
    git status : 현재 워킹 디렉토리 상태를 확인
    git log : git의 log를 확인
    git log -p : 파일 수정을 디테일하게 보여줌 
    git clone : remote저장소를 통째로 워킹 디렉토리로 복사
    git pull : remote의 정보를 가져와 워킹디렉토리와 병합
    git add 'filename' :  변경한 해당 파일을 stagearea에 올려놓기 위함
    git add -A : stagearea에 올라가있지 않은 모든 파일들을 한번에 올리는 것
    git commit : stagearea에 있는 파일들을 커밋시키는 것
    git commit 'filename' : stagearea에 있는 지정한 해당파일을 커밋시키는 것
    git reset --hard '커밋 번호' : 해당 커밋 번호로 하드 리셋
    git revert '커밋 번호' : 해당 커밋으로 돌아감
    git push origin : 원격의 레퍼런스로 업데이트 한다.
    
    
    branch
    git branch - 현재 있는 브렌치 목록을 보여준다.
    git branch 'branch name' - 지정한 브렌치 이름으로 브렌치를 생성한다.
    git branch 'branch name' 'Parent branch name' - 상위 브렌치 밑에 하위 브렌치를 생성한다.g
    git checkout 'branch name' - 지정한 브렌치 이름으로 옮겨서 작업한다.
    git branch -d 'branch name' - 지정한 브렌치를 삭제한다.
    git merge 'commit code'- 현재 브렌치에 해당 커밋코드의 커밋과 머지 시킨다.
    git branch -v - 각각의 브렌치의 마지막 커밋 상태를 보여준다.
    


