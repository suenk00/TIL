## REVIEW

# Github

### 회원가입

### 설정 변경

- main 브랜치를 master 브랜치로 기본값 수정

---

### 원격 저장소와 로컬 저장소 연결 방법

#### Repository 생성

- git remote
- git push: 내용 입력

**  루트 디렉토리(`/`)

- 일반적으로 windows c드라이브

** 홈 디렉토리(`~`)

- 홈 디렉토리로 이동

```BASH
$ cd Desktop/ #desktop 이동
$ cd TIL/ #TIL로 이동
$ git status #상태확인
$ git status
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   GIT.md
        deleted:    markdown/GIT.md

Untracked files: #트래킹이 안되는 파일
  (use "git add <file>..." to include in what will be committed)
        GITHUB.md

no changes added to commit (use "git add" and/or "git commit -a")
$ git add GITHUB.md #로 추가
# 아직까지는 추적파일만 만드는 중. 버전 추가 아님
```

### .gitignore

- 원격 저장소에도 파일이 있고, 로컬에도 이미 있고, 이미 트래킹 중인 파일을 로컬에서만 더 이상 추적하지 않도록 설정 -> 수정사항 발생 등 git에서 관리하지 않도록 하는 기능.

```bash
$ git update-index --assume-unchanged {file name} # 잘 안씀
```

- 로컬에 있는 파일 변동 추적 멈춤
- 원격 저장소에 해당 파일이 있다면 그 파일 삭제(원격 저장소에 push할 때 해당 파일 삭제)

​		ex tracking 되고 있는 사실만 삭제

```bash
$ git rm --cached {file name} # 자주 씀
```

- 로컬, 원격 저장소 모두 파일 삭제 후 추적 중지
- 그냥 파일 삭제랑 다른 점: 그냥 파일 삭제 시 git에 남아있음. 

```bash
$ git rm {file name} # 자주 씀
```

---



- 새로운 프로젝트 시작할 때 최상단에 만들어 두고 하는 것이 편할 것.

```bash
$ touch .gitignore # 숨김 파일 생성
$ touch password.txt # 패스워드 설정

gitignore.io 이용해서 숨김 프로세스 생성 가능 
```

** 상대경로:  내가 있는 위치를 기준으로 파일이 존재하는 곳을 찾아가는 것



---

- 새로운 수정사항 설정
- 계정을 만든 사람과 push한 사람이 다르면 오류 발생
- 계정 자체를 바꿔서 로그인하고 싶다면 window에 로그인된 자격증명을 바꿀 기능 사용
  - [자격 증명 관리자] - [Windows 자격 증명]-[편집] or [제거] 후 새 아이디로 재로그인

----



```bash
** #- 약자씀/ -- 풀네임
$ git commit -m "create github" # 변경사항 저장하기 위한 설명. 한 문장이 가장 좋음
$ git log --one line # 한 문장으로 로그 설명
```



#### github 사용설명

- Add a README file
  - 파일 내용 안에 있는 내용에 대한 설명 etc

```bash
echo "# TIL" >> README.md
git init 	# 최초로 초기화. 한 번만 하면 된다.
git add README.md
git commit -m "first commit"
git branch -M master
git remote add origin https://github.com/suenk00/TIL.git # 내가 만든 repository를 원격저장소에 추가하는데 그 별명을 origin이라는 이름으로 만들어 줌. git으로 관리하고 있는 업로드할 대상의 이름을 만든 것. origin자체의 다른 의미는 없음. git에 밀어넣을 건데 origin이라는 경로에다 master라는 것을 추가하는 것.  햐
# git remote add origin or git remote add origin second라는 이름으로 다른 곳에 저장할 수도 있음
git push -u origin master
# 원격 저장소에 추가. 한 번만 하면 된다.
```

** 붙여넣기: 오른쪽 마우스/shift+insert

** 간혹 `(end)`가 떠서 입력이 불가해진다면 `q`누르기!

** 파일 추가하고 싶으면 add commit 하기 `git add GITHUB.md` etc



#### 작성자 바꾸기

```bash
# 해당 채널에만 작성자 변경
$ git config user.email ____(이메일)
$ git config --global -l # 로 확인

$ cat. git/config # 해당 git에서 관리하고 있는 user 만 확인 가능
# 내부 설정만 바꾸는 것이기 때문에 status에는 안 뜸
```



** `add - commit - push` 반복

수정사항 발생 시 변경사항 추가한 후  commit

반드시 중간중간에 commit해서 브랜치 만들어 두기



#### 파일 불러오기

- clone: 없는 파일 불러오기. 저장

  ** 만약 삭제 작업 전 없어질 것을 우려한다면 다른 폴더 만들어서 저장해두기

```bash
$ git clone https://github.com/suenk00/TIL.git
# 단, 바탕화면에 TIL이 없어야 함.
# 이 경우 완전히 새로운 환경이되 지금까지 한 작업들을 불러와서 똑같이 할 수 있음.
```

- pull: 다른 곳에서 작업한 내용들을 집에서 새로운 파일로 작업해 원격 저장소에 push하는 것. git에 대한 정보를 이미 가지고 있을 때 사용하는 것. 원격저장소가 구버전, 내가 신버전이면 바뀌는 것 없음. 

```bash
$ 
```





