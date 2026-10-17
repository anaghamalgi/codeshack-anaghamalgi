# Git Notes: 10 Essential Git Commands

Git is a version control system that helps developers track changes to files, maintain project history, and collaborate with others through platforms such as GitHub.

## 1. `git init`

**Purpose:** Creates a new Git repository in the current directory. Use this when starting version control for a project that is not already a Git repository.

**Example:**
```bash
git init
```

**When to use it:** When starting a new local project and wanting Git to track its changes.

## 2. `git clone`

**Purpose:** Copies an existing remote repository to your computer, including its files and Git history.

**Example:**
```bash
git clone https://github.com/username/project.git
```

Replace the URL with the actual URL of the repository you want to copy.

**When to use it:** When joining an existing project or downloading your repository onto another computer.

## 3. `git status`

**Purpose:** Shows the current branch and which files are untracked, modified, staged, or ready to commit.

**Example:**
```bash
git status
```

**When to use it:** Frequently—especially before staging, committing, or pushing changes.

## 4. `git add`

**Purpose:** Stages changes so they can be included in the next commit. Staging lets you choose which changes to save.

**Example:**
```bash
git add README.md
```

To stage all changes in the current directory:
```bash
git add .
```

**When to use it:** After editing or creating files and before making a commit.

## 5. `git commit`

**Purpose:** Saves staged changes as a new commit in the local repository's history. A commit should have a clear message describing the change.

**Example:**
```bash
git commit -m "Add Git command notes"
```

**When to use it:** After staging a useful, logical set of changes.

## 6. `git log`

**Purpose:** Displays the repository's commit history, including commit IDs, authors, dates, and messages.

**Example:**
```bash
git log --oneline
```

**When to use it:** To review previous work and check which commits have been made.

## 7. `git diff`

**Purpose:** Shows differences between file versions. By default, it displays changes in tracked files that have not yet been staged.

**Example:**
```bash
git diff
```

To see changes that are already staged:
```bash
git diff --staged
```

**When to use it:** Before staging or committing, to review exactly what changed.

## 8. `git push`

**Purpose:** Uploads local commits to a remote repository such as GitHub.

**Example:**
```bash
git push origin main
```

This example pushes the local `main` branch to the remote named `origin`. Your remote and branch must be configured, and you need permission to push.

**When to use it:** After committing changes that you want to share on GitHub.

## 9. `git pull`

**Purpose:** Fetches updates from a remote repository and integrates them into your current branch, usually by merging.

**Example:**
```bash
git pull origin main
```

Run this while on the local branch that should receive the remote `main` branch's changes. Check your branch and working tree first.

**When to use it:** To bring remote changes into your current local branch before continuing work.

## 10. `git fetch`

**Purpose:** Downloads new commits and references from a remote repository without merging those changes into your current branch.

**Example:**
```bash
git fetch origin
```

After fetching, you can inspect the remote updates before deciding whether to merge or rebase them.

**When to use it:** To check for updates from GitHub without immediately changing your current branch's files.

## A Typical Git Workflow

A common workflow for editing a file and sharing the change is:

```bash
git status
git diff
git add README.md
git diff --staged
git commit -m "Update README"
git push origin main
```

Use the appropriate branch name for your own project. In a team repository, work on your assigned feature branch rather than committing directly to `main`.

## Summary

- `git init` starts a new local repository.
- `git clone` copies an existing repository.
- `git status` checks the state of your files.
- `git add` stages changes.
- `git commit` records staged changes.
- `git log` displays commit history.
- `git diff` reviews changes.
- `git push` uploads commits.
- `git pull` fetches and integrates remote changes.
- `git fetch` downloads remote updates without integrating them.

Learning these commands provides a foundation for tracking project changes and collaborating with Git and GitHub.
