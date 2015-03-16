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
```ShellSession
  git add .
  git commit -m "Short message describing what you did. "
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
  

