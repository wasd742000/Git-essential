# GIT & GITHUN ESSENTIAL TRAINING

## GIT
### Git config
Tell git who you are so that it will give you credit for the changes you made.
Github email.
'--global' option meaning that all the project on the computer use the same name and email.
''' git config --global user.name "name here" '''
''' git config --global user.email "email here" '''


Prepare the project folder. In the project folder:
''' git init '''

### Staging files
Staging area: a temporary area to store files that we want to commit later on.
To add files to staging area:
''' 
git add FILENAME 
// or add all files
git add --all
git add -A
git add .
'''

Commit (make a checkpoint for the project)
'''
git commit -m "commit note here"
'''

To verify git keep track of what we had done:
'''
git log
'''
## GITUB