## 프로젝트 생성
> React 예시

1. 로컬 - `create-react-app` 프로젝트 설치  
`npx create-react-app '작업폴더명'`

2. github.com - 원격 저장소 생성

3. 로컬 - `github` 원격 저장소 연결  
`git remote add origin 'github 저장소 주소'`

4. 로컬 - `main` 브랜치 생성   
`git branch -M main`

5. 로컬 - 원격 저장소에 소스 올리기  
`git push -u origin main`

#### 옵션 참고 [링크](https://www.git-scm.com/docs/git-branch/2.29.0)
##### -m or -M
`git branch (-m | -M) [<oldbranch>] <newbranch>`  
> With a -m or -M option, <oldbranch> will be renamed to <newbranch>. 
> If <oldbranch> had a corresponding reflog, it is renamed to match <newbranch>, and a reflog entry is created to remember the branch renaming. 
> If <newbranch> exists, -M must be used to force the rename to happen.


`-m or --move`
> Move/rename a branch and the corresponding reflog.

`-M`
> Shortcut for --move --force.

##### -u or --set-upstream-to
````
-u <upstream>
--set-upstream-to=<upstream>
````
> Set up <branchname>'s tracking information so <upstream> is considered <branchname>'s upstream branch. 
> If no <branchname> is specified, then it defaults to the current branch.
