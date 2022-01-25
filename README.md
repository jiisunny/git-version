# git-version 💻

Git 버전관리 개념 정리
<br /><br />

## 1. 버전 생성과 업로드의 이해
<br />

### [Git 기본 Setting]

Git을 처음 사용할 때 기본 설정

```bash
$ git --version
$ git init
$ git config -- global core.autocrlf input
$ git config --global user.name ‘GitHub 닉네임’
$ git config --global user.email ‘GitHub 이메일’
$ git config --global --list
```

- `git --version` : git 버전 확인
- `git init` : 버전관리를 하겠다고 선언
- `git config --global core.autocrlf input` : ios에서는 `input`, window 에서는 `true`를 입력한다.
- `git config --global user.name ‘GitHub 닉네임’` : 사용자 이름 추가
- `git config --global user.email ‘GitHub 이메일’` : 사용자 이메일 추가
- `git config --global --list` : 등록한 정보 확인

### [Git 버전관리]

작업 후 git 으로 버전을 관리할 때 사용

```bash
$ git status
$ git add .
$ git status
$ git commit -m 'Start project'
$ git log
```

- `git status` : 프로젝트 버전관리 상태 확인 (file : RED)
- `git add .` : 버전 관리 등록
`git status` : 재확인 (file : GREEN)
- `git commit -m 'Start project'` : 버전 생성
- `git log` : commit 한 버전 확인

### [GitHub에 프로젝트 업로드 하기]

버전 관리한 프로젝트를 GitHub 저장소로 업로드 하기

1. GitHub에 저장소 생성하기
> GitHub -> Repositories -> New -> 이름지정 -> (설명 기재) -> 공개/비공개 설정 -> Create repository
2. 저장소 링크 복사
3. VsCode - Terminal

```bash
$ git remote add origin + [복사한 저장소 링크]
$ git push origin master
$ git push origin master
```

- `git remote add origin + [복사한 저장소 링크]` : 원격 GitHub 저장소에 생성한다
- `git push origin master` : Git 명령어를 통해 원격저장소에 프로젝트 업로드
- `git push origin master` : 제대로 업로드 되었는지 재확인

4. GitHub 사이트 새로고침
5. 업로드 완료
<br /><br />

## 2. Netlify 지속적인 배포
<br />

### [Netlify 배포]
1. Netlify 사이트 GitHub 으로 로그인
2. 우측, New site from Git
3. Continuous Deployment - GitHub
4. Authorize Netlify
5. GitHub - All repositories - install
6. Netlify 사이트 - 저장소
7. Owner, Branch to Deploy(master가 대부분의 경우임) - Deploy site
8. 주소생성 완료
<br /><br />

## 3. 수정사항 버전 생성 - Commit
<br />

### [수정 후 Commit]

프로젝트에서 수정사항이 생겼을 때

1. VsCode - Terminal

```bash
$ git status
$ git add .
$ git status
$ git commit -m '뱃지 이미지 수정'
$ git log
```

- `git status` : 수정내역 확인 (file : RED)
- `git add .` : 버전 관리 등록
`git status` : 재확인 (file : GREEN)
- `git commit -m '뱃지 이미지 수정'` : 버전 생성
- `git log` : commit 한 버전 확인

2. 프로젝트에서 수정 후 GitGub에 업로드
3. VsCode - Terminal

```bash
$ git push origin master
```

- `git push origin master` : `origin`은 원격저장소의 별칭이다.

4. 업로드 완료
<br /><br />

## 4. 로그인 Branch
<br />

### [Branch 생성]

1. VsCode - Terminal

```bash
$ git branch
$ git branch -a
$ git branch signin
$ git branch
$ git checkout signing
```

- `git branch` : branch 목록이 나타난다
- `git branch -a` : 원격저장소의 branch 목록 확인가능
- `git branch signin` : Signin branch 생성
- `git branch` : branch 조회
- `git checkout signing` : signin으로 branch 변경

2. Signin 페이지 작업
3. 수정사항 업로드, VsCode - Terminal

```bash
$ git status
$ git add .
$ git status
$ git commit -m '로그인 페이지 시작하기'
$ git log
```

- `git status` : 수정내역 확인 (file : RED)
- `git add .` : 버전 관리 등록
`git status` : 재확인 (file : GREEN)
- `git commit -m 'Start project'` : 버전 생성
- `git log` : commit 한 버전 확인

4. Signin -> master로 branch 이동

```bash
$ git checkout master
```

- `git checkout master` : Signin에서 master로 branch 이동
<br /><br />

## 5. 로그인 Branch 병합 (pull request)
<br />

### [로그인 Branch 업로드]

1. Git 버전 관리

```bash
$ git status
$ git add .
$ git status
$ git commit -m '로그인 페이지 완성'
$ git log
```

- `git status` : 수정내역 확인 (file : RED)
- `git add .` : 버전 관리 등록
`git status` : 재확인 (file : GREEN)
- `git commit -m 'Start project'` : 버전 생성
- `git log` : commit 한 버전 확인

2. 원격 저장소에 push

```bash
$ git push origin signin
```

- `git push origin signin` : signin branch를 업로드 한다.

### [병합하기]

1. GitHub 상단 - Pull requests
2. 우측 New pull request
3. Base:master <- compare:signin 으로 설정 (Able to merge)
4. 우측 Create pull request
5. Comment 창에서 Create pull request
6. 페이지 하단 Merge pull request - confirm merge

### [Netlify 페이지 확인]

1. Deploys 메뉴 선택
2. 아래 merged 내용 확인 가능
<br /><br />

## 6. 프로젝트 복제 (Clone)
<br />

1. GitHub 로그인 - Your repositories - Starbucks 선택
2. Code 버튼 - Link Copy
3. VsCode - Terminal

```bash
$ ls(ios)
$ dir(window)
$ cd desk + [TAB] + [ENTER]
$ Ls + [ENTER]
$ cd ..
$ cd desk + [TAB] + [ENTER]
$ git clone + [GitHub에서 복사한 링크]
$ ls
```

- `ls`(ios) : 많은 파일명들이 보임<br />
ios에서는 `ls`, window 에서는 `dir`를 입력한다.
- `cd desk + [TAB] + [ENTER]` : 데스크탑으로 이동, `cd`는 `change directory`
- `ls + [ENTER]` : Desktop의 파일명들이 보임
- `cd ..` : Desktop 밖으로 이동
- `cd desk + [TAB] + [ENTER]`: 다시 데스크탑으로 이동
- `git clone + [GitHub에서 복사한 Link]` : GitHub 저장소 파일이 복제된다
- `ls` : Starbucks 파일 생성 확인 가능함

4. 복제한 파일 가져오기
5. VsCode - Terminal

```bash
$ cd desk + [TAB] + [ENTER]
$ cd Starbucks + [TAB] + [ENTER
$ code .
$ code . -r
```

- `cd desk + [TAB] + [ENTER]` : 데스크탑으로 이동, `cd`는 `change directory`
- `cd Starbucks + [TAB] + [ENTER]` : Starbucks 폴더로 접근
- `code .` : Starbucks 폴더가 새창으로 열린다
- `code . -r` : Starbucks 폴더가 기존창에서 열린다
<br /><br />

## 7. 버전 되돌리기 (Reset)
<br />

### [프로젝트 추가 작업]

1. A project 작업
2. VsCode - Terminal 실행 (버전 1 생성)

```bash
$ git init
$ git status
$ git add .
$ git status
$ git commit -m ‘1’
$ git log
```

3. A project 수정
4. VsCode - Terminal 실행 (버전 2 생성)

```bash
$ git status
$ git add .
$ git status
$ git commit -m ‘2’
$ git log
```

5. A project 수정
6. VsCode - Terminal 실행 (버전 3 생성)

```bash
$ git status
$ git add .
$ git status
$ git commit -m ‘3’
$ git log
```

### [버전 되돌리기]

7. 버전 2로 돌아가기

```bash
$ git reset --hard HEAD~1
```

- `git reset --hard HEAD~1` : 최신버전(HEAD)에서 뒤로 1버전 되돌림

8. 다시 버전 3으로 돌아가기

```bash
$ git reset --hard ORIG HEAD
```

- `git reset --hard ORIG HEAD` : `ORIG`는 `기존`이라는 뜻

9. 버전 1로 돌아가기

```bash
$ git reset --hard HEAD~2
```

- `git reset --hard HEAD~2` : 최신버전(HEAD)에서 뒤로 2버전 되돌림

10. 다시 버전 3로 돌아가기

```bash
$ Git reset --hard ORIG HEAD
```
<br /><br />

## 8. Branch 만들기
<br />

1. branch 생성
2. VsCode - Terminal

```bash
$ git branch purple
$ git branch
$ git checkout purple
```

- `git branch purple` : purple branch 생성
- `git branch` : branch 목록 확인 가능
- `git checkout purple` : purple branch로 이동

3. Purple project 내용 작성 후 버전 생성

```bash
$ git status
$ git add .
$ git status
$ git commit -m ‘purple/1’
$ git log
```

4. Master branch로 이동

```bash
$ git checkout master
```

5. Master branch 상태에서 html 내용 수정 (버전 4 생성)

```bash
$ git add .
$ git commit -m ‘4’
$ git  log
```

6. GitHub 저장소에 master branch 업로드
- Repositories - New - 저장소 이름 입력 - Create repository
- 저장소 주소 복사
7. VsCode - Terminal

```bash
$ git remote add origin + [복사한 링크]
$ git push origin master
```

- `git remote add origin + [복사한 링크]` : 원격저장소 주소 등록
- `git push origin master` : 저장소에 push

8. GitHub 저장소에 purple branch 업로드

```bash
$ git checkout purple
$ Git push origin purple
```

- `git checkout purple` : purple branch 로 이동
<br /><br />

## 9. 다른 환경에서 시작하기
<br />

1. GitHub - repositories - 저장소 링크 복사
2. VsCode - Terminal

```bash
$ ls(ios)
$ dir(window)
$ cd desk + [TAB] + [ENTER] : 바탕화면으로 경로 바꿈
$ git clone : 원격저장소 파일 복제
$ cd git- + [TAB]
$ code . -r : VsCode 현재창에서 파일 열림
```

- `ls`(ios) : 많은 파일명들이 보임<br />
ios에서는 `ls`, window 에서는 `dir`를 입력한다.
- `cd desk + [TAB] + [ENTER]` : 바탕화면으로 경로 바꿈
- `git clone` : 원격저장소 파일 복제
- `code . -r` : VsCode 현재창에서 파일 열림

3. 복제한 폴더 VsCode에서 열림

```bash
$ git branch
$ git branch -r
$ git checkout -t origin/purple
$ git branch
```

- `git branch -r` : 다른 branch 가져오기
- `git checkout -t origin/purple` : 원격저장소의 purple branch 가져옴
- `git branch` : master branch, purple branch 둘다 보임

4. 가져온 branch가 필요없어서 지울 때

```bash
$ git checkout master
$ git branch -d purple
```

- `git branch -d purple` : purple branch 삭제

5. Yellow branch 생성하기

```bash
$ git branch yellow
$ git branch
$ git checkout yellow
```

- `git branch yellow` : yellow branch 생성
- `git branch` : master, yellow branch 조회가능
- `git checkout yellow` : yellow branch로 이동

6. Yellow branch 삭제

```bash
$ git checkout master
$ git branch -d yellow
$ git branch
```

- `git checkout master` : master branch 로 이동
- `git branch -d yellow` : yellow branch 제거
- `git branch` : branch 목록 확인 (master branch만 나옴)

7. 생성과 동시에 해당 branch로 이동하기

```bash
$ git checkout -b yellow
```

- `git checkout -b yellow` : yellow branch 생성&이동

8. Yellow branch push 하기

```bash
$ git push origin yellow
```

9. GitHub 에서 프로젝트 확인가능
<br /><br />

## 10. 버전의 충돌 Conflict, 로컬 병합 Merge
<br />

### [새로운 PC에서 프로젝트 진행 (충돌상황) ]

1. PC에는 XYZ 수정 전 master로 버전 1 프로젝트가 열려있다
2. 원격저장소에 XYZ 내용이 있는 줄 모르고 버전 1에서 ABC로 내용 수정
3. 수정한 내용을 push함

```bash
$ git status
$ git add .
$ git commit -m ‘ABC’
```

4. 저장소에 push 시도, pull request로 병합시도

```bash
$ git push origin master
```

- `git push origin master` : rejected push로 거부됨 (저장소 내용과 로컬환경 내용이 다르기 때문이다)

5. 해결방법 1

> local 환경 버전 reset

```bash
$ git reset --hard HEAD~1
```

6. 해결방법 2 

> 수정한 내용을 새로운 버전으로 다시 만든다

```bash
$ git pull origin master
```

- `git pull origin master` : 원격저장소에서 local 환경으로 가져온다
- conflict 충돌 메세지 나옴
- html에 메세지가 뜬다 (내용선택 가능) : 사용하지 않을 코드를 지워주면 반영된다

7. 해결방법 3

> 저장소(XYZ), local(ABC) 내용을 섞어 새로운 버전(ABYZ)으로 만든다

```bash
$ git pull origin master
```

- `git pull origin master` : 원격저장소에서 local 환경으로 가져온다
- conflict 충돌 메세지 나옴
- html에 메세지가 뜬다 (원하는 내용으로 수정)
- 새로운 버전 생성

```bash
$ git status
$ git add .
$ git status
$ git commit -m ‘ABYZ’
$ git push origin master
```

- `git commit -m ‘ABYZ’` : 버전 생성
- `git push origin master` : 원격저장소로 업로드

8. Push 완료
