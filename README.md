# git-basics
Take you through an everyday git workflow

Need help at anytime?
```ShellSession
 man git
 git help
 man git-<verb> #eg man git-bisect
```

#### First Time Setup
##### Set your user name and email address. Necessary for commits
```ShellSession
 git config --global user.name "Rusty Taco"
 git config --global user.email rustytaco@yolo.com
```
#### Import A New Project
```ShellSession
 git clone git@github.com:amasare/git-basics.git
```
#### Make Changes
Modify existing file
Create a new file
Stage files
Modify existing file again
Notice staged and unstaged state when you run a git status.
```ShellSession
 git status
 git status -s (--short)
 git add .
 git commit -m "Short message describing what you did. "
```
Remove newly created file from git
```console
git rm
```
#### Viewing changes
```ShellSession
 git log [-p|--stat|--graph|--oneline][--pretty=short|full|fuller][--since="2 weeks ago"]
```
#### Share With Others
```ShellSession
 git push
```
#### Update Your Repository
```ShellSession
 git pull --rebase
```
#### Create Branch
```ShellSession
 git branch "branch name"
```  
#### Merge Branch
```ShellSession
  git merge master
```  
 
