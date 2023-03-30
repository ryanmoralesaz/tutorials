# How to make a git repo in Dropbox that you can then push to GITHUB

1.

```console
mkdir -p ~/Dropbox/Git
cd ~/Dropbox/Git
git init --bare myProject.git
cd ~/myProject
git remote add dropbox ~/Dropbox/Git/myProject.git

git push -u dropbox main
```

2.  Then

```console
cd ~/Dropbox/Git/myProject.git
git remote add origin path_to_github
git push -u origin main
```
