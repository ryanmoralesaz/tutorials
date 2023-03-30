# Git Commands

## Youtube Tutorial

[FreeCodeCamp](https://www.youtube.com/watch?v=e2IbNHi4uCI&t=1753s)

## Using bare repos

[Engineer man](https://www.youtube.com/watch?v=8aZW9mYOxhc)

## Command List

- `git branch`
  - shows all branches
- `git switch`
- `git status`
- `git init`
- `git branch -m newname`

* change remote origin name
* `git remote set-url --add --push origin git@github.com:muccg/my-project.git`
* show origin name  
  `git remote show origin`

  - show all files in a bare repo  
    `git ls-tree --full-tree -r HEAD`

* tell repo to just be bare repo  
  `git config --bool core.bare true`
