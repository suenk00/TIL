# GIT

## 초기 설정

- 최초로 한 번 만 설정하면 된다!

1. 누가 커밋을 남겼는지 확인할 수 있도록 이름과 이메일을 설정함

- 수정하려면 덮어쓰기 하면 된다

``` bash
# 명령어 사용 시 먼저 주체 설정
$ git config --global user.name 이름	
$ git config --global user.email 이메일	
# 주체 git 설정, 전역에 설치, -는 축약, 전역에 사용자 이름 설정, 이메일 설정
## gitlab 저장
```

2. 설정된 내용 확인

```bash
$ git config --global --list
# or
$ git config --global -l
```

3. 작업공간 구분 필요

- git으로 관리하기 위한 초기화 과정 필요
- TIL폴더 아래 md 파일 추적
- 이 과정에서 commit을 하면 version 상태 생성. 그러면 제목만 있던 내용에 대해 git이 추적하기 시작함. 즉, 내용이 추가되었다는 사실을 git이 추적하기 시작함. 

- commit을 통해 version을 쌓아가는 과정을 github라는 원격 저장소에 저장하는 것 = push 한다

  

  ** 주요 명령어

  add/commit/push

  commit: 변경 사항을 한 번에 저장하는 명령어

```bash
# 초기 설정
$ cd TIL/
$ ls
$ git init
```



## git init

- 현재 작업중인 directory git으로 관리



### 주의 사항

- 이미 master로 관리 중인 폴더 내에서 절대 절대 git init 금지!!!!



## git status

- Working directory와 Staging Area에 있는 파일들의 현재 상태 확인
- 상태
  1. `untracked` : git이 관리하지 않는 파일
  2. `tracked` : git이 관리하는 파일
     1. `Unmodified` : 최신 상태
     2. `Modified` : 수정되었지만 staging area에 반영되기 전
     3. `staged` : Staging area에 반영된 상태



## git add

```bash
# 특정 파일
$ git add file_name.txt

# 특정 폴더
$ git add folder/

# 현재 디렉토리에 속한 모든 파일/폴더
$ git add .
```



## git commit

- staging area에 올라온 파일의 변경 사항을 하나의 버전으로 저장하는 명령어
- `커밋 메세지`는 현재 변경사항을 기록하는 용도로 사용

``` bash
$ git commit -m "커밋 메세지"
[master (root-commit) d48f1b5] fist commit
 3 files changed, 99 insertions(+)
 create mode 100644 markdown/GIT.md
 create mode 100644 "markdown/\353\213\250\354\262\264\353\263\264\355\227\230\352\260\200\354\236\205\354\204\234\353\245\230_\353\266\200\354\232\270\352\262\275_1\353\260\230_\352\266\214\353\202\230\354\235\200.docx"
 create mode 100644 "markdown/\353\266\200\354\232\270\352\262\275_1\353\260\230_\352\266\214\353\202\230\354\235\200(3740).jpg"
 
## root-commit이라는 원래 초기의 상태에서 3개 파일이 바뀌었고 99개가 추가되었다...
```



## git log

- 커밋의 내역을 조회할 수 있는 명령어

- 옵션

  - `--oneline`: 한 줄로 축약했음을 보여줌

  - `--graph` : 브랜치와 머지 내력을 그래프로 보여주는 명령어
  - `--all` : 모든 브랜치의 내역
  - `--reverse` : 커밋 내역의 순서를 반대로 보여주는 명령어



** Staging area에서 git으로 이미 옮겨졌다면 더 add할 필요 없이 commit만 하면 된다. 하지만 수정된 사항은 staging area에 반드시 다시 올려야 함!!

*즉, add -> commit 의 반복 기억하기*

