># 명령어 정리
---

## - CLI 명령어

- 현재 폴더에 있는 파일 목록 보기
```bash
ls  (list)
```

- 폴더 생성
```bash
mkdir 폴더이름  (make directory)
```

- 해당 폴더로 이동
```bash
cd 폴더이름
```

- 현재 폴더로 이동
```bash
cd .
```

- 상위 폴더로 이동
```bash
cd ..
```

- 새로운 파일 생성
```bash
touch 파일명.확장자
```

- 해당 파일 삭제
```bash
rm 파일명.확장자
```

- 해당 폴더 삭제
```bash
rm -r 폴더명
```
---

## - Git 
### (1) 저장소 만들기

```bash
$ git init
``` 

### (2) 작업 완료 후 status
* 현재 상태 확인

```bash
$ git status
```

### (3) add
* 작업한 파일을 Staging Area 에 저장
```bash
$ git add .
```

### (4) commit
* '작업한 내용 요약' 을 커밋하여 버전으로 저장

```bash
$ git commit -m '작업한 내용 요약'
```
### (5) log
* 커밋한 버전들을 확인
```bash
$ git log
```
---
## - Github

* 원격 저장소의 정보 확인
```bash
git remote -v 
```

* 로컬 저장소에 원격 저장소 정보 설정 (일반적으로 origin)
```bash
git remote add <원격저장소> URL

git remote add origin URL
(원격저장소)(추가해)(Origin 으로)
```

* 원격 저장소 삭제
```bash
git remote rm <원격저장소> 

git remote origin
```

* 로컬 저장소의 버전을 원격 저장소로 보내기
```bash
git push <원격저장소> <브랜치>

git push origin master
```

* 원격 저장소의 버전을 로컬 저장소로 가져오기
```bash
git pull <원격저장소> <브랜치>

git pull origin master
```

* 원격 저장소 복제 (바탕화면에서 git bash에 입력)
```bash
git clone URL 
```