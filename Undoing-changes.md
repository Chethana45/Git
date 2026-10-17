# Undoing Changes in Git

## 1. Introduction

Git provides several commands for undoing changes. The correct command depends on whether the changes are unstaged, staged, committed, or already pushed.

Always check the repository status before using commands that may discard work.

## 2. Discard Unstaged Changes

```bash
git restore filename
```

Restores the file to its index version, discarding unstaged changes to that file.

**Warning:** The discarded changes may not be recoverable.

## 3. Unstage a File

```bash
git restore --staged filename
```

Removes a file from the staging area while keeping its working-directory changes.

## 4. Modify the Most Recent Commit

```bash
git commit --amend
```

Allows you to modify the most recent commit, including its message or staged content.

Avoid amending commits that have already been shared with teammates unless you coordinate the history rewrite.

## 5. Revert a Commit

```bash
git revert COMMIT_ID
```

Creates a new commit that reverses the changes introduced by the specified commit.

This is generally suitable for undoing a published change while preserving project history.

## 6. Reset to an Earlier Commit

### Soft Reset

```bash
git reset --soft HEAD~1
```

Moves the current branch back one commit while keeping the changes staged.

### Mixed Reset

```bash
git reset --mixed HEAD~1
```

Moves the current branch back one commit and leaves the changes unstaged in the working directory. This is the default reset mode.

### Hard Reset

```bash
git reset --hard HEAD~1
```

Moves the current branch back one commit and resets tracked files to that state.

**Warning:** This can permanently discard uncommitted changes. Use it only when you understand the consequences.

## 7. Recover Using the Reflog

```bash
git reflog
```

Shows recent movements of local references such as `HEAD`. It can help locate commits that are no longer visible in the current branch history.

Inspect the relevant commit before attempting recovery.

## 8. Which Command Should You Use?

| Situation | Command |
|---|---|
| Discard unstaged file changes | `git restore filename` |
| Unstage a file | `git restore --staged filename` |
| Undo a published commit | `git revert COMMIT_ID` |
| Move back while keeping changes staged | `git reset --soft HEAD~1` |
| Inspect recent reference history | `git reflog` |

## Conclusion

Choose a recovery command based on the state of your changes. Prefer `git revert` for undoing published commits, and use destructive commands with caution.
