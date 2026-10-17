# Understanding and Resolving Git Merge Conflicts

## 1. What Is a Merge Conflict?

A merge conflict occurs when Git cannot automatically combine changes from different branches. This often happens when two branches modify the same lines of a file differently.

Git needs the developer to decide which changes to keep.

## 2. How Does a Conflict Occur?

Suppose the `main` branch contains:

```text
Welcome to the project
```

A feature branch changes the line to:

```text
Welcome to our application
```

Meanwhile, another branch changes the same line to:

```text
Welcome to the platform
```

Git may be unable to determine which version is correct.

## 3. Conflict Markers

Git may mark the conflicting section like this:

```text
<<<<<<< HEAD
Welcome to our application
=======
Welcome to the platform
>>>>>>> feature/platform
```

- `<<<<<<< HEAD` marks the current branch's version.
- `=======` separates the competing changes.
- `>>>>>>> feature/platform` marks the incoming branch's version.

The actual branch labels may differ.

## 4. Steps to Resolve a Conflict

### Step 1: Check the Repository Status

```bash
git status
```

Git identifies files with unresolved conflicts.

### Step 2: Open the Conflicted File

Review both versions and decide how the final content should look.

For example, you might choose:

```text
Welcome to our application platform
```

Use wording appropriate to the actual project rather than blindly combining both versions.

### Step 3: Remove Conflict Markers

Edit the file so that it contains the intended final content. Remove the `<<<<<<<`, `=======`, and `>>>>>>>` markers.

### Step 4: Stage the Resolved File

```bash
git add filename
```

This tells Git that you have resolved the conflict in that file.

### Step 5: Complete the Merge

```bash
git status
```

Review the status. If the merge is still in progress, complete it with:

```bash
git commit
```

Git may open an editor containing a default merge commit message.

## 5. Abort a Merge

If you want to cancel an in-progress merge before completing it:

```bash
git merge --abort
```

This attempts to restore the pre-merge state. Save or back up important work before doing so.

## 6. Best Practices

- Review both sides of a conflict carefully.
- Communicate with teammates when changes overlap.
- Test the result after resolving conflicts.
- Never remove conflict markers without reviewing the code.
- Make sure the final file contains no unresolved conflict markers.

## Conclusion

Merge conflicts are normal during collaborative development. Understanding the conflicting changes and carefully choosing the final content helps maintain correct, reliable code.
