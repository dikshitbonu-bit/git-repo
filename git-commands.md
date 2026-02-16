###Git Commands Reference
A living document of Git commands I'm learning during my DevOps journey.
================================================================================
###Setup & Config

git --version
Check which version of Git is installed on your system.
Example: git --version

git config --global user.name "Your Name"
Set your name for all Git commits.
Example: git config --global user.name "DevOps Learner"

git config --global user.email "email@example.com"
Set your email for all Git commits.
Example: git config --global user.email "learner@devops.local"

git config --list
View all Git configuration settings.
Example: git config --list
================================================================================
###Basic Workflow

git init
Initialize a new Git repository in the current directory.
Example: git init

git status
Show the current state of your working directory and staging area.
Example: git status

git add <file>
Add file(s) to the staging area, preparing them for commit.
Example: git add git-commands.md

git add .
Add all changed files in the current directory to staging.
Example: git add .

git commit -m "message"
Create a commit with the staged changes and a descriptive message.
Example: git commit -m "Initial commit: Add git commands reference"
================================================================================
###Viewing Changes

git log
Display the commit history with full details.
Example: git log

git log --oneline
Show commit history in compact, one-line-per-commit format.
Example: git log --oneline

git diff
Show changes in files that haven't been staged yet.
Example: git diff

git diff --staged
Show changes in files that are staged for commit.
Example: git diff --staged
================================================================================
###Repository Management

ls -la .git/
Explore the contents of the hidden .git directory.
Example: ls -la .git/

git rm <file>
Remove a file from both working directory and staging area.
Example: git rm oldfile.txt

git mv <old> <new>
Rename or move a file and stage the change.
Example: git mv old-name.md new-name.md
================================================================================
###Commit History

git log --graph
Display commit history with an ASCII graph showing branch structure.
Example: git log --graph

git log --oneline --graph --all
Compact view of all branches with visual graph.
Example: git log --oneline --graph --all

git show <commit>
Show detailed information about a specific commit.
Example: git show ccc2e47

git log -n 5
Show only the last 5 commits.
Example: git log -n 5
================================================================================
