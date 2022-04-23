**GIT & GITHUN ESSENTIAL TRAINING**

# GIT
## 1) Git config
In gitbash (or other terminal)
```
git config --global user.name "name here"
git config --global user.email "email here" 
```
- Tell git who you are so that it will give you credit for the changes you made.
- Option `--global`  meaning that all the project on the computer use the same name and email.
- Use the same email registed with github.

Prepare the project folder. In the project folder:
```
git init
// this will create .git folder
```
## 2) Staging files
- Staging area: a temporary area to store files that we want to commit later on.
- To add files to staging area:
``` 
git add FILENAME 
// or add all files
git add --all
git add -A
git add .
```
- Commit (make a checkpoint for the project)
```
git commit -m "commit note here"
```
- To verify git keep track of what we had done:
```
git log
```
![commit info](img/1_log.png "Commit info")
## 3) Git environment
Git has 3 environment to move files:
- Working
- Staging
- Commit

Before a commit, files can be in 2 states:
- Tracked: files existed in the previous snapshot (commit)
- Untracked: anything else (new files added since the last commit)

Tracked files can be in several states:
- Unmodified: files have not changed since the last commit
- Modified: files have changed since the last commit
- Staged: files moved to staging environment

To view git environment changes:
```
git status
```

Restore (to unstage):
```
git restore FILENAME
// restore whole folder
git restore .
// or
git checkout .
```
## 4) Ignore files
Why ?
- Sensitive files
- Personal notes
- System files

Create a `.gitignore` file at the root of the project. 
<br>![git ignore file example](img/2_ignore.png "git ignore file example")

Global ignore file:
```
git config --global core.excludesfile [ignored file go here]
```

You may add a file to .gitignore file after a lot of commits. Should clear local caches:
```
git rm -r --cached .
```

## 5) Deleting and renaming files
### a) Deleting files
- Deleting project files using system file management or IDE file management can be restore by using `git restore`.
<br>![](img/3_del.png)
- Deleting project files using `git rm NAMEFILE` not only delete the file, but also move that deletion into staging and ready for commit (`git add`).
<br>![](img/4_rm.png)
- Using `git restore --staged FILENAME` to unstage.
<br>![](img/5_rs.png)

### b) Renaming files
- You can rename project files using system file management or IDE file management. This will copy the file with new name and delete the old name file. You can undo this by using `git restore` and delete the new name file.
<br>![](img/6_rn1.png)
- Rename using git:
```
git mv oldFileName newFileName
```
- The file is also ready to be commited
<br>![](img/7_mv.png)



## 6) Differences
- To check the difference of all project files compare to the last commit, using: 
```
git diff
```
- VS code has *Source control* with the same usage.
- Using `git log --oneline` for brief log information.
<br>![](img/8_log1.png)
- Using `git diff commitID1 commitID2` to show differences between two commit.

## 7) Changing history

# GITHUB