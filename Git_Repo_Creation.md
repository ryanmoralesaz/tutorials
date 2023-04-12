# How to make a git repo in Dropbox that you can then push to GITHUB

1.

```console
mkdir -p ~/myProject
mkdir -p ~/Dropbox/Git
cd ~/Dropbox/Git
git init --bare myProject.git
cd ~/myProject
git remote add dropbox ~/Dropbox/Git/myProject.git

git push -u dropbox main
```

2.  Then add a remote to push to GitHub

```console
cd ~/Dropbox/Git/myProject.git
git remote add origin path_to_github
git push -u origin main
```

# Make Google Drive into a git repo

1. make a myProject folder locally and use `git init`  
   make sure to use `git branch -m master main` to rename and checkout the main branch.
2. `CD` into google drive git folder

```console
git init --bare myProject.git
cd myProject.git
git branch -m main
```

3.  `CD` into local project

```console
git remote add gdrive /PATH_TO_GDRIVE_myProject.git
git add .
git commit -m "first commit"
git push -u gdrive main
```

4. Then add a remote to push to github

```console
cd ~/gdrive/Git/myProject.git
git remote add github path_to_github
git push -u github main
```
