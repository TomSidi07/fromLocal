# NOTES : GIT

+ Git is a version tracking system

+ Github and GitLab are providers built on the idea of Git

## Set Git default editor : windows 

- vscode : git config --global core.editor "code --wait"
- nano : git config --global core.editor "/usr/bin/nano"

## git config setting 
### global : with --global
- list all config : 

    ``git config list --global``
- set global user: 

    ``git config --global user.name "_name"``
    
    ``git config --global user.email "_email"``
### setting : for a repo without --global
- set global user: 
    ``git config user.name "_name"``
    
    ``git config user.email "_email"``

## GIT ADD & GIT COMMIT 
### git add : Transit
- command ``git add`` tells to Git ``follow all this file moves 👀``


``git add file.txt`` --add it to the--> ``stagging area(index area)``

### git commit : 
- command ``git commit`` tells to Git ``take a snapshot of the current state of all the files you've been follwed``

``git commit -m "message"``


### workflow:

``working_dir`` -- ``-gitadd``---> ``stagging area``-- ``-gitcommit``---> ``local repo``

### GIT PUSH & GIT PULL
<!-- GIT PUSH -->
## GIT LOG 

- cli :
	git log
	git log -_index_of_commit
## PUSHING LOCAL REPO TO A GIT PROVIDER:

we cannot use command to initialize a repo on github or gitlab; we need to do handle it on the webpage

### set a remote repo

	1- initial git : git init
	2- git add origin <url>
	3- check it : git remote -v
	4- push local commits: git push -u
	5- if it fails: you have to set uptream repo
## Branches
- Create a new branch from main:

		from the main branch : 
			git checkout -b _newbranch

- point remote branch:
	
		from the local new_branch : 
			git <action(can be push or ...)> set-uptream origin _bran_to_point 

- Get a commit from another branch
		
		1- you have to get the __commit_id
		2- checkout(switch) to the destination branch
		3- git cherry-pick __commit_id
## setting up ssh

	1- cd /.ssh

	2- generate ssh key: 
		ssh-keygen -t rsa -b 4096

	3- press enter enter enter

	4- config your ssh key in github settings/ssh key

## changing the remote url of an repo:

	1- locate the config file under the url property with: git config --edit

	2- cli:
		git remote set-url origin <url>
	3- check the changes cli step(1)
