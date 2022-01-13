# branch

## git branch 명령어

- 브랜치 `생성, 삭제, 조회`

```bash
# 브랜치 조회
$ git branch

# 원격 저장소의 브랜치 목록 확인
$ git branch -r

# 브랜치 생성
$ git branch {branch name}

# 브랜치 지우기
## 병합된(수정내역을 합치고 난 후에 삭제 가능)
$ git branch -d {branch name}
## (주의) 병합되지 않은 브랜치 강제 삭제
$ git branch -D {branch name}


```



### git switch

- 현재 브랜치에서 다른 브랜치로 `HEAD`를 이동시키는 명령어

- `HEAD`는 현재 브랜치를 가리키는 포인터

  ```BASH
  # 다른 브랜치로 이동
  $ git switch {다른 브랜치 이름}
  
  # 브랜치를 새로 생성하고 동시에 이동
  $ git switch -c {다른 브랜치 이름}
  ```

- **주의 사항**

​		git switch 하기 전에 commit !!!!

		$ git switch -c ssafy

교수님 이렇게 하고 나서 ssafy가 master가 됩니당..의 상황이 만들어지면 모든 브랜치 다 지우고 swtich -c 하면 원래 상태로 복구 가능



### merge

```
master에 dev 내용 가지고 오기 -> 'fast-forward(빨리감기)'확인
** fast-forward: dev를 분화시킨 master에는 변화가 없을 때 branch의 버전에 빨리감기 함.
이 경우 dev 브랜치를 지워도 기존의 dev branch에 만든 내용이 master에 남고 사라지지 않음
```

```bash
# master에 변동사항이 생긴 경우 -> 반드시 add . --> commit 하기!!!
$ touch login.txt
$ git switch master
$ touch master.txt

$ git merge login
`: wq` 만약 이게 아니라 `a` or `i`누르면 #"--끼워넣기--" 실행. 새로운 버전이 생성됨.

## 어떤 버전에서 분화되어 나왔는지 확인하려면 graph 그리기
$ git log --oneline --graph
*   1a6f7d6 (HEAD -> master) Merge branch 'login'
|\
| * 923444d (login) login create
* | 95605b8 create master
|/
* dcf746d first dev
* 55bd040 (origin/master, origin/HEAD) branch 생성 후 재시작
* 8fb29da workshop
* 4145490 과제 제출
* d9a4e47 modified github
* 09d22bd create github
* 0b9bc9d Modified GIT
* c5e66e8 20220112
* 0e6ffd2 second commit
* d48f1b5 fist commit
```

** `.` 현재 위치 의미. 전부 아님!!! 

ex `add .`:  전부 저장 아니고 현재 위치 저장임

