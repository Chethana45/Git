# Git Basics

## 1. What Is Git?

Git is a distributed version control system used to track changes in source code and other files. It helps developers maintain project history, collaborate with others, and return to earlier versions when necessary.

### Why Do We Use Git?

- Tracks changes over time.
- Maintains a history of commits.
- Supports parallel development through branches.
- Helps developers collaborate.
- Makes it possible to recover earlier versions of files.

## 2. What Is GitHub?

GitHub is an online platform for hosting Git repositories. It provides tools for collaboration, code reviews, pull requests, issue tracking, and project management.

**Git vs GitHub**

| Git | GitHub |
|---|---|
| Version control software | Online code hosting platform |
| Works locally | Hosts repositories remotely |
| Tracks file changes | Enables collaboration |
| Can work offline | Requires internet for online operations |

## 3. Important Git Terminology

### Repository
A repository, or repo, stores project files and their version history.

### Working Directory
The directory containing the files you are currently editing.

### Staging Area
A temporary area where you select changes to include in the next commit.

### Commit
A recorded snapshot of staged changes.

### Branch
An independent line of development.

### Remote
A reference to a repository hosted elsewhere, such as GitHub.

### Merge
The process of combining changes from different branches.

## 4. The Git Workflow

1. Edit files in the working directory.
2. Stage the changes.
3. Commit the staged changes.
4. Push commits to a remote repository when needed.

```text
Working Directory
       |
       | git add
       v
Staging Area
       |
       | git commit
       v
Local Repository
       |
       | git push
       v
Remote Repository (GitHub)
```

## 5. Install and Configure Git

Check the installed version:

```bash
git --version
```

Configure your name:

```bash
git config --global user.name "Chethana Sri"
```

Configure your email:

```bash
git config --global user.email "YOUR_EMAIL"
```

Check the configuration:

```bash
git config --list
```

Use an email you intend to associate with your Git commits.

## 6. Initialize a Repository

```bash
mkdir git-practice
cd git-practice
git init
```

This creates a local Git repository in the current directory.

## 7. Check Repository Status

```bash
git status
```

This shows the current branch, staged changes, unstaged changes, and untracked files.

## 8. Summary

Git tracks changes, commits record snapshots, branches support parallel work, and GitHub hosts repositories for sharing and collaboration.
