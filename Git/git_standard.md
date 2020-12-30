# Git 명령어

## 기본 명령어

|                    명령어                     |                      설명                       |
| :-------------------------------------------: | :---------------------------------------------: |
|                  `git init`                   |                  git 폴더 지정                  |
|                 `git status`                  | git 상태표시 (현재 git 상태 - commit or staged) |
|               `git add <file>`                |     file staged (파일을 스테이지에 업로드)      |
|              `git commit -m 'x'`              |     staged 된 file을 커밋 (x는 커밋된 이름)     |
| `git config — global user.name “user_name ”`  |             git 계정 name 변경하기              |
| `git config — global user.email “user_email”` |              git 계정Mail변경하기               |
|                   `git log`                   |          commit history 를 보는 명령어          |
|          `git remote add ??? 'url'`           |           url 등록 (???은 url의 가명)           |
|               `git push ??? x`                |     commit된 내용을 연결된 x 브랜치로 전송      |
|               `git pull ??? x`                |       x의 자료를 로컬 저장소로 불러온다.        |

---

## 중급 명령어

|                   명령어                   |                설명                |
| :----------------------------------------: | :--------------------------------: |
|                `git branch`                |          현재 branch 조회          |
|               `git branch x`               |       x란 branch를 만들어줌        |
|               `git switch x`               |         x란 branch로 이동          |
| `git log --pretty=oneline --abbrev-commit` |            로그 간략화             |
| `git log --pretty=format:"%h %s" --graph`  |           로그 그래프화            |
|             `git branch -d x`              | x란 브랜치 삭제(중요내용시 물어봄) |
|             `git branch -D x`              |    x란 브랜치 삭제(무조건 삭제)    |
|              `git switch <x>`              |       x란 branch로 head 변경       |
|            `git switch -c <x>`             |   x란 branch를 생성후 head 변경    |
|         `git checkout <commit-Id>`         |    해당 커밋-id의 상태로 되돌림    |
|                `git merge`                 |   브랜치를 현재 브랜치로 합친다.   |
|                                            |                                    |

## 알아두면 좋은 상식들

* remote repo : 원격 저장소 (인터넷이나 네트워크에 있는 원격 저장소, 즉 이게 있어야 다른 사                      람과 협업이 가능하다)
* HEAD : Git에 있는 특수한 포인터, 지금 작업하고 있는 로컬 브랜치를 가르킨다.
* fast forward : head를 merge하는게 아니라 앞으로 땡겨오는것. (즉 branch를 합치는게 아니라 최신 브랜치로 head를 옮겨오는 작업으로 볼 수 있다.)
* conflict : 병렬로 작업함에 따라 merge할 경우 서로 자료가 충돌하는경우.

* .gitignore 파일에 쓸모없는 파일 목록 추가는 https://gitignore.io 사이트를 참조하면된다.
* 다른 컴퓨터에서 TIL 관리할땐 clone 주소를 받아와서 내용을 추가하면 된다.
* master 브랜치에는 절대 push나 pull을 하지 않는다. (협력할때)

## 프로젝트 시작할 때 알아두면 좋은것들

project 생성할 때,

1. touch .gitignore
2. touch README.md
3. git init => add => commit 순으로 진행하면 된다.