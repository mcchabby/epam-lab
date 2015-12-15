# EPAM Git Lab
## Instructor: Vitali Shulha

## Blob: 
- Smallest piece of Git project.
- Snapshot of a file.

## SHA1:
- Hashing algorithm. 160 bits, 40 hex length.
- Everything stored in Git is hashed.

## Undoing Changes
**Git Reset**
	- Soft: Change HEAD to old SHA1
		- git reset --soft <sha1>
		- Add changes to index
	- Mixed (Default)
		- Change HEAD to old SHA1
		- git reset --mixed <sha1>
		- Do not add changes to index
	- Hard
		- Does not save changes
		- Does not remove the new commit
**Working Directory**
**Staging Area**
**Local Branch**
**Remote Repository**

## Branching
**Merging**
	- Fast-forward merge: Does not produce additional commit
	- Non FF Merge: Produces additional commit with details
	- Resolve Merge COnflicts
		- Abort Merge: git merge -abort
		- Resolve by selecting version: git checkout --ours -theirs
		- Resolve manually: git diff
		- Use Merge tool
*How to avoid conflicts:*
	- Short commits
	- No edits to whitespaces
	- Merge often

## Git Stash
- Save working directory: git stash
- View stashes: git stash list
- Bring them back: git stash pop / git stash apply

## Teamwork
**Blame:** See all commits related to the file
	- git blame *file*
**Bisect:** Binary search
	- git bisect start
**Merge requests**
	- Make feature in branch
	- Review and merge from UI
**Rebase:** Trying to create fast forward merges every time
	Possible corruption of history. Non-linear history.
	Never rebase the public branches
**Cherry-Pick:** the way you can pick any commit in any branch and apply to any branch

## Branching Strategies
**Centralized Workflow:** Team uses 1 branch only
**Feature Branch Workflow:** Dedicate one branch per each feature
	- Use Pull Requests
**Gitflow Workflow:** Several major branches (develop, master, features)
	- Master is for production only
	- Release and hotfix branches
**Forking Workflow:** Separate repository for each developer

## Books
- [Pro Git] https://git-scm.com/book/en/v2
- [Version Control with Git] http://shop.oreilly.com/product/0636920022862.do
