# Essential Git Commands

## 1. Repository Setup

### Check Git Version

```bash
git --version
```

Displays the installed Git version.

### Initialize a Repository

```bash
git init
```

Creates a new local repository in the current directory.

### Clone a Repository

```bash
git clone https://github.com/USERNAME/REPOSITORY.git
```

Downloads a remote repository and its history to your computer.

## 2. Check Changes

```bash
git status
```

Displays the state of the working directory and staging area.

```bash
git diff
```

Shows unstaged changes to tracked files.

```bash
git diff --staged
```

Shows changes that have been staged for the next commit.

```bash
git log --oneline
```

Displays a compact commit history.

## 3. Stage and Commit Changes

```bash
git add filename
```

Stages a specific file.

```bash
git add .
```

Stages changes under the current directory, subject to Git's ignore rules.

```bash
git commit -m "Add login validation"
```

Records staged changes with a descriptive message.

## 4. Remote Repository Commands

```bash
git remote -v
```

Displays configured remote repository URLs.

```bash
git remote add origin https://github.com/USERNAME/REPOSITORY.git
```

Adds a remote named `origin`.

```bash
git push -u origin main
```

Pushes the local `main` branch to `origin` and sets its upstream tracking branch.

```bash
git pull
```

Fetches changes from the configured upstream and integrates them into the current branch.

```bash
git fetch
```

Downloads remote updates without integrating them into the current branch.

## 5. Branch Commands

```bash
git branch
```

Lists local branches.

```bash
git switch -c feature/login
```

Creates and switches to a new branch.

```bash
git switch main
```

Switches to the `main` branch.

```bash
git merge feature/login
```

Merges the specified branch into the current branch.

```bash
git branch -d feature/login
```

Deletes a local branch that Git considers safely merged.

## 6. Undo and Recovery Commands

```bash
git restore filename
```

Discards unstaged changes in the specified file. Use carefully because those changes may be lost.

```bash
git restore --staged filename
```

Removes the specified file from the staging area without discarding its working-directory changes.

```bash
git revert COMMIT_ID
```

Creates a new commit that reverses the changes introduced by a specified commit.

```bash
git reset --soft HEAD~1
```

Moves the current branch back one commit while keeping the changes staged.

## 7. Configuration

```bash
git config --global user.name "Chethana Sri"
git config --global user.email "YOUR_EMAIL"
```

Sets the default author identity for your commits.

## 8. A Common Workflow

```bash
git status
git add .
git diff --staged
git commit -m "Describe the change"
git push
```

Review the staged changes before committing, and check the status if any command reports an error.

## Best Practices

- Write meaningful commit messages.
- Check `git status` regularly.
- Commit small, logical changes.
- Never commit passwords, API keys, or private credentials.
- Review changes before pushing to GitHub.
