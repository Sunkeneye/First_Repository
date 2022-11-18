# First_Repository

## 요청사항

- 지금 git 명령어가 정확히 무슨 역할을 하는지 확인할 필요가 있음
- 아래는 예시

```shell
git branch -M main # main branch 생성
```

## 에러 발생

- Repo를 생성하면서 Nest.js폴더와 React.js폴더를 연결하던 중에 문제가 발생
- 원래는 First-Repository와 연결을 하려고 하였으나 아예 새로운 Repo를 만들어 연결하기 위해 Second_Repository를 생성하여 이 Repo와 연결하려고 GitHub의 공식 매뉴얼(...or push an existing repository from the command line)대로 하였으나

```
git remote add origin https://github.com/Sunkeneye/Second_Repository.git\n
git branch -M main
git push -u origin main
```
- 을  Git Bash에 입력하였으나

```
error: remote origin already exists.
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/Sunkeneye/First-Repository.git'
```

- 라는 에러가 발생

- 구글링을 통해 해결방법을 찾아 아래대로 입력하였으나
```
git remote remove origin
git remote add origin https://github.com/Sunkeneye/Second_Repository.git
git remote -v
  'Git Bash의 반응': origin https://github.com/Sunkeneye/Second_Repository.git (fetch)
  'Git Bash의 반응': origin https://github.com/Sunkeneye/Second_Repository.git (push)
git push origin master
  'Git Bash의 반응': error: src refspec main does not match any
  'Git Bash의 반응': error: failed to push some refs to 'https://github.com/Sunkeneye/Second_Repository.git'
```

- 라는 에러가 또 발생

- 다시 구글링을 하여 해결을 하려고 아래의 코드를 넣으려고 하였으나

```
git init
git add .
git commit -m "message"
git remote add origin "https://github.com/Sunkeneye/Second_Repository.git"
git push -u origin master
```

- git add . 에서 waring: ~ 같은 스크립트가 끝도 없이 작성되어 중단한 상황
    
Help...


- Node.js
JavaScript로 브라우저 밖에서 서버를 구축하는 등의 코드를 실행할 수 있게 해주는 런타임 환경
웹퍼블리싱은 기본적으로  HTML, CSS, JavaScript 언어를 사용하여 프로젝트를 진행함
또한 시간적 생산성, 편리성, 필요성, 크로스 브라우징 등을 위해 다양한 라이브러리를 사용하는데
이를 디펜던시스(dependencies)라고 한다
이 라이브러리들을 설치하고 사용하기 위해서는 이를 제공하는 각각의 사이트에 접속하여
파일을 다운로드하거나, CDN으로 연결하여 사용해야 한다
그렇기에 최신 버전의 라이브러리가 나오거나 최신 버전의 CDN 경로를 알기 위해서는
매번 해당 라이브러리 사이트에 방문해야 한다
이 시간적 소모와 번거로움을 해결하기 위한 것이 yarn 패키지 매니저다

- npm(Node Package Manager)
Node.js의 기본 패키지 매니저
npm은 필수 단계를 순차적으로 수행하기 때문에 한 개의 패키지 다운로드를 완료해야
다음 패키지를 다운로드 할 수 있다

- yarn
페이스북에서 발표한 Node.js의 패키지 매니저

- 패키지(package)
전 세계의 개발자들이 제작한 다양한 자바스크립트 코드를
npm 온라인 데이터베이스에 업로드하여 게시하며 공유하는데
이것을 프로그램 패키지라고 한다.
이러한 패키지들은 누구나 사용 가능하며 npm 또는 yarn과 같은 패키지 매니저를 통하여 다운로드가 가능하다

- 패키지 매니저
컴퓨터의 운영체제를 위해 일정한 방식으로 
컴퓨터 프로그램의 설치, 업그레이드 구성, 제거 과정을 자동화하는 소프트웨어 도구들의 모음
- nvm
Node.js의 버전 관리자
Linux의 쉘 스크립트 언어로 만들어졌기 때문에 Windows에서는 사용할 수 없다.
따라서 리눅스 환경을 만들어줘야 함

- yarn 설치 방법
Node.js를 설치하면 자동적으로 설치된다

1. Node.js 설치
2. Node.js 설치 후 윈도우 cmd에서 yarn 설치 여부 확인
>>>npm install -g yarn == npm으로 global로 설정된 yarn을 설치하라
4.cmd에서 명령어 입력 후 결과값 확인
>>>node -v == 설치된 node.js의 버전을 표시하라
>>>npm -v == 설치된 npm의 버전을 표시하라
>>>yarn -v == 설치된 yarn의 버전을 표시하라
```
C:\Users\sunke\node -v
v18.12.1

C:\Users\sunke\npm -v
8.19.2

C:\Users\sunke\yarn -v
1.22.19
```

- Docker
애플리케이션의 모든 코드 및 종속성을 표준 형식으로 패키징할 수 있게 해주는 컨테이너
이를 통해 애플리케이션이 컴퓨팅 환경 전반에서 빠르고 안정적으로 실행될 수 있다
리눅스의 응용 프로그램들을 프로세스 격리 기술들을 활용하여 컨테이너로 실행하고 관리하는 오픈소스 프로젝트

- 컨테이너
운영체제의 커넝리 하나의 사용자 공간 인스턴스가 아닌
여러 개의 격리된 사용자 공간 인스턴스를 갖출 수 있도록 하는 서버 가상화 방식

- 사용자 공간 
전통적인 컴퓨터 운영체제는 일반적으로 가상 메모리를 커널 공간과 사용자 공간으로 분리시킨다
커널 공간은 커널, 커널 확장 기능, 대부분의 장치 드라이버를 실행하기 위한 예비 공간이다
사용자 공간은 모든 사용자 모드 응용 프로그램들이 동작하는 메모리 영역으로,
이 메모리는 필요할 때 페이징 처리될 수 있다

- 커널(kernel)
컴퓨터 운영체제의 핵심이 되는 컴퓨터 프로그램으로 시스템의 모든 것을 완전히 통제한다
운영체제의 다른 부분 및 응용 프로그램 수행에 필요한 여러 가지 서비스를 제공한다

- 커널의 역할
보안: 커널은 컴퓨터 하드웨어와 프로세스의 보안을 책임진다
자원 관리: 한정된 시스템 자원을 효율적으로 관리하여 프로그램의 실행을 원활하게 한다
특히 프로세스에 처리기를 할당하는 것을 스케줄링이라고 한다
추상화: 같은 종류의 부품에 대해 다양한 하드웨어를 설계할 수 있기 때문에 
하드웨어에 직접 접근하는 것을 문제를 매우 복잡하게 만들 수 있다.
일반적으로 커널은 운영체제의 복잡한 내부를 감추고 깔끔하고 일관성 있는 인터페이스를 
하드웨어에 제공하기 위해 몇 가지 하드웨어 추상화(같은 종류의 장비에 대한 공통 명령어의 집합)
들로 구현된다.
이 하드웨어 추상화는 프로그래머가 여러 장비에서 작동하는 프로그램을 개발하는 것을 돕는다.
하드웨어 추상화 계층(HAL)은 제조사의 장비 규격에 대한 특정한 명령어를 제공하는 소프트웨어 드라이버에 의지한다

- 인스턴스(가상 머신)
컴퓨팅 환경을 소프트웨어로 구현한 것, 즉 컴퓨터 시스템을 에뮬레이션(가상현실화)하는 소프트웨어
가상머신상에서 운영체제나 응용 프로그램을 설치 및 실행할 수 있다

- Docker 설치
설치 도중 문제가 발생
```
Docker.Core.DockerException:
Failed to start
   위치: Docker.Engines.LinuxkitDaemonStartup.<WaitAsync>d__5.MoveNext() 파일 C:\workspaces\main-merge\src\github.com\docker\pinata\win\src\Docker.Engines\LinuxkitDaemonStartup.cs:줄 54
--- 예외가 throw된 이전 위치의 스택 추적 끝 ---
   위치: System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
   위치: System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
   위치: Docker.Engines.WSL2.LinuxWSL2Engine.<DoStartAsync>d__26.MoveNext() 파일 C:\workspaces\main-merge\src\github.com\docker\pinata\win\src\Docker.Engines\WSL2\LinuxWSL2Engine.cs:줄 170
--- 예외가 throw된 이전 위치의 스택 추적 끝 ---
   위치: System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
   위치: System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
   위치: Docker.ApiServices.StateMachines.TaskExtensions.<WrapAsyncInCancellationException>d__0.MoveNext() 파일 C:\workspaces\main-merge\src\github.com\docker\pinata\win\src\Docker.ApiServices\StateMachines\TaskExtensions.cs:줄 29
--- 예외가 throw된 이전 위치의 스택 추적 끝 ---
   위치: System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
   위치: System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
   위치: Docker.ApiServices.StateMachines.StartTransition.<DoRunAsync>d__5.MoveNext() 파일 C:\workspaces\main-merge\src\github.com\docker\pinata\win\src\Docker.ApiServices\StateMachines\StartTransition.cs:줄 67
--- 예외가 throw된 이전 위치의 스택 추적 끝 ---
   위치: System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
   위치: Docker.ApiServices.StateMachines.StartTransition.<DoRunAsync>d__5.MoveNext() 파일 C:\workspaces\main-merge\src\github.com\docker\pinata\win\src\Docker.ApiServices\StateMachines\StartTransition.cs:줄 92
```

https://github.com/docker/for-win/issues/12960에서 문제 해결

Git Bash에서 netsh winsock reset 입력 후 문제 해결
```
netsh winsock reset : winsock 키를 재작성하라
```
- netsh: 네트워크 셸
네트워크 셸은  Windows Server를 실행하는 컴퓨터에 다양한 네트워크 통신서버 역할 및 구성 요소를
설치한 후 이들의 상태를 구성하고 표시할 수 있는 명령줄 유틸리티다
- winsock(Windows Socket API)
Windows와 TCP/IP 간의 통신을 지원하는 프로그래밍 인터페이스
윈도우 운영체제의 인터넷 응용 프로그램에 대한 입력 및 출력 요청을 다룬다
- Netsh Winsock Reset을 하면 어떤 일이 일어나는가
Winsock을 재설정하면 Windows에서 Winsock 카탈로그에 대한 구성이 실행 취소된다
웹 브라우저, 이메일 클라이언트 또는 VPN 프로그램과 같은 네트워킹 프로그램으로 변경할 수 있다
wsock32 DLL 파일을 기본 설정으로 되돌려 해당 소프트웨어가 TCP/IP 트래픽에 연결할 때 새로운 시작을 하도록 한다

- WSL2 설치
WSL은 윈도우에서 경량 가상화 기술을 사용해 리눅스를 구동할 수 있도록 도와주는 기능
WSL를 설치해야 Docker를 실행할 수 있음



- Docker 설치 후 Git Bash에서 버전 테스트
```
sunke@Sunkeneye MINGW64 ~
$ docker -v
Docker version 20.10.20, build 9fdeb 9c

sunke@Sunkeneye MINGW64 ~
$ docker ps
CONTAINER ID		IMAGE		COMMAND		CREATED		STAT
US			PORTS		NAMES
81dbdd2932ae		docker101tutorial		"/docker-entrypoint._"		7 minutes ago		UP 7
 minutes		0.0.0.0.:80->80/tcp docker-tutorial

sunke@Sunkeneye MINGW64 ~
$ git -v
git version 2.38.1.windows.1
```

- Nest.js
Node.js에 기반을 둔 웹 API 프레임워크로써 Express 또는 Fastify 프레임워크를 래핑하여 동작한다
Node.js는 손쉽게 사용할 수 있고 뛰어난 확장성을 가지고 있지만, 
과도한 유연함으로 인해 SW의 품질이 일정하지 않고
알맞은 라이브러리를 찾기 위해 사용자가 많은 시간을 할애해야 한다.
이에 반해 Nest.js는 데이터베이스, ORM, 설정(Configuration), 유효성 검사 등 수많은 기능을 기본으로 제공한다
Angular로부터 영향을 받아 모듈/컴포넌트 기반으로 프로그램을 작성함으로써 재사용성을 높여준다
IoC(Inversion of Control, 제어역전), DI(Dependency Injection, 의존성 주입), AOP(Aspect Oriented Programming, 관점 지향 프로그래밍)와 같은 객체 지향 개념을 도입했다
프로그래밍 언어는 타입스크립트를 기본으로 채택하고 있어 타입스크립트가 가진 타입시스템의 장점을 누릴 수 있다

https://docs.nestjs.com/
To install the TypeScript starter project with Git:
```
$ git clone https://github.com/nestjs/typescript-starter.git project
$ cd project
$ npm install
$ npm run start


sunke@Sunkeneye MINGW64 ~ (main)
$ git clone https://github.com/nestjs/typescript-starter.git project
Cloning into 'project'...
remote: Enumerating objects: 955, done.
remote: Counting objects: 100% (33/33), done.
remote: Compressing objects: 100% (29/29), done.
remote: Total 955 (delta 12), reused 14 (delta 4), pack-reused 922
Receiving objects: 100% (955/955), 1.79 MiB | 9.12 MiB/s, done.
Resolving deltas: 100% (500/500), done.

sunke@Sunkeneye MINGW64 ~ (main)
$ cd project

sunke@Sunkeneye MINGW64 ~/project (master)
$ npm install
npm WARN old lockfile
npm WARN old lockfile The package-lock.json file was created with an old version of npm,
npm WARN old lockfile so supplemental metadata must be fetched from the registry.
npm WARN old lockfile
npm WARN old lockfile This is a one-time fix-up, please be patient...
npm WARN old lockfile

added 700 packages, and audited 701 packages in 10s

80 packages are looking for funding
  run `npm fund` for details

1 high severity vulnerability

To address all issues, run:
  npm audit fix

Run `npm audit` for details.

sunke@Sunkeneye MINGW64 ~/project (master)
$ npm run start

> nest-typescript-starter@1.0.0 start
> nest start

[Nest] 5436  - 2022. 11. 16. 오후 1:26:23     LOG [NestFactory] Starting Nest application...
[Nest] 5436  - 2022. 11. 16. 오후 1:26:23     LOG [InstanceLoader] AppModule dependencies initialized +16ms
[Nest] 5436  - 2022. 11. 16. 오후 1:26:23     LOG [RoutesResolver] AppController {/}: +3ms
[Nest] 5436  - 2022. 11. 16. 오후 1:26:23     LOG [RouterExplorer] Mapped {/, GET} route +1ms
[Nest] 5436  - 2022. 11. 16. 오후 1:26:23     LOG [NestApplication] Nest application successfully started +1ms





Open your browser and navigate to http://localhost:3000/.

>>> Hello World!
```
라는 결과가 나옴

- React.js
메타에서 개발한 오픈 소스 자바스크립트 라이브러리

Create React App
```
npx create-react-app my-app
cd my-app								*cd : Change Directory. 디렉토리로 이동
npm start
```
의 명령어를 입력했어야 했으나

//npx create-react-app my-app 
명령어가 인식이 되지 않았음

```
$ npx create-react-app my-app
The directory my-app contains files that could conflict:

  node_modules/
  package-lock.json
  package.json
  public/
  src/

Either try using a new directory name, or remove the files listed above.
```
라는 반응이 나옴
이 문제를 제대로 해결하지 않았던 게 화근이었을까

- Github에서 첫 번째 Repository 만들기
```
git remote add origin https://github.com/Sunkeneye/First-Repository.git
( 원격 저장소(=Github)에 연결하기 )

git branch -M main
( branch 생성 후 이동. -M main의 의미는 정확히 파악하지 못 함)

git push -u origin main
( 지역 저장소의 커밋을 맨 처음 원격 저장소에 올리는 경우 )
```
순서대로 Git Bash에 입력하던 도중 문제가 발생

```
error: remote origin already exists.
>>> 원격 저장소가 이미 존재한다는 뜻(?)

error: src refspec main does not match any
>>> 새로운 폴더를 만들거나 해당 폴더 내 생성된 .git 파일들을 삭제 후 처음부터 명령어를 입력하면 된다고 함

error: failed to push some refs to 'https://github.com/Sunkeneye/First-Repository.git'
>>> 원격 저장소에 내 로컬(내 컴퓨터)에 없는 파일이 있을 때 내 파일을 push 하면 발생하는 오류
```
라는 반응

구글링을 통해 해결 방법을 찾아 아래대로 입력하였으나
```
git remote remove origin
git remote add origin https://github.com/Sunkeneye/Second_Repository.git
git remote -v
  'Git Bash의 반응': origin https://github.com/Sunkeneye/Second_Repository.git (fetch)
  'Git Bash의 반응': origin https://github.com/Sunkeneye/Second_Repository.git (push)
git push origin master
  'Git Bash의 반응': error: src refspec main does not match any
  'Git Bash의 반응': error: failed to push some refs to 'https://github.com/Sunkeneye/Second_Repository.git'
```
라는 에러가 또 발생


다시 구글링을 하여 해결을 하려고 아래의 코드를 넣으려고 하였으나
```
git init
git add .
git commit -m "message"
git remote add origin "https://github.com/Sunkeneye/Second_Repository.git"
git push -u origin master  
```
//git add .
에서 waring: ~ 같은 스크립트가 끝도 없이 작성되어 중단한 상황
하지만 이건 내가 뭘 잘 몰라서 벌어진 문제였고...
위의 코드는 내가 생성한 코드를 github에 올릴 때 사용하는 코드였음...


- 진욱이의 솔루션을 받은 결과
이상한 디렉토리에 git add .이 되어 있었고
nest.js와 react.js를 재설치하고 디렉토리를 새로 만들어 각각 git에 연결함

nest.js 재설치 명령어
```
$ npm i -g @nestjs/cli
>>> npm에게 명령 / install하라 / global범위로 / nest.js 클라이언트를

$ nest new sunkeneyenest
>>> nest에게 명령 / 새로운 디렉토리 sunkeneyenest를 생성하라 (사용자 디렉토리에 저장된다)
```

react.js 재설치 명령어
```
$ npx create-react sunkeneyereact
>>> npx에게 명령(npm 5.2+버전의 패키지 실행 도구) / react 디렉토리 sunkeneyereact를 생성하라

$ cd sunkeneyereact
>>> sunkeneyereact 디렉토리로 변경하라(이동하라?)

$ npm start
>>> npm에게 명령 / 실행하라
```

이렇게 nest.js 디렉토리와 react.js 디렉토리가 생성됨
이제 이 디렉토리를 git의 새로운 repository에 push한다

git에 디렉토리 push하기

1. push할 디렉토리에 들어가서 해당 경로에서 cmd입력
2. cmd에서 code . 입력 ( vscode에서 해당 디렉토리 전체를 열기 )
3. vscode 터미널에서 git init ( git 저장소를 생성 )
4. git add . ( git에 해당 로컬 디렉토리 전부를 스테이지에 올린다 )
5. git remote add origin https://github/Sunkeneye/SunekeneyeNest.git ( git의 원력 레파지토리에 추가한다)
6. git branch -M main
7. git push -u origin main
후에 문제 로컬 디렉토리를 repository에 정성작으로 연결 성공
