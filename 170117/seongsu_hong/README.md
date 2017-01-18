**Comment: ctr+c/ctr+v는 지양합시다~**


#1. 버전관리
###1-1. 버전관리란 무엇인가?
: 버전 관리(version control, revision control), 소스 관리(source control), 소스 코드 관리(source code management, SCM)란 동일한 정보에 대한 여러 버전을 관리하는 것을 말한다.

	공학과 소프트웨어 개발에서 팀 단위로 개발 중인 소스 코드나, 청사진 같은 설계도 등의 디지털 문서를 관리하는데 사용된다. 그러한 문서의 변경 사항들에 숫자나 문자로 이뤄진 "버전"을 부여해서 구분한다. "버전"을 통해서 시간적으로 변경 사항과 그 변경 사항을 작성한 작업자를 추적할 수 있다.

	간단한 버전 관리 방법으로는 처음 작성한 코드에 버전 번호 1을 부여한다. 변경 사항이 생기면, 버전 번호를 2로 증가시킨다. 이처럼 추후 변경 사항이 발생 시마다 버전 번호를 1씩 증가시킨다.
 	
 	소프트웨어 엔지니어링에서는 일반적인 소프트웨어 소스 코드만을 관리하는 내역을 주로 버전 관리라고 정의하게 된다. 일반적으로 산업 공학이나 이전 생산 기반 제조 공학 등에서 소프트웨어 쪽으로 넘어오는 학문적 관심에 의해 이전 생산 공학에서 사용하던 개념을 가져오게 되었고, 그에따라 버전 관리(Software Version Management)와 형상 관리(Software Configuration Management)의 개념들이 따라왔다고 볼 수 있겠다.

<hr>
**버전 관리를 이용해야하는 까닭**
: 거의 대부분의 주요 소프트웨어 개발 프로젝트는 아직도 소프트웨어의 설계도라 할 수 있는 소스 코드 작성이 주요한 부분이 되며 이러한 소스 코드는 기업체 또는 연구소의 핵심 역량이 응축된 핵심 자산이다. 따라서 어떠 형태로든 소스 코드를 백업하여 분실의 위험에서 보호하고 개정 전후 내용을 파악하여 추후 발생할지도 모를 오류 수정에 대비하는 절차가 필요하다. 버전 관리 소프트웨어는 조직의 핵심 자산인 소스 코드의 개정과 백업 절차를 자동화하여 오류 수정 과정을 도와줄 수 있는 시스템으로 이미 다수의 국제 협력 개방 소프트웨어 개발 실무에서도 널리 사용되고 있다. 다음은 버전 관리 시스템을 사용하는 원인을 정리한 것이다.

	* 무언가 잘못되었을 때 복구를 돕기 위하여
	* 프로젝트 진행 중 과거의 어떤 시점으로 돌아갈 수 있게 하기 위하여
	* 여러사람이 같은 프로젝트에 참여할 경우, 각자가 수정한 부분을 팀원 전체가 동기화하는 과정을 자동화하기 위하여
	* 소스 코드의 변경 사항을 추적하기 위하여
	* 소스 코드에서 누가 수정했는지 추적하기 위하여
	* 대규모 수정 작업을 더욱 안전하게 진행하기 위하여
	* Branch로 프로젝트에 영향을 최소화 하면서 새로운 부분을 개발하기 위하여
	* Merge로 검증이 끝난 후 새로이 개발된 부분을 본류(trunk)에 합치기 위하여
	* 많은 오픈 소스 프로젝트에서 어떠한 형태로든 버전 관리를 사용하고 있으므로
	* 코드의 특정 부분이 왜 그렇게 쓰여 졌는지 의미를 추적하기 위하여
<hr>
###1-2. 버전관리 방법
1. 로컬버전관리시스템
: 대부분의 사람들이 버전 관리를 위해 쓰는 방법은 파일을 다른 디렉토리에 복사하는 것이다(똑똑한 사람이라면 디렉토리 이름에 시간을 넣을 것이다). 이 방법은 간단하고 자주 사용되는 방법이지만 실수가 발생하기 쉽다. 어느 디렉토리에서 작업하고 있었는지 잊어버리고 엉뚱한 파일을 덮어쓰거나 의도하지 않았던 위치로 복사할 수도 있다.
![](/home/hong/바탕화면/local.png)
2. 중앙 집중식 버전 관리 시스템 (Centralized Version Control System; CVCS)
: CVCS는 로컬 VCS에 비해 장점이 많다. 누구나 다른 사람들이 무엇을 하고 있는지 알 수 있고, 관리자는 누가 무엇을 할 수 있는지 꼼꼼하게 관리할 수 있다. CVCS를 관리하는 것은 수많은 클라이언트의 로컬 데이터베이스를 관리하는 것보다 훨씬 쉽다.
그러나 CVCS는 심각한 단점이 있다. 중앙 서버가 잘못되면 모든 것이 잘못된다는 점이다. 서버가 다운될 경우 서버가 다시 복구될 때까지 다른 사람과의 협업도, 진행 중이던 작업을 버전 관리하는 것도 불가능해진다.
![](/home/hong/바탕화면/center.png) 
3. 분산 버전 관리 시스템 (Distributed Version Control System; DVCS)
: 버에 문제가 생겨도 어느 클라이언트든 복제된 저장소를 다시 서버로 복사하면 서버가 복구된다. 체크아웃(checkout)을 할 때마다 전체 백업이 일어난다.
![](/home/hong/바탕화면/server.png) 
<hr>
#2. git 명령어
 * git init : 현재 디렉토리에 .git폴더 생성
 * git status : 현재 디렉토리 상태 확인
 * git clone : remote 저장소를 통째로 워킹 디렉토리에 복사
 * git pull : remote의 정보를 가져와 디렉토리와 병합
 * git add : 새로 만들어졌거나 변경된 파일을 디렉토리에서 stage에 올리기
 	* git add 이름
 	* git add * 
 * git commit : stage에 올라온 파일을 local repo에 올리기 +comment를 남기기
 	* git commit -m "커밋에 대한 설명"
 	* git commit -a -m "커밋에 대한 설명"(add와 commit 한번에)
 * git push : remote로 파일, comment 보내기
 	* git push origin master
 *  git remote : 깃에 원격서버주소를 지정
 	* git remote add origin 원격서버주소
 * git revert 커밋넘버 : 해당 commit을 취소
 * git reset 커밋넘버 : 해당 commit으로 작업 되돌림되돌
 * git checkout -b feature : feature라는 branch를 만들고 이동
 * git checkout master : master branch로 이동
 * git brach -d feature : feature 라는 branch를 삭제
 * git merge 이름 : 해당 디렉토리에서 merge 실행
 * git diff 원래branch 비교비branch : 변경 내용 merge 전에 바뀐 내용전송 확인
 * git log : commit 기록 보기
 	* git log --graph : branch log를 그래프로 보기
 * git checkout -- 파일이름 : 변경 내용을 변경 전 상태로 되돌림
 * gitk : git의 내장 GUI
 * git config color.ui true : git output을 컬러로 출력하기
 