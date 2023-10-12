# Git

## Create

Clone an existing repository
``` 
git clone ssh://user@domain.com/repo.git
``` 
Create a new local repository
``` 
git init
``` 

<br>
<br>

## Undo

Discard all local changes in your working directory
```
git reset -hard HEAD
```
Discard local changes in a specific file
```
git checkout HEAD \<file>
```
Revert a commit (by producing a new commit with contrary changes)
```
git revert \<commit>
```
Reset your HEAD pointer to a previous commit ... and discard all changes since then
```
git reset -hard \<commit>
```
... and preserve all changes as unstaged changes
```
git reset \<commit>
```
... and preserve uncommited local changes
```
git reset -keep \<commit>
```
<br>
<br>

## Commit history

Show all commits, starting with newest
```
git log
```
Show changes over time for a specific file
```
git log -p \<file>
```
Who changed what and when in \<file>
```
git blame \<file>
```

<br>
<br>

## Local changes

Changed files in your working directory
```
git status
```
Changes to tracked files
```
git diff
```
Add all current changes to the next commit
```
git add
```
Add some changes in \<file> to the next commit
```
git add -p \<file>
```
Commit all local changes in tracked files
```
git commit -a
```
Commit previously staged changes
```
git commit
```
Change the last commit
##### Don't amend published commits!
```
git commit -amend
```
<br>
<br>

## Update & Publish

List all currently configured remotes
```
git remote -v
```
Show information about remote
```
git remote show \<remote>
```
Add new remote repository, named \<remote>
```
git remote add \<shortname> \<url>
```
Download all changes from \<remote>, but don't integrate into HEAD
```
git fetch \<remote>
```
Download all changes and directly merge/integrate into HEAD
```
git pull \<remote> \<branch>
```
Publish local changes on a remote
##### Delete a branch on the remote
```
git branch -dr \<remote/branch>
```
Publish your tags
```
git push --tags
```
<br>
<br>

## Branches & Tags

List all existing branches
```
git branch -av
```
Switch HEAD branch
```
git checkout \<branch>
```
Create a new branch based on your current HEAD
```
git branch \<new-branch>
```
Create a new tracking branch basd on a remote branch
```
git checkout --track \<remote/branch>
```
Delete a local ranch
```
git branch -d \<branch>
```
Mark th cuent commit with a tag
```
git tag \<tag-branch>
```
<br>
<br>

## Merge & Rebase

Merge \<branch> into our current HEAD
```
git merge \<branch>
```
Rebase your curent HEAD onto \<branch>
##### Don't rebase published commits!
```
git rebase \<branch>
```
Abort rebase
```
git rebase --abort
```
Continue a rebase after resolving conflicts
```
git rebase --continue
```
Use your configued merge tool to solve conflicts
```
git mergetool
```
Use your editor to manually solve conflicts and (afer reslving) mark file as resolved
```
git add \<resolved-file>
git rm \<resolved-file>
```