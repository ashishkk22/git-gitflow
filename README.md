# Git Practical exam
|  |  |
| ------ | ------ |
| Initializing a repository		|	git init |
| Stages a single file			|	git add filename.js |
| Viewing the status		|		git status|
| Commits with message		    |        git commit -m "Message" or git commit |
| Creates a new branch	 | 			git branch branchName  | 
 | Switches to the another branch  | 		git checkout branchName  | 
  | Deletes the branch		 | 		git branch -d branchName | 
 | Merge branch into the current branch  | 	git merge branchName  | 
 | Pushes branch to origin	 | 		git push -u origin branchName | 
 | Cloning a repository		 | 		git clone repoUrl | 
 | Adds a new remote called upstream	 | 	git remote add upstream url  | 
 | Push the local changes to remote	 | 	git push  | 
 | To save the some changes in the local 	 | git stash | 
 | To add the changes in the working tree |  	git stash pop | 
 | To clear the stash area 		 | 	git stash clear | 
 | To log all the information 	 | 		git log | 
 | Rebase 			 | 		git rebase branch_name | 
 | Cherry pick commit from the diff branch |  	git cherry-pick HASH | 

## Pull and merge difference
 A git pull is going to run a git fetch and then a git merge. If you want to bring your local repository up to speed with a remote repository that is what you would run.\
 A git fetch is going to import commits from a remote repo without merging them, which gives you the opportunity to review them before integrating.
→ if we don't have to directly merge the feature branch to the main branch then we have to do the pull request and after it is being approved it is going to merged in to the main branch\
→ pull request is also going to be beneficial if we don't own the repo and we are doing contributions with the fork repo\
→ with the merge both repo is going to be merged\
## Rebase
→ with the help of the rebase we can merge the branches \
→ this method is useful only when are doing the change to the branches\
	Git rebase feature → from the main branch and then new commit \
	Rebase is going to be done in that way\
## Change commit message
→to change the commit message we have to use\
Git commit –amend\
And after this command we will get the latest commit and we can edit it\
But if it is pushed on the github then we have to use\
Git push -u origin master -force\
We should not use the above command with force if we do that after our clone or latest pull if some change are there then it is going to be erased so we should use\
Git push -u origin master –force-with-lease\
So it is going to give the warning if there is any commit after our latest pull.\
## Cherry-pick
→ To merge  the main branch with the some specific commit of feature branch\
Git cherry-pick [id] \
Then after new commit and we are able to import all the changes that are present in that commit\
## Drop commit
→ to drop the commit one method doing it with rebase\
Git reabse -i [id] \
It is going to open the interactive environment and we can decide that we have to pick it or squash it\
→ second way is that we can reset the commit with\
Git reset –soft [HASH]\
