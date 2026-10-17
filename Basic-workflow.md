# Git Practical Exercises

These exercises demonstrate the Git workflow in a separate practice repository.

## Exercise 1: Create a Repository

```bash
mkdir git-practice
cd git-practice
git init
```

**Expected result:** Git initializes a repository in the current directory.

## Exercise 2: Create and Commit a File

Create a file named `hello.txt` containing:

```text
Hello, Git!
This is my first Git practice.
```

Then run:

```bash
git status
git add hello.txt
git commit -m "Add hello text file"
git log --oneline
```

**Expected result:** Git records the file in a commit.

## Exercise 3: Modify a File

Add another line to `hello.txt`:

```text
Learning version control step by step.
```

Run:

```bash
git diff
git add hello.txt
git diff --staged
git commit -m "Update hello text"
```

**Expected result:** You can inspect changes before recording them.

## Exercise 4: Create a Branch

```bash
git switch -c feature/greeting
```

Edit `hello.txt`, then commit the change:

```bash
git add hello.txt
git commit -m "Add greeting feature"
```

**Expected result:** The feature branch contains a new commit.

## Exercise 5: Merge the Branch

```bash
git switch main
git merge feature/greeting
```

**Expected result:** Git integrates the feature branch into `main`, provided the merge can be completed.

## Exercise 6: Inspect the History

```bash
git log --oneline --graph --all
```

**Expected result:** A compact graph of the repository's commit history.

## Exercise 7: Connect to GitHub

Create an empty repository on GitHub named `git-practice`. Then connect your local repository:

```bash
git remote add origin https://github.com/USERNAME/git-practice.git
git push -u origin main
```

Replace `USERNAME` with your GitHub username.

If the remote repository already contains commits, or your local branch has a different name, you may need to integrate the remote history or adjust the commands first.

## Exercise 8: Check Your Status

```bash
git status
```

Confirm that there are no unexpected changes remaining.

## Completion Checklist

- [ ] Initialized a repository
- [ ] Created and committed a file
- [ ] Inspected changes using `git diff`
- [ ] Created a feature branch
- [ ] Merged a branch
- [ ] Inspected commit history
- [ ] Pushed a repository to GitHub

## Final Learning Goal

After completing these exercises, you should understand the basic Git workflow and be ready to practice version control in your own software projects.
