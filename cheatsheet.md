# Git in Powershell Command Cheat Sheet
> ## We'll be able to fly, don't fear the repo
*Author: Philip Mannering*  
*Date: 2020-04-05*

Git is the most popular ___version control system (VCS)___ that is especially useful in tracking changes to text documents. Learn git now to avoid naming files like `my_source_code_v4_final_final.py`

Below are a list of frequently used git commands that I use in Powershell to track my the development of code. This document was written by myself for myself as a reference.

If you do not have git you can download it from `https://git-scm.com`

## Check you have Git Installed
```
> git --version
git version 2.26.0.windows.1
```
Or simply type `git` to get a list of useful commands
```
> git
start a working area (see also: git help tutorial)
   clone             Clone a repository into a new directory
   init              Create an empty Git repository or reinitialize an existing one
   ⋮
```

For specific information on a git command (say, git status) use,
```
> git help status
```

## Starting a Project  
First navigate to the project folder using `> cd path/to/folder`.

Clone and existing repository, 
```
> git clone <remote directory>
```
Or to start a new project,
```
> mkdir my_new_project
> cd my_new_project
> git init
```
Check your project has the _.git_ folder by using either
```
> Get-ChildItem -Force    # for all files
> Get-ChildItem -Hidden   # Just the hidden files
> ls -h					  # shorthand
```

## Tracking Changes
The **most important command** to check which files are being tracked and which files have been modified to be _staged_ or _commited_ (or both).
```
> git status
```

The vast majority of your workflow,
```
(make changes)
> git add .
> git commit -m "A descriptive label of changes"
(make more changes)
> git add .
> git commit -m "Another descriptive label of changes"
(make even more changes)
> git add .
> git commit -m "Another descriptive label of changes"
```
Or add and commit changes in a single command,
```
git commit -am "Another descriptive label of changes
```
Tips,
* Use `> git status` often to check which files need to be staged and committed.
* Add similar edits together under a single commit.
* Use `> code` or `> code newfile.txt` to open up Visual Studio Code from the command line.






##### Checking that status of your local repository - shows changed but not added files in red
		git status

##### Creating a new branch for you to work on
		git branch <new branch name>

##### See all branches in your remote repository
		git branch -a

##### Moving onto a branch
		git checkout <branch name>

##### Deleting a branch
		git branch -d <branch name>

##### Moving files while preserving git history
		git mv <source> <destination>
 
 
##### making a new branch whilst moving into it AT THE SAME TIME
		git checkout -b <new branch name>

