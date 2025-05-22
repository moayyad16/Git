# Git Version Control
Note:

This guide is designed to help you learn Git in Visual Studio Code (VS Code), which has great built-in support for viewing your commit and branch history visually via Git Graph and Source Control. 

## Getting Started
1. Create your repo on your GitHub account to `push` your work on it.
2. Go to VS Code and clone the repo using `ctrl+shift+p`, then write `git: clone` in the search bar. Or you can choose `Clone Git Repository ...` from the graphical user interface in VS Code.
   ![Screenshot 2025-05-22 192609](https://github.com/user-attachments/assets/17124f8b-18cb-4bd8-b4a1-34789fe8b933)
3. Enter your repo URL.
It may ask you to connect your GitHub account to VS Code; do so to follow up.

## Git commands that I frequently use 
#### 1. Check the status of your repo
```bash
git status
```
See if you have made changes to any file or added a new one. Also, to see which files are staged, unstaged, or untracked.

#### 2. List all branches
```bash
git branch
```
List of the branches that you have created. 

#### 3. Create a new branch
```bash
git branch my-branch-name
```
Create a new branch

#### 4. Switch to another branch 
```bash
git checkout my-branch-name
```

#### 5. Create and switch to a new branch
```bash
git checkout -b your-new-branch-name
```
This command combines the last two together by creating a new branch and switching to it immediately. 

#### 6. Stage and Unstage
```bash
git add .
```
To stage your changes to be pushed to the remote repo.
```bash
git reset
```
Unstage the staged files. You can use this to unstage all the files or to ensure that there is no staged one. 

To unstage a certain file, you can use: 
```bash
git reset file_name
```
#### 7. Commit
```bash
git commit -m "commit comment"
```
Commit my changes to the GitHub or the remote repository. 

#### 8. Stash
```bach
git stash
```
Hide the current changes in a hidden directory. 
```bach
git stash pop   
```
Restore the stashed files from the hidden directory. 

#### 9. Log
```bash
git log
```
Show the commit history

#### 10. Fetch
```bash
git fetch
```
Gets new commits or updates from GitHub or your remote repo. If many developers are working on the same repo, they may commit changes to the repo that you have to fetch to your local repo. 
### 11. Merge
```bach
git merge
```
Merge the fetched changes from the remote repo with your local repo work.

#### 12. Fetch and Merge
```bash
git pull --rebase
```
Combine fetch and merge, cleaner history in the commit graph

#### 13. Push
```bash
git push
```
Push your commit to the repo 


---

## Appendix: Key Git Concepts Explained

### What is Git?
**Git** is a distributed version control system used to track changes in source code during software development. It allows multiple developers to work on a project simultaneously, keeping a detailed history of every change.

- Helps in collaboration
- Allows rollback to previous versions
- Enables branching and merging
- Stores data efficiently


### What is a Branch?
A **branch** in Git is an independent line of development that allows you to work on new features or fixes without affecting the main codebase.

- `main` or `master` is usually the default branch
- Use `git branch <name>` to create a new branch
- Use `git checkout <name>` to move between branches

Branches are essential for working in parallel and testing changes before merging them into the main line.


### What is Staging?
The **staging area** is where you prepare a snapshot of your changes before committing them to the repository.

- Use `git add` to stage changes
- Only staged files are included in the next commit
- Think of it as a "preview" step


### What is a Commit?
A **commit** is a saved snapshot of your staged changes. Each commit has a unique ID and a message describing what was changed.

- Use `git commit -m "your message"` to commit
- Commits allow you to track progress and roll back if needed
- They form the building blocks of your project's history


### What is `git push`?

`git push` is the command used to upload your local branch's commits to a remote repository.

#### What it does:
- Transfers **commits** from your **local branch** to the **corresponding remote branch**
- If the remote branch doesn’t exist yet, it will be **created**
- Only **committed** changes are pushed — unstaged or uncommitted changes stay local


### What is a Local Repository?
A **local repository** is the copy of your project stored on your own machine. You do all your development work here.

- Contains all branches, commits, and files
- Git operations like `add`, `commit`, and `branch` work locally


### What is a Remote Repository?
A **remote repository** is a version of your project hosted on a server (e.g., GitHub, GitLab, Bitbucket) that you can push to or pull from.

- Use `git push` to upload your commits
- Use `git pull` or `git fetch` to get updates from others
- Supports team collaboration across machines


### What is Git Stash?
**Stashing** allows you to temporarily save (stash) changes you’re not ready to commit, so you can switch branches or pull updates without losing your work.

- Use `git stash` to hide changes
- Use `git stash pop` or `git stash apply` to bring them back
- Handy for context switching or resolving conflicts


### What is `git pull --rebase`?
`git pull --rebase` is an alternative to the standard `git pull` that integrates changes from the remote branch in a cleaner way.

- Instead of merging, it re-applies your local commits on top of the latest remote commits
- Creates a **linear commit history**
- Ideal for avoiding messy merge commits


## Refrences
1. [VS Code Source Control Overview](https://code.visualstudio.com/docs/sourcecontrol/overview)  
2. [Git Official Documentation](https://git-scm.com/doc)















