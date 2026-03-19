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
- When we want to undo the changes we use `git reset`
- `--sot` `--mixed` `--hard`





