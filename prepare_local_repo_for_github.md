# How to prepare a local folder to push to github

> 1.  Navigate inside of desired of repo with terminal

> 2.  Initialize the repo
>     > `git init`

> 3.  add a readme file
>     > `touch README.md`

> 4.  add a .gitignore file
>     > `touch .gitignore`

> > add `.DS_Store` to the file for mac

> > add `node_modules/`

> > add `logs/`

> > if there is a problem with .DS_Store on mac run `git rm --cached .DS_Store`

> 5.  add all files to git
>     > `git add .`

> 6.  Add first commit message
>     > `git commit -m "initial message"`

> 7.  View the commit status
>     > `git status`

> 8. change name of main branch from "master" to "main"
>    > `git branch -M main`

> 9. add the remote origin (this part can be tricky)
>    > `git remote add origin _(your repo url)_`

> 10. push to the remote origin
>     > `git push -u origin main`
