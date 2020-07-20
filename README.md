# Guide to set up your Repo

### [Basic writing and formatting syntax](https://help.github.com/articles/basic-writing-and-formatting-syntax/)
Create sophisticated formatting for your prose and code on GitHub with simple syntax.

## Adding an existing project to GitHub using the command line
- git init
- git add .
- git commit -m "First commit"
- git remote add origin [your repo url]()
- git remote -v
- git push origin master

## Issues
- Faced below issue while pushing to remote repo.
```
$ git push -u origin master
Username for 'https://github.com': viragjainVJ
To https://github.com/viragjainVJ/react-draggable-list
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'https://github.com/viragjainVJ/react-draggable-list'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
> Use Command :+1: `git push -f origin master` :+1:


## Redux-First Routing
```
npm install --save redux-first-routing
```
Redux-first routing is a variation on pushState routing that makes Redux the star of the routing model.

### A Redux-first routing solution satisfies the following criteria:

- The location is held in the Redux store.
- The location is changed by dispatching Redux actions.
- The application reads location data solely from the store.
- The store and browser history are kept in sync behind the scenes.
- Let middleware handle the side-effect of history navigation.

![Usage with Universal Router](https://camo.githubusercontent.com/381e787f15ad1f830a41d3e261157ae07d9f3999/687474703a2f2f692e696d6775722e636f6d2f557a51745934542e6a7067)

[Medium FreeCodeCamp](https://medium.freecodecamp.org/an-introduction-to-the-redux-first-routing-model-98926ebf53cb)

### Create Git Repo on Top of any branch
- git checkout -b <new_branch_name> (Create a branch in local)
- git push origin <new_branch_name> (Update & create a branch on Remote)

### Rename Git Repo
- git branch -m old-name new-name
- git push origin :old-name new-name
- git push origin -u new-name

OR

- git branch -m old_branch new_branch         # Rename branch locally    
- git push origin :old_branch                 # Delete the old branch    
- git push --set-upstream origin new_branch   # Push the new branch, set local branch to track the new remote

### Delete Git Repo
- git branch -D <branch_name> (Delete from Local)
- git push origin :<branch_name> (Delete from Remote) 
 or
- git push <remote_name> --delete <branch_name> (Delete from Remote) 

### Stash Data Retrieval
Stash the changes in a dirty working directory away
```
git stash list [<options>]
git stash show [<options>] [<stash>]
git stash drop [-q|--quiet] [<stash>]
git stash ( pop | apply ) [--index] [-q|--quiet] [<stash>]
git stash branch <branchname> [<stash>]
git stash [push [-p|--patch] [-k|--[no-]keep-index] [-q|--quiet]
	     [-u|--include-untracked] [-a|--all] [-m|--message <message>]
	     [--] [<pathspec>…​]]
git stash clear
git stash create [<message>]
git stash store [-m|--message <message>] [-q|--quiet] <commit>
```
Refer [Stash Command Description](https://git-scm.com/docs/git-stash)

### Remove Repository from Local to clone again
```
rm -rf repositoryA
```
### Merge Commits into one commit Message
- git rebase -i HEAD~N
- change the pick to squash and save the rebase
- it will ask for the commit message, save the message and proceed.
- if chnages are already pushed to remote branch and rebasing on local branch then --force the push
- git push origin <branch_name> --force

### Discard unwanted chnages from VS Code
- git clean  -d  -f .

### Cherry-Pick Commit
- git cherry-pick <SHA/commit-id> -m 1

### Revert Specific Commit or merge request
- git revert -m 1 <commit-id>
