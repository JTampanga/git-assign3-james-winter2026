# Git Tutorial Reflection

## Tutorial Completed

**Learn Git Branching** – [http://pcottle.github.io/learnGitBranching/]

---

## What I Learned

### 1. The Core Git Workflow

The tutorial reinforced the fundamental Git workflow: making changes to files in a working directory, staging those changes with `git add`, and then permanently recording them with `git commit`. Each commit is like a snapshot of the project at a specific point in time, not just a list of file differences, but a complete picture of what the repository looked like at that moment.

### 2. Commits and the Commit Graph

One of the most valuable things I learned is how Git thinks about history as a **directed acyclic graph (DAG)** of commits. Each commit points back to its parent, forming a chain. This makes it possible to trace the entire history of a project.

### 3. Branching

Git branches are simply **lightweight pointers** to a specific commit. Creating a new branch doesn't copy any files, it just creates a new label that moves forward as you add commits. This makes branching in Git extremely fast and cheap compared to older version control systems.

Key commands practiced:
```bash
git branch feature-branch     # create a new branch
git checkout feature-branch   # switch to it
git checkout -b new-branch     # create and switch in one step
```

### 4. Merging

After working on a feature branch, changes can be integrated back into the main branch using `git merge`. The tutorial showed how Git handles:
- **Fast-forward merges**: when the main branch has not diverged, Git simply moves the pointer forward
- **Three-way merges**: when both branches have new commits, Git creates a new merge commit combining both histories

### 5. Rebasing

`git rebase` is an alternative to merging. Instead of creating a merge commit, it **replays** your commits on top of another branch, resulting in a cleaner, linear history. This is useful for keeping a project history readable.

```bash
git rebase main   # replay current branch commits onto main
```

### 6. HEAD and Relative References

`HEAD` is a special pointer that tells Git which commit you are currently working from. The tutorial taught relative references:
- `HEAD~1` — one commit behind HEAD
- `HEAD^` — the parent of HEAD
- These are extremely useful for navigating history without needing to copy SHA hashes

### 7. Cherry-pick and Interactive Rebase

For more advanced workflows, `git cherry-pick` lets you copy specific commits onto the current branch, while `git rebase -i` (interactive rebase) lets you reorder, squash, or drop commits before sharing them.

---

## Key Takeaways

- Git is not just a backup tool — it is a **collaboration and history management system**
- Branching is cheap: use it freely for every feature or experiment
- Commit messages matter — they are your future self's notes on what changed and why
- Understanding `HEAD` and the commit graph makes advanced commands much less intimidating
- The visual, interactive format of *Learn Git Branching* made abstract concepts like DAGs and rebasing much easier to grasp than reading documentation alone

---

## Commands Reference Summary

| Command | Purpose |
|---------|---------|
| `git init` | Initialize a new local repository |
| `git add <file>` | Stage changes for commit |
| `git commit -m "message"` | Record staged changes |
| `git branch <name>` | Create a new branch |
| `git checkout <branch>` | Switch branches |
| `git merge <branch>` | Merge branch into current |
| `git rebase <branch>` | Rebase current branch onto another |
| `git log` | View commit history |
| `git log --oneline` | Compact commit history view |
| `git push origin main` | Push local commits to remote |
