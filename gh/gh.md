# Most Used GitHub CLI (`gh`) Commands


## 1. Authentication and Setup
- `gh auth login` – Log in to GitHub CLI  
- `gh auth logout` – Log out of GitHub CLI  
- `gh auth status` – Check authentication status  
- `gh config set editor <editor>` – Set default editor (e.g., `vim`, `nano`)  
- `gh version` – Show the installed GitHub CLI version  

## 2. Working with Repositories
- `gh repo create <repo-name>` – Create a new GitHub repository  
- `gh repo create --private` – Create a private repository  
- `gh repo create --public` – Create a public repository  
- `gh repo create --source=. --push` – Create a repository from the current directory and push it  
- `gh repo clone <repo-name>` – Clone a GitHub repository  
- `gh repo fork <repo-name>` – Fork a repository  

## 3. Managing Repositories
- `gh repo list` – List repositories for the authenticated user  
- `gh repo view <repo-name>` – View repository details  
- `gh repo edit --visibility private` – Change repository visibility to private  
- `gh repo delete <repo-name>` – Delete a repository  

## 4. Issues Management
- `gh issue list` – List open issues in the current repository  
- `gh issue create` – Create a new issue  
- `gh issue close <issue-number>` – Close an issue  
- `gh issue reopen <issue-number>` – Reopen an issue  
- `gh issue view <issue-number>` – View issue details  

## 5. Working with Pull Requests
- `gh pr list` – List open pull requests  
- `gh pr create` – Create a new pull request  
- `gh pr view <pr-number>` – View a specific pull request  
- `gh pr merge <pr-number>` – Merge a pull request  
- `gh pr close <pr-number>` – Close a pull request  
- `gh pr checkout <pr-number>` – Check out a pull request locally  

## 6. Working with Gists
- `gh gist create <file>` – Create a new gist  
- `gh gist list` – List all gists for the user  
- `gh gist view <gist-id>` – View a specific gist  
- `gh gist edit <gist-id>` – Edit a gist  
- `gh gist delete <gist-id>` – Delete a gist  

## 7. Managing Releases
- `gh release list` – List all releases in a repository  
- `gh release create <tag>` – Create a new release  
- `gh release edit <tag>` – Edit a release  
- `gh release delete <tag>` – Delete a release  

## 8. Managing SSH Keys
- `gh ssh-key add <key-file>` – Add an SSH key to GitHub  
- `gh ssh-key list` – List SSH keys for the authenticated user  
- `gh ssh-key delete <key-id>` – Remove an SSH key  

## 9. Managing Notifications
- `gh notification list` – List notifications  
- `gh notification mark-read` – Mark all notifications as read  
- `gh notification unsubscribe <thread-id>` – Unsubscribe from a notification thread  

## 10. Managing Actions and Workflows
- `gh run list` – List workflow runs in a repository  
- `gh run view <run-id>` – View details of a workflow run  
- `gh run cancel <run-id>` – Cancel a workflow run  
- `gh run rerun <run-id>` – Re-run a failed workflow  

---
