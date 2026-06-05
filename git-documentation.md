# Git

## 1.Git Configuration
This is the git environment customization

```bash
git config --global user.name <name>
git config --global user.email <email>
```
---
## 2. Cloning an Existing Repository
If we want to get a copy of an existing Git repository
```bash
git clone <url>
```
---
## 3. Checking the Status of Files
The tool used to determine which files are in which state
```bash
git status
```
---

## 4. The Standard Workflow
### 4.1 Stage the files
To stage a single file
```
git add <filename>
```
To stage all the files
```
git add .
```
### 4.2 Removing Files
To remove a file from Git, we have to remove it from our tracked files and then commit
```
git rm <filename>
```
### 4.3 Commit the file
To commit a single file
```
git commit <filename>
```
To commit all the files
```
git commit .
```
### 4.4 Undoing Things
if we messup commit messages or missed some files during commiting we can undo the commit if it is too early
```
git commit -m "<Message>"
git add <file-name>
git commit --amend
```
### 4.5 To unstage the file
If we want to unstage the staged file in any scenario we can perform
```
git reset HEAD <filename>
```

### 4.6 To push the committed file into remote
To push the committed files from local repository to a remote repository:

If we already linked  branch to the remote repository previously, simply run:
```
git push
```
If we just created a new local branch and are pushing it to the remote for the first time
```
git push -u origin <branch-name>
```
---

## 5. Git Branching
### 5.1 To Create a new branch
```
git branch <branch_name>
```
### 5.2 Switching Branches
To switch to an existing branch
```
git checkout <branch_name>
```
### 5.3 To delete a Branch
```
git branch -d <branch_name>
```
### 5.4 Branch Management
To view the branches that are already merged and not merged we can use 
```
git branch --merged
```
and 
```
git branch --no-merged
```
---

## 6. Git cherry-pick Workflow
Used to apply the changes introduced by an individual, specific commit from one branch onto the currently checked-out branch without merging the entire history of the source branch
### 6.1 Find the commit hash
Switch to or inspect the branch containing the commit and grab its SHA identifier.
```
git log --oneline
```
### 6.2 Switch to the target branch
Navigate to the branch where we want to apply the changes.
```
git checkout <branch-name>
```

### 6.3 Execute the cherry-pick
Run the command followed by the commit hash.
```
git cherry-pick <commit-hash>
```

---