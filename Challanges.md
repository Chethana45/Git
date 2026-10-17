# Git & GitHub Challenges

A hands-on challenge collection to practice Git commands, version control, branching, merging, and collaboration.

Try solving each challenge yourself before looking up the commands.

## Level 1: Beginner Challenges

### Challenge 1: Initialize a Repository
- Create a folder named `git-challenge`.
- Initialize a Git repository inside it.
- Create a `README.md` file.
- Make your first commit.

**Goal:** Practice `git init`, `git add`, and `git commit`.

### Challenge 2: Track Multiple Files
- Create three files: `index.html`, `style.css`, and `script.js`.
- Stage all three files.
- Commit them with a meaningful message.

**Goal:** Understand staging and commits.

### Challenge 3: Inspect Changes
- Modify one of your files.
- View the differences before staging.
- Stage the file and view the staged differences.
- Commit the change.

**Goal:** Practice `git status`, `git diff`, and `git diff --staged`.

### Challenge 4: Write Good Commit Messages
Create three separate commits with descriptive messages.

Examples:
- `Add navigation section`
- `Fix button alignment`
- `Update project documentation`

**Goal:** Learn to maintain a readable history.

## Level 2: Branching Challenges

### Challenge 5: Create a Feature Branch
- Create a branch named `feature/profile`.
- Add a `profile.md` file.
- Commit your changes.
- Switch back to `main`.

**Goal:** Practice branch creation and switching.

### Challenge 6: Merge a Feature
- Merge `feature/profile` into `main`.
- Inspect the commit history.
- Delete the local feature branch after confirming it is merged.

**Goal:** Practice merging and branch cleanup.

### Challenge 7: Work on Two Features
Create two branches:
- `feature/login`
- `feature/dashboard`

Implement a separate file on each branch and merge both into `main`.

**Goal:** Understand independent feature development.

## Level 3: Merge Conflict Challenges

### Challenge 8: Create Your First Conflict
- Create `message.txt` on `main`.
- Create a branch named `feature/message`.
- Change the same line differently on both branches.
- Commit each change.
- Merge the feature branch into `main`.
- Resolve the conflict manually.

**Goal:** Understand conflict markers and resolution.

### Challenge 9: Resolve a Conflict Carefully
Create a conflict in a Markdown file. Instead of choosing one entire version, combine the intended information from both branches into a correct final version.

**Goal:** Resolve conflicts without accidentally losing useful changes.

## Level 4: Remote Repository Challenges

### Challenge 10: Push to GitHub
- Create an empty GitHub repository.
- Connect your local repository to it.
- Push your `main` branch.
- Verify that your files appear on GitHub.

**Goal:** Practice `git remote`, `git push`, and upstream tracking.

### Challenge 11: Clone and Update
- Clone your repository into another folder.
- Add a file and commit it in the original copy.
- Fetch the updates in the cloned copy.
- Inspect the changes and integrate them.

**Goal:** Understand `git clone`, `git fetch`, and `git pull`.

### Challenge 12: Handle Remote Changes
Make a change on GitHub's website, then make a separate local change. Fetch the remote update and integrate both sets of changes safely.

**Goal:** Practice synchronizing local and remote work.

## Level 5: Recovery Challenges

### Challenge 13: Unstage a File
Stage a file, then remove it from the staging area without discarding the changes.

**Goal:** Use `git restore --staged`.

### Challenge 14: Undo a Commit Safely
Create a commit and reverse it using `git revert`.

**Goal:** Understand how Git preserves history when reversing a change.

### Challenge 15: Investigate Your History
Use `git log --oneline --graph --all` and `git reflog` to inspect commit history and recent reference movements.

**Goal:** Learn to investigate repository history.

## Level 6: Advanced Challenges

### Challenge 16: Build a `.gitignore`
Create a `.gitignore` file that excludes:
- `node_modules/`
- `.env`
- `dist/`
- `*.log`

Verify the behavior with untracked sample files. Remember that `.gitignore` does not automatically untrack files already committed.

### Challenge 17: Simulate a Team Workflow
- Create a feature branch.
- Implement a small feature.
- Push the branch to GitHub.
- Open a pull request.
- Review the changes and merge the pull request.

**Goal:** Practice a standard collaborative workflow.

### Challenge 18: Diagnose a Failed Push
In a disposable test repository, create a remote commit that your local branch does not contain. Attempt to push your local commit, inspect the error, fetch the remote changes, integrate them, and push again.

**Goal:** Understand why non-fast-forward push rejections occur.

## Completion Checklist

- [ ] Completed all beginner challenges.
- [ ] Created and merged feature branches.
- [ ] Resolved a merge conflict.
- [ ] Pushed and cloned a GitHub repository.
- [ ] Practiced safe recovery commands.
- [ ] Configured a `.gitignore` file.
- [ ] Completed a pull request workflow.
- [ ] Documented the commands learned.

## Final Goal

Complete these challenges in a dedicated practice repository. Record the commands you used and the problems you encountered so this collection becomes a practical reference for future projects and technical interviews.
