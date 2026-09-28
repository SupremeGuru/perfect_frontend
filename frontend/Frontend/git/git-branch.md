To branch with Git, the most efficient approach is to create and switch to a new branch simultaneously using the single command git switch -c <branch-name> or git checkout -b <branch-name>. [1, 2] 
## Standard Branching Workflow
Here is the recommended step-by-step workflow to safely create, work on, and publish a new branch:
## 1. Update your local repository
Before creating a branch, switch to your main codebase (usually main or master) and pull the latest changes: [3] 

git checkout main
git pull origin main

## 2. Create and switch to your new branch
Use the git switch command (available in Git 2.23+) with the -c (create) flag: [2] 

git switch -c feature-your-branch-name

Alternative older command: git checkout -b feature-your-branch-name. [1, 2] 
## 3. Verify your current branch
To confirm which branch you are actively working on, list your branches. The active branch will be highlighted with an asterisk (*): [4, 5] 

git branch

## 4. Push your branch to a remote server
Once you make changes and commit them locally, publish your branch to a remote repository like GitHub or GitLab: [3, 6] 

git push -u origin feature-your-branch-name

Note: The -u flag sets the upstream tracking, meaning you can just type git push for all future updates on this branch. [3, 7] 
------------------------------
## Useful Branch Management Commands

| Action | Command |
|---|---|
| Switch to an existing branch | git switch <branch-name> (or git checkout <branch-name>) |
| Delete a local branch (safely) | git branch -d <branch-name> |
| Force delete a local branch | git branch -D <branch-name> (use if changes were never merged) |
| Rename current branch | git branch -m <new-name> |
| List all local & remote branches | git branch -a |

For a complete breakdown of advanced branch manipulation, refer to the [Atlassian Git Branching Tutorial](https://www.atlassian.com/git/tutorials/using-branches) or the official reference guide on [Git-SCM Branching](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging). [1, 8] 
If you would like to proceed with the next steps, let me know if you want to learn how to merge your branch back into the main code or how to resolve merge conflicts. [1] 

[1] [https://git-scm.com](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)
[2] [https://git-scm.com](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell)
[3] [https://www.youtube.com](https://www.youtube.com/shorts/GdayzrwfKu8)
[4] [https://www.w3schools.com](https://www.w3schools.com/git/git_branch.asp?remote=github)
[5] [https://gitkraken.com](https://gitkraken.com/learn/git/branch)
[6] [https://www.youtube.com](https://www.youtube.com/watch?v=Wbz8zM_5iCc&t=127)
[7] [https://www.varonis.com](https://www.varonis.com/blog/git-branching-and-merging)
[8] [https://www.atlassian.com](https://www.atlassian.com/git/tutorials/using-branches)
