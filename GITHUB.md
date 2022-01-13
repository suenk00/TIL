## REVIEW

# Github

### 회원가입

### 설정 변경

- main 브랜치를 master 브랜치로 기본값 수정

---

### 원격 저장소와 로컬 저장소 연결 방법

#### Repository 생성

- git remote
- git push

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

#### gitignore

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





