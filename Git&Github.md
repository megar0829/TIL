# Git bash

>### 사용환경
- GUI (graphic user interface) : 그래픽 기반 사용환경
- CLI (command line interface) : 명령어 기반 사용환경
  - CLI 명령어
  ```bash
    - ls : 현재 폴더에 있는 파일을 보여줌 (목록)
    - mkdir 폴더이름 : 폴더 생성 (디렉토리 생성)
    - cd 폴더이름 : 폴더 이동 (디렉토리 이동)
    - cd . : 현재 폴더로 이동 (현재 디렉토리)
    - cd .. : 상위 폴더로 이동 (상위 디렉토리)
    - touch 파일명 : 새로운 파일 생성
    - rm 파일명 : 파일 삭제 (remove)
    - rm -r 폴더명 : 폴더 삭제
    ```
>### Git 과 Github
- git : 소스코드를 관리하는 도구 
- github : 온라인에서 git을 사용하는 도구
>### Git 이란
- git : 분산 버전 관리 시스템
- 버전(커밋) : 컴퓨터 소프트웨어의 특정 상태

- **버전 기록** 
  1. 작업을 하고(파일 생성) : 1통
  2. 변경된 파일을 모아(add) : 2통
  3. 버전으로 남긴다.(commit) : 3통

    `ex)`

    (1통) Untracked files : 트래킹되지 않은 파일들
    (상황) 1.txt 를 만들었지만, add를 하지 않음

    (1통) Changes not staged for commit : 커밋을 위해 staged가 아닌 변경사항들
    (상황) 커밋된적 있는 보고서.txt 파일을 수정한 상태

    (2통) Changes to be committed : 커밋될 변경사항들
    (상황) 보고서.txt 만들고 add 함.

    `nothing to commit, working tree clean => 1통, 2통 비어있음!`

- Status 로 확인할 수 있는 파일의 상태
  - Tracked : 이전부터 버전으로 관리되고 있는 파일 상태
	  - Unmodified : git status에 나타나지 않음(X) => 현재 폴더에 없는 경우
	  - Modified : Changes not staged for commit (1통)
	  - Staged : Changes to be committed (2통)
  - Untracked : 버전으로 관리된적 없는 파일 상태 (파일을 새로 만든 경우)

- add, commit 취소
  - add 취소
    1통에 있는 파일을 1통에서 없앤다 (가장 최신 상태의 파일로 돌아간다)
    ```bash
    git restore '파일명'
    ```
  - commit 취소
    add 해서 2통에 저장한 파일을 다시 1통으로 보낸다
    stage 된 파일을 다시 untracked 상태로 변경
    ```bash
    git restore --staged '파일명'
    ```  
  - 커밋 메세지 수정
    `커밋의 해시값이 달라지기 때문에 안하는게 좋다`
    ```bash
    git commit --amend
    ```

>### 버전 기록 요약
  1. 파일을 작성(작업) : 1통 
  2. git add 로 Staging Area에 모으기 : 2통 
  3. git commit -m '메모' 로 모아 놓은 파일들을 커밋 : 3통
  ```bash
  git add 파일명
  git commit -m '커밋할 내용'
  ```
### git : 분산버전관리 시스템
1. 파일을 생성(Create), 수정(Update), 삭제(Delete) 한다. 
    => 1통에 저장

2. 1통에 있는 파일을 git add 를 통해서 2통으로 이동한다.(가상 공간에 저장한다.) 
    => 2통에 저장

3. 2통에 있는 파일을 git commit 을 이용하여 버전으로 기록한다.
    => 3통에 저장
---

## 2022-12-28

# Github

>### 원격저장소(Remote Repository) 활용  => github

- 로컬 저장소의 버전을 원격저장소로 보낸다.
```bash
git push
```

- 원격저장소의 버전을 로컬 저장소로 가져온다.
```bash
git pull
```

- 원격 저장소의 정보 확인
```bash
git remote -v
```

- 로컬 저장소에 원격 저장소 정보 설정하기
```bash
 git remote add origin '저장소' '주소 URL'
(원격저장소)(추가해)(Origin 으로)
```

- 로컬 저장소에 지정된 원격 저장소 삭제
```bash
git remote rm '원격저장소'
```

- 원격 저장소로 로컬 저장소 변경 사항(커밋)을 올림 (Push)
```bash
git push origin master
```
- 원격 저장소로부터 변경된 내역을 받아와서 이력을 병합함 
=> 원격 저장소가 로컬보다 더 많은 정보를 가지고 있을경우 파일을 가져올 수있음
```bash
git pull origin master
```

- 원격 저장소 복제 (바탕화면에 git bash를 열고 코드 입력)
```bash
git clone URL 
```

`파일을 작성하고 add 까지만 해도 push는 안된다. 파일을 올리는 것이 아니라 커밋을 올리는것이다. 꼭 커밋까지 하기!!`

- ### gitignore 
  - 버전관리랑 상관없는 파일들을 무시하다.
  - .gitignore 라는 파일을 만든 후 함께 관리하지 않을 파일이나 폴더, 파일형식 등을 제외할 수 있다.
  - ex) 파일명, 폴더명/, *.확장자

`이전에 커밋된 파일은 무시할 수 없으니 처음부터 .gitignore를 만들어서 설정하자 commit history 는  되도록이면 바꾸지 말자 `

- 브랜치 생성
```bash
git branch {branch name}
```

- 브랜치 이동
```bash
git checkout {branch name}
```

- 브랜치 생성 및 이동
```bash
git checkout-b {branch name}
```

- 브랜치 목록
```bash
git branch
```

- 브랜치 삭제
```bash
git branch -d {branch name}
```

- ### Local (혼자서 작업)
```
1. 브런치 만들고
2. 작업
3. 커밋
4. 로컬에서 마스터 이동 병합
```
- ### github flow (실제 협업)
```
1. 브런치 만들고
2. 작업
3. 커밋
4. github으로 브랜치 push
5. pull request 생성  pull을 요청(이거좀 가져가줘)
6. 코드 리뷰 후 merge  
```