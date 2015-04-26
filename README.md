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
Modify existing file "donkey.txt"  
Create 3 new files "playArea1.txt", "playArea2.txt", "playArea3.txt"  
Stage files  
Modify existing file "donkey.txt" again  
Notice staged and unstaged state when you run a git status.
```ShellSession
 git status
 git status -s (--short)
 git diff (--staged)
 git add .
 git commit -m "Short message describing what you did. "
```
Remove newly created file "playArea1.txt" from git (staging and working directory)
```console
git rm playArea1.txt
```
#### View changes
```ShellSession
 git log [-p|--stat|--graph|--oneline][--pretty=short|full|fuller][--since="2 weeks ago"]
```
#### Undo changes
*Anything that you lose that you have not commited can never be gotten back*
######If you forgot to add "i_forgot_you.txt" to your commit.
```console
git add .
git commit --amend
```
######If you want to unstage (remove from snapshot ready for commit) a file
Modify and stage "donkey.txt"
```console
git add . 
```
Remove file from index
```console
git reset HEAD donkey.txt
```
File is in working directory and modified state only. To unmodify (revert it to it's last committed state) <strong>DANGEROUS</strong>:
```console
git checkout -- donkey.txt
```
#### Share With Others
```ShellSession
 git push
```
#### Update Your Repository
```ShellSession
 git pull --rebase
```
#### Tag
Tag specific version in history as important
```console
git tag 'release1'
git status
git show 'release1'
```
Tag information doesn't usually go with a push. To push tag:
```console
git push origin 'release1'
```

#### Create Branch
```ShellSession
 git branch "branch name"
```  
#### Merge Branch
```ShellSession
  git merge master
```  
 
