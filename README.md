# git-basics
Take you through an everyday git workflow

Need help at anytime?  
http://git-scm.com/book/
```console
 man git
 git help
 man git-<verb> #eg man git-bisect
```

#### First Time Setup
##### Set your user name and email address. Necessary for commits
```console
 git config --global user.name "Rusty Taco"
 git config --global user.email rustytaco@yolo.com
```
#### Import A New Project
```console
 git clone git@github.com:amasare/git-basics.git
```
#### Make Changes
Modify existing file "donkey.txt"  
Create 3 new files "playArea1.txt", "playArea2.txt", "playArea3.txt"  
Stage files  
Modify existing file "donkey.txt" again  
Notice staged and unstaged state when you run a git status.
```console
 git status
 git status -s (--short)
 git diff (--staged)
 git add .
 git commit -m "Short message describing what you did. "
```
Remove newly created file "playArea1.txt" from git (staging and working directory -becomes untracked)
```console
git rm playArea1.txt
```
######Commit Messages Guide
<ul>
<li>Separate subject from body with a blank line</li>
<li>Limit the subject line to 50 characters</li>
<li>Capitalize the subject line</li>
<li>Do not end the subject line with a period</li>
<li>Use the imperative mood in the subject line</li>
<li>Wrap the body at 72 characters</li>
<li>Use the body to explain what and why vs. how</li>  
</ul>
#### View changes
```console
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
####Aliases
Shortcuts for specified commands
```console
git config --global alias.co checkout #Next time run 'git co' instead of 'git checkout'
git config --global alias.unstage 'reset HEAD --'
git config --global alias.last 'log -1 HEAD'
```
Modify playArea2.txt, stage it, then unstage with your new alias

###Branches
#### Create Branch
```console
git branch 'awesome_branch'
git log --decorate #observe which commits all the branches are pointing to
```  
HEAD - branch git is on at the moment
#### Switch To New Branch
```console
git checkout 'awesome_branch'
```  
Create commit on new branch and check commits pointed to again    
Switch to master, check commits pointed to. Changes are isolated!
```console
git log --decorate --all
``` 

#### Merge Branch
Replay changes in awesome_branch since it diverged from master, record result in a new commit on top of master
```ShellSession
git merge master
```  
 
### Random Favourites
```console
git blame
git bisect
```  
