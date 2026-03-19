# devops-git-learning
Git Learning 

### Pull Request
Team collebration without afttecting the master branch.
Explain the process.

### List the global configs
```
git config user.name
git config user.email
git config --global --list
git config --list
```

### Create a GitHub Repo

### Clone the repo
```
git clone <Repo-URL>
```

### First Commit and Push
- update the README.md
- Commit and Push
```
git add README.md
git commit -m "Commit Message" (What is commit message)
git push
git log --oneline
```

### Github Brnaching
- main/master branch from where the code is pushed to the production
- unverified code changes are kept in a different branch seperated from the main branch.
- Create a Branch and develop your code and test it.
- Create a pull request
```
git branch -a
git fetch (sync the local branches with github)
git branch -a
git checkout feature/git-learning
git branch 
```
### Untracked file
- red in color and we have to tell the git to track the file.
```
git add file-name
```
Note:- If you delete the repo/file before commiting to the remote repo, your changes will be lost.

### Fork Vs Clone
- When you dont have access to the original repo or the repo in someones account
Fork → Clone → Work → Push → Pull Request.
Clone -> Making copy of the repo into your local machine.

### Pull Request
- pull request lifecycle

### Git fetch Vs Git Pull
- Fetch - Pulls the latest changes but will not merge the changes to the branch
        - it provides an option to review it and merge or rebase the changes
- Pull  - its a combination of git fetch and git merge/rebase

### Git Reset
- Add the feature files from 1-5 and test it
- When we want to undo the changes we use `git reset`
- `--sot` `--mixed` `--hard`
- Default is `--mixed` When you use `--mixed` it puts the file out of staging area
- `git reset --mixed 40b0188` (In my case it bring back the deleted file)
- `git restore file-name` to restore the file
- `git reset --soft` Puts the file in the staging area.
- `git reset --hard` Remove/Delete the file from the local as well as the history.

### Git Amend
- club multiple commits into single commit no need to make multiple commits
- Use `git commit --amend ` opens the last commit either you can add the comments or update the existing commit. New commit can also be the part of existing commit.


### Git Cherry Pick
- Pick particular commit and integrate it with our feature branch.
- B1 f1.txt f2.txt f4.txt. B2 f1.txt f2.txt f3.txt
- Taking f3.txt from B2 to B1
- Picking changes from one branch to another brnach is called cherry picking.
```
git checkout feature/branch2
git log --oneline (pick the commit msg)
git checkout feature/branch1
git cherry-pick <commit hash>
git push
```

### git rebase
- squash: Merge multiple commits into single commit.
`git rebase -i commit-id` Multiple commits into single commit

### git reorder
- We can correct the commit order. pick the commit before the commits you want to correct.
`git rebase -i  <commit-hash>` cut and paste the commit msg in the order you want.
