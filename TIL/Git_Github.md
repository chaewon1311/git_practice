# Git
Git은 Working Directory → Staging Area → Repository 의 과정으로 버전 관리를 수행합니다.

- `Working Directory (= Working Tree)` : 사용자의 일반적인 작업이 일어나는 곳   
- `Staging Area (= Index)` : 커밋을 위한 파일 및 폴더가 추가되는 곳
- `Repository` : staging area에 있던 파일 및 폴더의 변경사항(커밋)을 저장하는 곳   

## git init
현재 작업 중인 디렉토리를 Git으로 관리한다는 명령어

```
$ git init
Initialized empty Git repository in C:/Users/kyle/git-practice/.git/
```

#### 주의사항
- 이미 Git 저장소인 폴더 내에 또 다른 Git 저장소를 만들지 않는다.
- 홈 디렉토리에서 git init을 하지 않는다.

## git status
Working Directory와 Staging Area에 있는 **파일의 현재 상태**를 알려주는 명령어


| `Untracked`  |  Git이 관리하지 않는 파일, Staging Area에 올라가지 않는 파일. |
|---|---|
|  `Tracked` |  Git이 관리하는 파일 |
|  `Unmodified` |  최신 상태 |
| `Modified`  |  수정되었지만 아직 Staging Area에는 반영하지 않은 상태 |
|  `Staged` | Staging Area에 올라간 상태  |

## git add
- Working Directory에 있는 파일을 Staging Area로 올리는 명령어
- Git이 해당 파일을 추적(관리)할 수 있도록 만든다.

```
# 특정 파일
$ git add a.txt(파일명)

# 특정 폴더
$ git add my_folder/(폴더명)

# 현재 디렉토리에 속한 파일/폴더 전부
$ git add .
```

## git commit
Staging Area에 올라온 파일의 변경 사항을 하나의 버전(커밋)으로 저장하는 명령어

```
$ git commit 파일명 -m "변동 사항, 코멘트 등"
[main (root-commit) c02659f] first commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 a.txt
```

## git log
커밋의 내역(ID, 작성자, 시간, 메세지 등)을 조회할 수 있는 명령어

- `--oneline` : 한 줄로 축약해서 보여줍니다.    
- `--graph` : 브랜치와 머지 내역을 그래프로 보여줍니다.   
- `--all` : 현재 브랜치를 포함한 모든 브랜치의 내역을 보여줍니다.   
- `--reverse` : 커밋 내역의 순서를 반대로 보여줍니다. (최신이 가장 아래)   
- `-p` : 파일의 변경 내용도 같이 보여줍니다.   
- `-2` : 원하는 갯수 만큼의 내역을 보여줍니다. (2 말고 임의의 숫자 사용 가능)

![Git image](https://files.slack.com/files-pri/T0A3H2DAV7A-F0A3ZTHCFM3/_______________________________2025-12-17______________4.39.01.png)

# Github
>Git과 연동하는 로컬 저장소로, 로컬 저장소과 연동하여 자유롭게 파일 업로드가 가능하다.

## git remote
로컬 저장소에 원격 저장소를 등록, 조회, 삭제할 수 있는 명령어

1. 등록  
   `git remote add <이름> <주소>` 형식으로 작성합니다.
   ```
   $ git remote add origin https://github.com/edukyle/TIL.git

    [풀이]
    git 명령어를 작성할건데, remote(원격 저장소)에 add(추가) 한다.
    origin이라는 이름으로 https://github.com/edukyle/TIL.git라는 주소의 원격 저장소를 등록한다.
   ```
2. 조회
   `git remote -v` 로 작성합니다.
   ```
   $ git remote -v
    origin  https://github.com/edukyle/TIL.git (fetch)
    origin  https://github.com/edukyle/TIL.git (push)

    add를 이용해 추가했던 원격 저장소의 이름과 주소가 출력됩니다.
    ```

3. 삭제  
    - `git remote rm <이름>` 혹은 `git remote remove <이름>` 으로 작성합니다.
    - 로컬과 원격 저장소의 연결을 끊는 것이지, 원격 저장소 자체를 삭제하는 게 아님.
    ```
    - $ git remote rm origin
    $ git remote remove origin

    [풀이]
    git 명령어를 작성할건데, remote(원격 저장소)와의 연결을 rm(remove, 삭제) 한다.
    그 원격 저장소의 이름은 origin이다.
    ```

 ## 원격 저장소(Github)에 업로드

1.로컬 저장소에서 커밋 생성
```
현재 상태 확인

$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        day1.md

nothing added to commit but untracked files present (use "git add" to track)
```

2. git push
- 로컬 저장소의 커밋을 원격 저장소에 업로드하는 명령어
- `git push <저장소 이름> <브랜치 이름>` 형식으로 작성합니다.
- `-u` 옵션을 사용하면, 두 번째 커밋부터는 `저장소 이름, 브랜치 이름`을 생략 가능합니다.
  ```
  $ git push origin main

    [풀이]
    git 명령어를 사용할건데, origin이라는 이름의 원격 저장소의 main 브랜치에 push 한다.

    ------------------------------------------------

    $ git push -u origin main
    이후에는 $ git push 라고만 작성해도 push가 됩니다.
    ```

    