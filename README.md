# git-version ๐ป

Git ๋ฒ์ ๊ด๋ฆฌ ๊ฐ๋ ์ ๋ฆฌ
<br /><br />

## 1. ๋ฒ์  ์์ฑ๊ณผ ์๋ก๋์ ์ดํด
<br />

### [Git ๊ธฐ๋ณธ Setting]

Git์ ์ฒ์ ์ฌ์ฉํ  ๋ ๊ธฐ๋ณธ ์ค์ 

```bash
$ git --version
$ git init
$ git config -- global core.autocrlf input
$ git config --global user.name โGitHub ๋๋ค์โ
$ git config --global user.email โGitHub ์ด๋ฉ์ผโ
$ git config --global --list
```

- `git --version` : git ๋ฒ์  ํ์ธ
- `git init` : ๋ฒ์ ๊ด๋ฆฌ๋ฅผ ํ๊ฒ ๋ค๊ณ  ์ ์ธ
- `git config --global core.autocrlf input` : ios์์๋ `input`, window ์์๋ `true`๋ฅผ ์๋ ฅํ๋ค.
- `git config --global user.name โGitHub ๋๋ค์โ` : ์ฌ์ฉ์ ์ด๋ฆ ์ถ๊ฐ
- `git config --global user.email โGitHub ์ด๋ฉ์ผโ` : ์ฌ์ฉ์ ์ด๋ฉ์ผ ์ถ๊ฐ
- `git config --global --list` : ๋ฑ๋กํ ์ ๋ณด ํ์ธ

### [Git ๋ฒ์ ๊ด๋ฆฌ]

์์ ํ git ์ผ๋ก ๋ฒ์ ์ ๊ด๋ฆฌํ  ๋ ์ฌ์ฉ

```bash
$ git status
$ git add .
$ git status
$ git commit -m 'Start project'
$ git log
```

- `git status` : ํ๋ก์ ํธ ๋ฒ์ ๊ด๋ฆฌ ์ํ ํ์ธ (file : RED)
- `git add .` : ๋ฒ์  ๊ด๋ฆฌ ๋ฑ๋ก
`git status` : ์ฌํ์ธ (file : GREEN)
- `git commit -m 'Start project'` : ๋ฒ์  ์์ฑ
- `git log` : commit ํ ๋ฒ์  ํ์ธ

### [GitHub์ ํ๋ก์ ํธ ์๋ก๋ ํ๊ธฐ]

๋ฒ์  ๊ด๋ฆฌํ ํ๋ก์ ํธ๋ฅผ GitHub ์ ์ฅ์๋ก ์๋ก๋ ํ๊ธฐ

1. GitHub์ ์ ์ฅ์ ์์ฑํ๊ธฐ
> GitHub -> Repositories -> New -> ์ด๋ฆ์ง์  -> (์ค๋ช ๊ธฐ์ฌ) -> ๊ณต๊ฐ/๋น๊ณต๊ฐ ์ค์  -> Create repository
2. ์ ์ฅ์ ๋งํฌ ๋ณต์ฌ
3. VsCode - Terminal

```bash
$ git remote add origin + [๋ณต์ฌํ ์ ์ฅ์ ๋งํฌ]
$ git push origin master
$ git push origin master
```

- `git remote add origin + [๋ณต์ฌํ ์ ์ฅ์ ๋งํฌ]` : ์๊ฒฉ GitHub ์ ์ฅ์์ ์์ฑํ๋ค
- `git push origin master` : Git ๋ช๋ น์ด๋ฅผ ํตํด ์๊ฒฉ์ ์ฅ์์ ํ๋ก์ ํธ ์๋ก๋
- `git push origin master` : ์ ๋๋ก ์๋ก๋ ๋์๋์ง ์ฌํ์ธ

4. GitHub ์ฌ์ดํธ ์๋ก๊ณ ์นจ
5. ์๋ก๋ ์๋ฃ
<br /><br />

## 2. Netlify ์ง์์ ์ธ ๋ฐฐํฌ
<br />

### [Netlify ๋ฐฐํฌ]
1. Netlify ์ฌ์ดํธ GitHub ์ผ๋ก ๋ก๊ทธ์ธ
2. ์ฐ์ธก, New site from Git
3. Continuous Deployment - GitHub
4. Authorize Netlify
5. GitHub - All repositories - install
6. Netlify ์ฌ์ดํธ - ์ ์ฅ์
7. Owner, Branch to Deploy(master๊ฐ ๋๋ถ๋ถ์ ๊ฒฝ์ฐ์) - Deploy site
8. ์ฃผ์์์ฑ ์๋ฃ
<br /><br />

## 3. ์์ ์ฌํญ ๋ฒ์  ์์ฑ - Commit
<br />

### [์์  ํ Commit]

ํ๋ก์ ํธ์์ ์์ ์ฌํญ์ด ์๊ฒผ์ ๋

1. VsCode - Terminal

```bash
$ git status
$ git add .
$ git status
$ git commit -m '๋ฑ์ง ์ด๋ฏธ์ง ์์ '
$ git log
```

- `git status` : ์์ ๋ด์ญ ํ์ธ (file : RED)
- `git add .` : ๋ฒ์  ๊ด๋ฆฌ ๋ฑ๋ก
`git status` : ์ฌํ์ธ (file : GREEN)
- `git commit -m '๋ฑ์ง ์ด๋ฏธ์ง ์์ '` : ๋ฒ์  ์์ฑ
- `git log` : commit ํ ๋ฒ์  ํ์ธ

2. ํ๋ก์ ํธ์์ ์์  ํ GitGub์ ์๋ก๋
3. VsCode - Terminal

```bash
$ git push origin master
```

- `git push origin master` : `origin`์ ์๊ฒฉ์ ์ฅ์์ ๋ณ์นญ์ด๋ค.

4. ์๋ก๋ ์๋ฃ
<br /><br />

## 4. ๋ก๊ทธ์ธ Branch
<br />

### [Branch ์์ฑ]

1. VsCode - Terminal

```bash
$ git branch
$ git branch -a
$ git branch signin
$ git branch
$ git checkout signing
```

- `git branch` : branch ๋ชฉ๋ก์ด ๋ํ๋๋ค
- `git branch -a` : ์๊ฒฉ์ ์ฅ์์ branch ๋ชฉ๋ก ํ์ธ๊ฐ๋ฅ
- `git branch signin` : Signin branch ์์ฑ
- `git branch` : branch ์กฐํ
- `git checkout signing` : signin์ผ๋ก branch ๋ณ๊ฒฝ

2. Signin ํ์ด์ง ์์
3. ์์ ์ฌํญ ์๋ก๋, VsCode - Terminal

```bash
$ git status
$ git add .
$ git status
$ git commit -m '๋ก๊ทธ์ธ ํ์ด์ง ์์ํ๊ธฐ'
$ git log
```

- `git status` : ์์ ๋ด์ญ ํ์ธ (file : RED)
- `git add .` : ๋ฒ์  ๊ด๋ฆฌ ๋ฑ๋ก
`git status` : ์ฌํ์ธ (file : GREEN)
- `git commit -m 'Start project'` : ๋ฒ์  ์์ฑ
- `git log` : commit ํ ๋ฒ์  ํ์ธ

4. Signin -> master๋ก branch ์ด๋

```bash
$ git checkout master
```

- `git checkout master` : Signin์์ master๋ก branch ์ด๋
<br /><br />

## 5. ๋ก๊ทธ์ธ Branch ๋ณํฉ (pull request)
<br />

### [๋ก๊ทธ์ธ Branch ์๋ก๋]

1. Git ๋ฒ์  ๊ด๋ฆฌ

```bash
$ git status
$ git add .
$ git status
$ git commit -m '๋ก๊ทธ์ธ ํ์ด์ง ์์ฑ'
$ git log
```

- `git status` : ์์ ๋ด์ญ ํ์ธ (file : RED)
- `git add .` : ๋ฒ์  ๊ด๋ฆฌ ๋ฑ๋ก
`git status` : ์ฌํ์ธ (file : GREEN)
- `git commit -m 'Start project'` : ๋ฒ์  ์์ฑ
- `git log` : commit ํ ๋ฒ์  ํ์ธ

2. ์๊ฒฉ ์ ์ฅ์์ push

```bash
$ git push origin signin
```

- `git push origin signin` : signin branch๋ฅผ ์๋ก๋ ํ๋ค.

### [๋ณํฉํ๊ธฐ]

1. GitHub ์๋จ - Pull requests
2. ์ฐ์ธก New pull request
3. Base:master <- compare:signin ์ผ๋ก ์ค์  (Able to merge)
4. ์ฐ์ธก Create pull request
5. Comment ์ฐฝ์์ Create pull request
6. ํ์ด์ง ํ๋จ Merge pull request - confirm merge

### [Netlify ํ์ด์ง ํ์ธ]

1. Deploys ๋ฉ๋ด ์ ํ
2. ์๋ merged ๋ด์ฉ ํ์ธ ๊ฐ๋ฅ
<br /><br />

## 6. ํ๋ก์ ํธ ๋ณต์  (Clone)
<br />

1. GitHub ๋ก๊ทธ์ธ - Your repositories - Starbucks ์ ํ
2. Code ๋ฒํผ - Link Copy
3. VsCode - Terminal

```bash
$ ls(ios)
$ dir(window)
$ cd desk + [TAB] + [ENTER]
$ Ls + [ENTER]
$ cd ..
$ cd desk + [TAB] + [ENTER]
$ git clone + [GitHub์์ ๋ณต์ฌํ ๋งํฌ]
$ ls
```

- `ls`(ios) : ๋ง์ ํ์ผ๋ช๋ค์ด ๋ณด์<br />
ios์์๋ `ls`, window ์์๋ `dir`๋ฅผ ์๋ ฅํ๋ค.
- `cd desk + [TAB] + [ENTER]` : ๋ฐ์คํฌํ์ผ๋ก ์ด๋, `cd`๋ `change directory`
- `ls + [ENTER]` : Desktop์ ํ์ผ๋ช๋ค์ด ๋ณด์
- `cd ..` : Desktop ๋ฐ์ผ๋ก ์ด๋
- `cd desk + [TAB] + [ENTER]`: ๋ค์ ๋ฐ์คํฌํ์ผ๋ก ์ด๋
- `git clone + [GitHub์์ ๋ณต์ฌํ Link]` : GitHub ์ ์ฅ์ ํ์ผ์ด ๋ณต์ ๋๋ค
- `ls` : Starbucks ํ์ผ ์์ฑ ํ์ธ ๊ฐ๋ฅํจ

4. ๋ณต์ ํ ํ์ผ ๊ฐ์ ธ์ค๊ธฐ
5. VsCode - Terminal

```bash
$ cd desk + [TAB] + [ENTER]
$ cd Starbucks + [TAB] + [ENTER
$ code .
$ code . -r
```

- `cd desk + [TAB] + [ENTER]` : ๋ฐ์คํฌํ์ผ๋ก ์ด๋, `cd`๋ `change directory`
- `cd Starbucks + [TAB] + [ENTER]` : Starbucks ํด๋๋ก ์ ๊ทผ
- `code .` : Starbucks ํด๋๊ฐ ์์ฐฝ์ผ๋ก ์ด๋ฆฐ๋ค
- `code . -r` : Starbucks ํด๋๊ฐ ๊ธฐ์กด์ฐฝ์์ ์ด๋ฆฐ๋ค
<br /><br />

## 7. ๋ฒ์  ๋๋๋ฆฌ๊ธฐ (Reset)
<br />

### [ํ๋ก์ ํธ ์ถ๊ฐ ์์]

1. A project ์์
2. VsCode - Terminal ์คํ (๋ฒ์  1 ์์ฑ)

```bash
$ git init
$ git status
$ git add .
$ git status
$ git commit -m โ1โ
$ git log
```

3. A project ์์ 
4. VsCode - Terminal ์คํ (๋ฒ์  2 ์์ฑ)

```bash
$ git status
$ git add .
$ git status
$ git commit -m โ2โ
$ git log
```

5. A project ์์ 
6. VsCode - Terminal ์คํ (๋ฒ์  3 ์์ฑ)

```bash
$ git status
$ git add .
$ git status
$ git commit -m โ3โ
$ git log
```

### [๋ฒ์  ๋๋๋ฆฌ๊ธฐ]

7. ๋ฒ์  2๋ก ๋์๊ฐ๊ธฐ

```bash
$ git reset --hard HEAD~1
```

- `git reset --hard HEAD~1` : ์ต์ ๋ฒ์ (HEAD)์์ ๋ค๋ก 1๋ฒ์  ๋๋๋ฆผ

8. ๋ค์ ๋ฒ์  3์ผ๋ก ๋์๊ฐ๊ธฐ

```bash
$ git reset --hard ORIG HEAD
```

- `git reset --hard ORIG HEAD` : `ORIG`๋ `๊ธฐ์กด`์ด๋ผ๋ ๋ป

9. ๋ฒ์  1๋ก ๋์๊ฐ๊ธฐ

```bash
$ git reset --hard HEAD~2
```

- `git reset --hard HEAD~2` : ์ต์ ๋ฒ์ (HEAD)์์ ๋ค๋ก 2๋ฒ์  ๋๋๋ฆผ

10. ๋ค์ ๋ฒ์  3๋ก ๋์๊ฐ๊ธฐ

```bash
$ Git reset --hard ORIG HEAD
```
<br /><br />

## 8. Branch ๋ง๋ค๊ธฐ
<br />

1. branch ์์ฑ
2. VsCode - Terminal

```bash
$ git branch purple
$ git branch
$ git checkout purple
```

- `git branch purple` : purple branch ์์ฑ
- `git branch` : branch ๋ชฉ๋ก ํ์ธ ๊ฐ๋ฅ
- `git checkout purple` : purple branch๋ก ์ด๋

3. Purple project ๋ด์ฉ ์์ฑ ํ ๋ฒ์  ์์ฑ

```bash
$ git status
$ git add .
$ git status
$ git commit -m โpurple/1โ
$ git log
```

4. Master branch๋ก ์ด๋

```bash
$ git checkout master
```

5. Master branch ์ํ์์ html ๋ด์ฉ ์์  (๋ฒ์  4 ์์ฑ)

```bash
$ git add .
$ git commit -m โ4โ
$ git  log
```

6. GitHub ์ ์ฅ์์ master branch ์๋ก๋
- Repositories - New - ์ ์ฅ์ ์ด๋ฆ ์๋ ฅ - Create repository
- ์ ์ฅ์ ์ฃผ์ ๋ณต์ฌ
7. VsCode - Terminal

```bash
$ git remote add origin + [๋ณต์ฌํ ๋งํฌ]
$ git push origin master
```

- `git remote add origin + [๋ณต์ฌํ ๋งํฌ]` : ์๊ฒฉ์ ์ฅ์ ์ฃผ์ ๋ฑ๋ก
- `git push origin master` : ์ ์ฅ์์ push

8. GitHub ์ ์ฅ์์ purple branch ์๋ก๋

```bash
$ git checkout purple
$ Git push origin purple
```

- `git checkout purple` : purple branch ๋ก ์ด๋
<br /><br />

## 9. ๋ค๋ฅธ ํ๊ฒฝ์์ ์์ํ๊ธฐ
<br />

1. GitHub - repositories - ์ ์ฅ์ ๋งํฌ ๋ณต์ฌ
2. VsCode - Terminal

```bash
$ ls(ios)
$ dir(window)
$ cd desk + [TAB] + [ENTER] : ๋ฐํํ๋ฉด์ผ๋ก ๊ฒฝ๋ก ๋ฐ๊ฟ
$ git clone : ์๊ฒฉ์ ์ฅ์ ํ์ผ ๋ณต์ 
$ cd git- + [TAB]
$ code . -r : VsCode ํ์ฌ์ฐฝ์์ ํ์ผ ์ด๋ฆผ
```

- `ls`(ios) : ๋ง์ ํ์ผ๋ช๋ค์ด ๋ณด์<br />
ios์์๋ `ls`, window ์์๋ `dir`๋ฅผ ์๋ ฅํ๋ค.
- `cd desk + [TAB] + [ENTER]` : ๋ฐํํ๋ฉด์ผ๋ก ๊ฒฝ๋ก ๋ฐ๊ฟ
- `git clone` : ์๊ฒฉ์ ์ฅ์ ํ์ผ ๋ณต์ 
- `code . -r` : VsCode ํ์ฌ์ฐฝ์์ ํ์ผ ์ด๋ฆผ

3. ๋ณต์ ํ ํด๋ VsCode์์ ์ด๋ฆผ

```bash
$ git branch
$ git branch -r
$ git checkout -t origin/purple
$ git branch
```

- `git branch -r` : ๋ค๋ฅธ branch ๊ฐ์ ธ์ค๊ธฐ
- `git checkout -t origin/purple` : ์๊ฒฉ์ ์ฅ์์ purple branch ๊ฐ์ ธ์ด
- `git branch` : master branch, purple branch ๋๋ค ๋ณด์

4. ๊ฐ์ ธ์จ branch๊ฐ ํ์์์ด์ ์ง์ธ ๋

```bash
$ git checkout master
$ git branch -d purple
```

- `git branch -d purple` : purple branch ์ญ์ 

5. Yellow branch ์์ฑํ๊ธฐ

```bash
$ git branch yellow
$ git branch
$ git checkout yellow
```

- `git branch yellow` : yellow branch ์์ฑ
- `git branch` : master, yellow branch ์กฐํ๊ฐ๋ฅ
- `git checkout yellow` : yellow branch๋ก ์ด๋

6. Yellow branch ์ญ์ 

```bash
$ git checkout master
$ git branch -d yellow
$ git branch
```

- `git checkout master` : master branch ๋ก ์ด๋
- `git branch -d yellow` : yellow branch ์ ๊ฑฐ
- `git branch` : branch ๋ชฉ๋ก ํ์ธ (master branch๋ง ๋์ด)

7. ์์ฑ๊ณผ ๋์์ ํด๋น branch๋ก ์ด๋ํ๊ธฐ

```bash
$ git checkout -b yellow
```

- `git checkout -b yellow` : yellow branch ์์ฑ&์ด๋

8. Yellow branch push ํ๊ธฐ

```bash
$ git push origin yellow
```

9. GitHub ์์ ํ๋ก์ ํธ ํ์ธ๊ฐ๋ฅ
<br /><br />

## 10. ๋ฒ์ ์ ์ถฉ๋ Conflict, ๋ก์ปฌ ๋ณํฉ Merge
<br />

### [์๋ก์ด PC์์ ํ๋ก์ ํธ ์งํ (์ถฉ๋์ํฉ) ]

1. PC์๋ XYZ ์์  ์  master๋ก ๋ฒ์  1 ํ๋ก์ ํธ๊ฐ ์ด๋ ค์๋ค
2. ์๊ฒฉ์ ์ฅ์์ XYZ ๋ด์ฉ์ด ์๋ ์ค ๋ชจ๋ฅด๊ณ  ๋ฒ์  1์์ ABC๋ก ๋ด์ฉ ์์ 
3. ์์ ํ ๋ด์ฉ์ pushํจ

```bash
$ git status
$ git add .
$ git commit -m โABCโ
```

4. ์ ์ฅ์์ push ์๋, pull request๋ก ๋ณํฉ์๋

```bash
$ git push origin master
```

- `git push origin master` : rejected push๋ก ๊ฑฐ๋ถ๋จ (์ ์ฅ์ ๋ด์ฉ๊ณผ ๋ก์ปฌํ๊ฒฝ ๋ด์ฉ์ด ๋ค๋ฅด๊ธฐ ๋๋ฌธ์ด๋ค)

5. ํด๊ฒฐ๋ฐฉ๋ฒ 1

> local ํ๊ฒฝ ๋ฒ์  reset

```bash
$ git reset --hard HEAD~1
```

6. ํด๊ฒฐ๋ฐฉ๋ฒ 2 

> ์์ ํ ๋ด์ฉ์ ์๋ก์ด ๋ฒ์ ์ผ๋ก ๋ค์ ๋ง๋ ๋ค

```bash
$ git pull origin master
```

- `git pull origin master` : ์๊ฒฉ์ ์ฅ์์์ local ํ๊ฒฝ์ผ๋ก ๊ฐ์ ธ์จ๋ค
- conflict ์ถฉ๋ ๋ฉ์ธ์ง ๋์ด
- html์ ๋ฉ์ธ์ง๊ฐ ๋ฌ๋ค (๋ด์ฉ์ ํ ๊ฐ๋ฅ) : ์ฌ์ฉํ์ง ์์ ์ฝ๋๋ฅผ ์ง์์ฃผ๋ฉด ๋ฐ์๋๋ค

7. ํด๊ฒฐ๋ฐฉ๋ฒ 3

> ์ ์ฅ์(XYZ), local(ABC) ๋ด์ฉ์ ์์ด ์๋ก์ด ๋ฒ์ (ABYZ)์ผ๋ก ๋ง๋ ๋ค

```bash
$ git pull origin master
```

- `git pull origin master` : ์๊ฒฉ์ ์ฅ์์์ local ํ๊ฒฝ์ผ๋ก ๊ฐ์ ธ์จ๋ค
- conflict ์ถฉ๋ ๋ฉ์ธ์ง ๋์ด
- html์ ๋ฉ์ธ์ง๊ฐ ๋ฌ๋ค (์ํ๋ ๋ด์ฉ์ผ๋ก ์์ )
- ์๋ก์ด ๋ฒ์  ์์ฑ

```bash
$ git status
$ git add .
$ git status
$ git commit -m โABYZโ
$ git push origin master
```

- `git commit -m โABYZโ` : ๋ฒ์  ์์ฑ
- `git push origin master` : ์๊ฒฉ์ ์ฅ์๋ก ์๋ก๋

8. Push ์๋ฃ
