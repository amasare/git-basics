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
Create 3 new files "playArea1.txt", "playArea2.txt", "playArea3.txt"
Stage files
Modify existing file "donkeyRyhmes.txt" again
Notice staged and unstaged state when you run a git status.
```ShellSession
 git status
 git status -s (--short)
 git add .
 git commit -m "Short message describing what you did. "
```
Remove newly created file "playArea1.txt" from git (staging and working directory)
```console
git rm playArea1.txt
```

Undoing
*Anything that you lose that you have not commited can never be gotten back*
If you forgot to add "i_forgot_you.txt" to your commit.
```console
git add .
git commit --amend
```

If you want to unstage (remove from snapshot ready for commit) a file
Create "i_am_going_to_unstage_you_in_a_sec.txt"
```console
git add . 
git reset HEAD i_am_going_to_unstage_you_in_a_sec.txt
```
File is now in working directory and modified state only. To unmodify:
```console
git add . 
git checkout -- i_am_going_to_unstage_you_in_a_sec.txt
rm i_am_going_to_unstage_you_in_a_sec.txt
git checkout -- playArea2.txt
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
 
