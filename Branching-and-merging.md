# Git Branching and Merging

## 1. What Is a Branch?

A branch is a separate line of development. It allows developers to work on a feature or bug fix independently of the main codebase.

For example:

- `main` — stable project code
- `feature/login` — login functionality
- `fix/navbar` — navigation bug fix

## 2. List Branches

```bash
git branch
```

Lists local branches. The current branch is marked with an asterisk.

## 3. Create a Branch

```bash
git branch feature/login
```

Creates a branch named `feature/login` without switching to it.

## 4. Create and Switch to a Branch

```bash
git switch -c feature/login
```

Creates the branch and switches to it.

## 5. Switch Between Branches

```bash
git switch main
```

Switches to the `main` branch.

Before switching, make sure your local changes are safely handled.

## 6. Merge a Branch

Suppose you have completed the login feature.

First, switch to the branch that should receive the changes:

```bash
git switch main
```

Then merge the feature branch:

```bash
git merge feature/login
```

This integrates the feature branch's changes into `main`.

## 7. Push a New Branch to GitHub

```bash
git push -u origin feature/login
```

Publishes the branch to GitHub and sets its upstream tracking branch.

## 8. Delete a Merged Branch

```bash
git branch -d feature/login
```

Deletes the local feature branch if Git considers it safely merged.

## 9. Example Team Workflow

1. Create a feature branch.
2. Implement the feature.
3. Test the changes.
4. Commit the changes.
5. Push the branch to GitHub.
6. Open a pull request for review.
7. Merge the approved changes into `main`.

## Conclusion

Branches support parallel development and help keep the main branch stable. Merging integrates completed work, while pull requests support review and collaboration.
