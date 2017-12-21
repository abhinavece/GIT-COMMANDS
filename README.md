# GIT-COMMANDS
List Of git commands


******************************  REBASE  *************************************
In Git, there are two main ways to integrate changes from one branch into another: the merge and the rebase.

			A---B---C topic
         /
    D---E---F---G master

	WOULD BE
	
					A'--B'--C' topic
                 /
    D---E---F---G master

	
-- Create a new branch called <branch>

git checkout <branch>

-- master and topic are branches

git rebase master  
OR
git rebase master topic

-- If conflict occurs , then make changes on (<<<<<<<<<) lines and tell git that conflicts has been resolved using 

git add <filename>

-- continue REBASE after conflicts resolved

git rebase --continue

-- UNDO REBASE
git rebase --abort

*****************************************************************************
// Backout changes

git reset HEAD <fileName> to unstage
git checkout -- <fileName> to discard changes in working directory

******************************************************************************
// Checking log
git log --oneline --decorate --graph --all
or
git hist

// Checking everything you have done
git reflog

// Comparison -- use difftool for visual tool popup

git diff => difference between working and staging

git diff HEAD => difference between working and last commit

git diff --staged HEAD => Comparing between the Staging Area and the Git Repository (Last Commit)

git diff HEAD <commitID>  => difference between commits

git diff master origin/master => difference between local master and origin master

// Stashing the working file (which is not yet added to staging area or commited, simply thats in working directory)

****************************  Check deleted files on master barnch  *****************************
git clean -n

Remove deleted files from local
git clean -f 

*****************************  git stash   ********************************

// have pull or do change in other file commit it and now go for stash apply (for tracked files)

git stash apply => now add it and commit it and then drop the stash from list
git stash list
git stash drop
=================

******************************   Adding new/modified  staged files using -u 

git stash -u => adding all kind of file in stash area
git stash pop => applied and dropped

git stash show stash@{1}
git stahs apply stash@{1}
git stash drop stash@{1}

git stash clear => removes all stashes from the list

//========= Applying stash in new branch

make any kind of file => modified/untracked/staged
git stash -u  =>saved working directory in stash
git stash --branch newBranchName  => new branch created and stash is applied and stash is dropped also

// ========================== RESET HEAD to some commit
git reset HEAD HEAD^ => Head will direct to one commit back
git reset HEAD HEAD^1 =>

__________________________________________________________________________________________________________________________
__________________________________________________________________________________________________________________________

office 2007
KGFVY-7733B-8WCK9-KTG64-BC7D8
