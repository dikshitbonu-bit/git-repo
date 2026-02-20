# Git Commands Reference

 A living document of Git commands I'm learning during my DevOps journey.

---

## Table of Contents

1. [Setup & Config](#1-setup--config)
2. [Basic Workflow](#2-basic-workflow)
3. [Viewing Changes](#3-viewing-changes)
4. [Repository Management](#4-repository-management)
5. [Commit History](#5-commit-history)
6. [Undoing Changes](#6-undoing-changes)
7. [Branching](#7-branching)
8. [Remote Repositories](#8-remote-repositories)

---

## 1. Setup & Config

1. **Check Git version**
   - Command: `git --version`
   - Description: Check which version of Git is installed on your system.
   - Example: `git --version`

2. **Set global username**
   - Command: `git config --global user.name "Your Name"`
   - Description: Set your name for all Git commits.
   - Example: `git config --global user.name "DevOps Learner"`

3. **Set global email**
   - Command: `git config --global user.email "email@example.com"`
   - Description: Set your email for all Git commits.
   - Example: `git config --global user.email "learner@devops.local"`

4. **View all configurations**
   - Command: `git config --list`
   - Description: View all Git configuration settings.
   - Example: `git config --list`

---

## 2. Basic Workflow

1. **Initialize repository**
   - Command: `git init`
   - Description: Initialize a new Git repository in the current directory.
   - Example: `git init`

2. **Check status**
   - Command: `git status`
   - Description: Show the current state of your working directory and staging area.
   - Example: `git status`

3. **Add specific file**
   - Command: `git <add file>`
   - Description: Add file(s) to the staging area, preparing them for commit.
   - Example: `git add git-commands.md`

4. **Add all files**
   - Command: `git add .`
   - Description: Add all changed files in the current directory to staging.
   - Example: `git add .`

5. **Commit changes**
   - Command: `git commit -m "message"`
   - Description: Create a commit with the staged changes and a descriptive message.
   - Example: `git commit -m "Initial commit: Add git commands reference"`

---

## 3. Viewing Changes

1. **View commit history**
   - Command: `git log`
   - Description: Display the commit history with full details.
   - Example: `git log`

2. **Compact log view**
   - Command: `git log --oneline`
   - Description: Show commit history in compact, one-line-per-commit format.
   - Example: `git log --oneline`

3. **View unstaged changes**
   - Command: `git diff`
   - Description: Show changes in files that haven't been staged yet.
   - Example: `git diff`

4. **View staged changes**
   - Command: `git diff --staged`
   - Description: Show changes in files that are staged for commit.
   - Example: `git diff --staged`

---

## 4. Repository Management

1. **Explore .git directory**
   - Command: `ls -la .git/`
   - Description: Explore the contents of the hidden .git directory.
   - Example: `ls -la .git/`

2. **Remove file**
   - Command: `git rm <old file>`
   - Description: Remove a file from both working directory and staging area.
   - Example: `git rm oldfile.txt`

3. **Rename/move file**
   - Command: `git mv <old-file> <new-file>`
   - Description: Rename or move a file and stage the change.
   - Example: `git mv old-name.md new-name.md`

---

## 5. Commit History

1. **Graph view**
   - Command: `git log --graph`
   - Description: Display commit history with an ASCII graph showing branch structure.
   - Example: `git log --graph`

2. **Compact graph all branches**
   - Command: `git log --oneline --graph --all`
   - Description: Compact view of all branches with visual graph.
   - Example: `git log --oneline --graph --all`

3. **Show specific commit**
   - Command: `git show commit`
   - Description: Show detailed information about a specific commit.
   - Example: `git show ccc2e47`

4. **Limit commit count**
   - Command: `git log -n 5`
   - Description: Show only the last 5 commits.
   - Example: `git log -n 5`

---

## 6. Undoing Changes

1. **Restore file**
   - Command: `git <file>`
   - Description: Discard changes in working directory (unstage and revert to last commit).
   - Example: `git restore file.txt`

2. **Unstage file**
   - Command: `git restore --staged <file>`
   - Description: Unstage a file but keep the changes in working directory.
   - Example: `git restore --staged file.txt`

---

## 7. Branching

1. **List branches**
   - Command: `git branch`
   - Description: List all local branches in the repository.
   - Example: `git branch`

2. **Create branch**
   - Command: `git branch <name of the branch>`
   - Description: Create a new branch but don't switch to it.
   - Example: `git branch feature-1`

3. **Switch branch (legacy)**
   - Command: `git checkout branch `
   - Description: Switch to an existing branch.
   - Example: `git checkout feature-1`

4. **Create and switch (legacy)**
   - Command: `git checkout -b branch`
   - Description: Create a new branch and switch to it in one command.
   - Example: `git checkout -b feature-2`

5. **Switch branch (modern)**
   - Command: `git switch branch`
   - Description: Modern command to switch between branches (clearer than checkout).
   - Example: `git switch main`

6. **Create and switch (modern)**
   - Command: `git switch -c branch`
   - Description: Create a new branch and switch to it (modern alternative).
   - Example: `git switch -c feature-3`

7. **Delete merged branch**
   - Command: `git branch -d branch`
   - Description: Delete a branch (only if it's been merged).
   - Example: `git branch -d old-feature`

8. **Force delete branch**
   - Command: `git branch -D branch;`
   - Description: Force delete a branch even if not merged.
   - Example: `git branch -D experimental`

9. **Merge branch**
   - Command: `git merge branch`
   - Description: Merge specified branch into current branch.
   - Example: `git merge feature-1`

---

## 8. Remote Repositories

1. **Add remote**
   - Command: `git remote add origin <url>`
   - Description: Connect your local repo to a remote repository.
   - Example: `git remote add origin https://github.com/username/repo.git`

2. **View remotes**
   - Command: `git remote -v`
   - Description: View all configured remote repositories.
   - Example: `git remote -v`

3. **Push to remote**
   - Command: `git push <remote> <branch>`
   - Description: Upload your commits to a remote repository.
   - Example: `git push origin main`

4. **Push with upstream*
   - Command: `git push -u  <remote> <branch>`
   - Description: Push and set upstream tracking (for first push of a branch).
   - Example: `git push -u origin feature-1`

5. **Pull changes**
   - Command: `git pull  <remote> <branch>`
   - Description: Fetch changes from remote and merge into current branch.
   - Example: `git pull origin main`

6. **Fetch changes**
   - Command: `git fetch remote`
   - Description: Download changes from remote but don't merge them.
   - Example: `git fetch origin`

7. **Clone repository**
   - Command: `git clone <url>`
   - Description: Copy a remote repository to your local machine.
   - Example: `git clone https://github.com/username/repo.git`

8. **Push all branches**
   - Command: `git push --all`
   - Description: Push all branches to remote.
   - Example: `git push --all origin`

9. **Remove remote**
   - Command: `git remote remove origin`
   - Description: Remove a remote connection.
   - Example: `git remote remove origin`

---

## Quick Reference Cheat Sheet

```bash
# Start a new repository
git init
git add .
git commit -m "Initial commit"

# Create and switch to new branch
git switch -c feature-branch

# Push to remote
git push -u origin feature-branch

# Pull latest changes
git pull origin main

# View status and log
git status
git log --oneline

# Merge Commands
git merge feature-branch              # Merge (fast-forward if possible)
git merge --no-ff feature-branch      # Force merge commit
git merge --squash feature-branch     # Squash all commits into one

# Rebase Commands
git rebase main                       # Rebase current branch onto main
git rebase --continue                 # Continue after resolving conflicts
git rebase --abort                    # Cancel the rebase

# Stash Commands
git stash push -m "description"       # Stash with message
git stash list                        # List all stashes
git stash pop                         # Apply and delete latest stash
git stash apply stash@{0}             # Apply specific stash (keep it)
git stash drop stash@{0}              # Delete specific stash
git stash clear                       # Delete all stashes

# Cherry-Pick Commands
git cherry-pick abc1234               # Cherry-pick single commit
git cherry-pick A^..C                 # Cherry-pick range
git cherry-pick --continue            # Continue after resolving conflicts
git cherry-pick --abort               # Cancel the cherry-pick

# Visualization
git log --oneline --graph --all       # Visual commit history
```

# Reset Commands
git reset --soft HEAD~1
# Keep changes staged

git reset --mixed HEAD~1
# Keep changes unstaged (default)

git reset --hard HEAD~1
# Discard all changes (DESTRUCTIVE)

git reset --hard <commit-hash>
# Reset to specific commit

# Revert Commands
git revert <commit-hash>
# Create new commit that undoes target commit

git revert HEAD
# Revert last commit

git revert HEAD~3
# Revert commit 3 steps back

git revert --no-commit <commit-hash>
# Stage changes without committing

git revert --continue
# Continue after resolving conflicts

git revert --abort
# Cancel the revert

# Reflog (Recovery)
git reflog
# View all Git operations (safety net)

git reset --hard HEAD@{2}
# Recover to specific reflog entry
