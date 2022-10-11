# GIT CONTROL

## General

GIT LOCAL includes:

- working directory
- staging area : ready to commit
- local repo

GIT REMOTE includes:

- remote repo

## Command line

### Configure

- **git config --global user.name "your name"**
- **git config --global user.email "your email"**
- **git config --list**

### Begin

- **git init**: Initialize empty git repo.
- **git remote add < origin > < https: remote >** link local repo to remote repo.
- **git remote -v**: info if remote.
- **git add < ., file, --all, -A >**: file will be staged in Staging Environment, ready to be committed to the repo you are working.
- **git rm --cached < file >**: unstage
- **git status < options: --short >**
- **git commit -m "your commit"**: move file from staging are to local repo.
- **git push -u origin branch < options: --force >**: local repo to remote repo.
- **git pull origin branch**: remote repo to local repo

### Branch

- **git branch -a**: see all branches
- **git branch < new branch >**: create a new branch.
- **git checkout < name branch >**: switch branch.
- **git switch < name branch >**: switch branch.
- **git checkout -b < name branch >**: create a new branch and switch branch.
- **git branch -d < branch name >**: delete a branch.

### Git merge

- **git merge < other branch >**: *<ins>Merge fast forward</ins>*. Merge current branch with other branch.
- **git merge --abort**: to abort the merge.
- **git merge < other branch > --no-ff**: merge *<ins>no fast forward</ins>*.
Ex:
Before merging: (HEAD)C1 <= C2 <= C3(origin)
After merging:
C1 <= C2 <= C3(origin) <= (HEAD)C4  
|____________________________|

### Git ignore (create file .gitignore)

Example:

- *.log: ignore all ".log" file.
- temp/ : ignore all files in any directory named "temp".

### Git revert

- **git revert HEAD --no-edit**: revert 1 commit without editing commit.

### Advanced git

- **git rebase**:
You are in branch B2. *"git rebase master"* will move B2 to master.( Can make merge no fast forward turn to merge fast forward. **<ins>Be carefull</ins>**).

- **git rebase --preserve-merges**
- **git reset < commit id >**: move back to a previous commit, discarding any changes that made after that commit.
- **git reset --hard**: change HEAD but not keep your working
- **git reset --soft**: change HEAD but still keep your working
- **git cherry-pick < branch >**: copy branch.
