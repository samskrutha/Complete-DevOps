# Git Guide and Commands

## Table of Contents
1. [Introduction to Git](#introduction-to-git)
2. [Getting Started](#getting-started)
3. [Basic Git Commands](#basic-git-commands)
4. [Branching and Merging](#branching-and-merging)
5. [Advanced Git Commands](#advanced-git-commands)
6. [Git Configuration](#git-configuration)
7. [Git Workflows](#git-workflows)
8. [Additional Resources](#additional-resources)

## Introduction to Git
Git is a distributed version control system designed to handle everything from small to very large projects with speed and efficiency. It allows multiple developers to work on a project simultaneously without overwriting each other’s changes.

## Getting Started

### Installing Git
- **Windows**: Download from [gitforwindows.org](https://gitforwindows.org).
- **macOS**: Install via Homebrew: `brew install git`.
- **Linux**: Install via package manager, e.g., `sudo apt-get install git` on Debian-based distributions.

### Configuring Git
Set up your Git configuration by providing your name and email. These will be used in your commits.

```sh
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## Basic Git Commands

### Initializing a Repository
```sh
git init
```
Initializes a new Git repository.

### Cloning a Repository
```sh
git clone <repository-url>
```
Creates a local copy of a remote repository.

### Checking Repository Status
```sh
git status
```
Displays the state of the working directory and the staging area.

### Adding Changes
```sh
git add <file>
git add .
```
Stages changes for the next commit. `.` stages all changes.

### Committing Changes
```sh
git commit -m "Commit message"
```
Records the changes in the repository.

### Viewing Commit History
```sh
git log
```
Shows the commit history for the repository.

### Viewing Changes
```sh
git diff
```
Shows changes between commits, commit and working tree, etc.

### Removing Files
```sh
git rm <file>
```
Removes a file from the working directory and stages the removal.

### Moving/Renaming Files
```sh
git mv <oldfile> <newfile>
```
Moves or renames a file.

### Ignoring Files
Create a `.gitignore` file to ignore specific files and directories.

### Restoring Changes
```sh
git checkout -- <file>
```
Restores the file from the latest commit.

## Branching and Merging

### Creating a New Branch
```sh
git branch <branch-name>
```
Creates a new branch.

### Listing Branches
```sh
git branch
```
Lists all branches.

### Switching Branches
```sh
git checkout <branch-name>
```
Switches to the specified branch.

### Merging Branches
```sh
git merge <branch-name>
```
Merges the specified branch into the current branch.

### Deleting a Branch
```sh
git branch -d <branch-name>
```
Deletes the specified branch.

### Rebasing Branches
```sh
git rebase <branch-name>
```
Rebases the current branch onto the specified branch.

## Advanced Git Commands

### Stashing Changes
```sh
git stash
```
Temporarily saves changes that are not ready to be committed.

### Applying Stash
```sh
git stash apply
```
Applies the stashed changes.

### Dropping Stash
```sh
git stash drop
```
Deletes the stashed changes.

### Cherry-picking Commits
```sh
git cherry-pick <commit-hash>
```
Applies the changes from a specific commit.

### Resetting Commits
```sh
git reset --hard <commit-hash>
```
Resets the current branch to a specific commit.

### Reverting Commits
```sh
git revert <commit-hash>
```
Creates a new commit that undoes the changes from a specific commit.

### Viewing Remote Repositories
```sh
git remote -v
```
Displays remote repositories.

### Adding a Remote Repository
```sh
git remote add <name> <url>
```
Adds a new remote repository.

### Fetching Changes
```sh
git fetch
```
Fetches changes from the remote repository.

### Pulling Changes
```sh
git pull
```
Fetches and merges changes from the remote repository.

### Pushing Changes
```sh
git push
```
Uploads local changes to the remote repository.

### Tagging Commits
```sh
git tag <tag-name>
```
Creates a new tag.

## Git Configuration

### Listing Configuration
```sh
git config --list
```
Displays all Git configurations.

### Setting Aliases
```sh
git config --global alias.<alias-name> <git-command>
```
Creates a shortcut for a Git command.

### Configuring Line Endings
```sh
git config --global core.autocrlf true
```
Configures automatic conversion of line endings.

## Git Workflows

### Feature Branch Workflow
- Create a new branch for each feature.
- Merge the feature branch into the main branch once the feature is complete.

### Forking Workflow
- Fork a repository.
- Clone the forked repository.
- Create a branch, make changes, and push to your fork.
- Open a pull request to the original repository.

### Gitflow Workflow
- Uses multiple branches (main, develop, feature, release, hotfix).
- Structured workflow for managing releases and hotfixes.

## Additional Resources

- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Learning Lab](https://lab.github.com/)
- [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials)

---
