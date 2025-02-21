# Git Command Reference


## 1. Getting Started
- `git init` – Initialize a new Git repository  
- `git clone <repo_url>` – Clone an existing repository  
- `git config --global user.name "<Your Name>"` – Set the global username  
- `git config --global user.email "<Your Email>"` – Set the global email  
- `git config --list` – View all global configurations  

## 2. Working with Repositories
- `git status` – Check the current status of the working directory  
- `git add <file>` – Stage a specific file for commit  
- `git add .` – Stage all files in the working directory  
- `git reset <file>` – Unstage a file (move it back to working state)  
- `git reset --hard` – Reset the working directory to the last committed state  

## 3. Committing Changes
- `git commit -m "<commit_message>"` – Commit staged changes with a message  
- `git commit -am "<commit_message>"` – Add and commit changes in one command  
- `git commit --amend` – Modify the last commit (useful for fixing commit messages)  
- `git log` – View commit history  
- `git log --oneline` – View commit history in a single-line format  

## 4. Branching
- `git branch` – List all branches  
- `git branch <branch_name>` – Create a new branch  
- `git checkout <branch_name>` – Switch to a specific branch  
- `git checkout -b <branch_name>` – Create and switch to a new branch  
- `git branch -d <branch_name>` – Delete a local branch  

## 5. Merging and Rebasing
- `git merge <branch_name>` – Merge a branch into the current branch  
- `git rebase <branch_name>` – Reapply commits on top of another branch  
- `git cherry-pick <commit_hash>` – Apply a specific commit to the current branch  
- `git diff <branch1> <branch2>` – Compare differences between branches  
- `git diff` – Show changes in the working directory  

## 6. Remote Repositories
- `git remote -v` – View remote repositories  
- `git remote add <name> <url>` – Add a remote repository  
- `git remote remove <name>` – Remove a remote repository  
- `git fetch <remote>` – Fetch changes from a remote repository  
- `git pull <remote> <branch>` – Pull changes from a remote branch  

## 7. Pushing Changes
- `git push <remote> <branch>` – Push changes to a remote repository  
- `git push -u <remote> <branch>` – Push and set upstream tracking for a branch  
- `git push --force` – Force push (be cautious, this rewrites history)  
- `git push --tags` – Push tags to a remote repository  

## 8. Stashing Changes
- `git stash` – Stash uncommitted changes  
- `git stash list` – Show list of stashed changes  
- `git stash apply` – Apply the last stashed changes  
- `git stash pop` – Apply and remove the last stashed changes  
- `git stash drop` – Delete the last stashed changes  

## 9. Undoing Changes
- `git checkout -- <file>` – Discard changes in a file  
- `git revert <commit_hash>` – Revert a commit by creating a new commit  
- `git reset --soft HEAD~1` – Undo the last commit but keep changes staged  
- `git reset --hard HEAD~1` – Undo the last commit and discard changes  
- `git clean -f` – Remove untracked files  

## 10. Tagging
- `git tag` – List all tags  
- `git tag -a <tag_name> -m "<message>"` – Create an annotated tag  
- `git tag -d <tag_name>` – Delete a local tag  
- `git push <remote> --tags` – Push tags to a remote repository  
- `git show <tag_name>` – Show details of a tag  

---

This list covers **the top 50 essential Git commands** that you’ll use regularly. 🚀  
For more advanced Git usage, explore **Git rebase, interactive commits, and hooks**.