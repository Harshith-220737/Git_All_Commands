# Git Merge & Integration Commands

---

# 🔀 Introduction to Merge

Merging in Git means combining changes from one branch into another.

Most commonly:

- You create a feature branch
- Work on it
- Merge it back into `main`

---

# 1️⃣ git merge

### 🔹 Command

```bash
git merge <branch-name>
```

### 🔹 Purpose

Combines another branch into your current branch.

### 🔹 Simple Explanation

This command tells Git:

> "Take the changes from this branch and add them to the branch I am currently on."

### 🔹 Example Workflow

```bash
git switch main
git merge feature-login
```

This merges `feature-login` into `main`.

### 🔹 What Happens Internally?

- Git combines changes
- If no conflicts → automatic merge
- If conflicts → asks you to resolve them manually

### 🔹 Use Case

Used after completing a feature branch.

---

# 2️⃣ git merge --no-ff

### 🔹 Command

```bash
git merge --no-ff <branch-name>
```

### 🔹 Purpose

Forces Git to create a merge commit even if a fast-forward merge is possible.

### 🔹 Simple Explanation

Normally, if no new commits exist in the target branch, Git may simply move the pointer forward (called Fast-Forward merge).

With `--no-ff`, Git always creates a separate merge commit.

### 🔹 Example

```bash
git switch main
git merge --no-ff feature-payment
```

### 🔹 Why Use --no-ff?

- Keeps branch history visible
- Clearly shows when a feature was merged
- Preferred in professional team projects

---

# 🔥 Fast-Forward vs No Fast-Forward

## ✅ Fast-Forward (Default)

- No merge commit created
- Cleaner history
- But feature branch history becomes less visible

## ✅ No Fast-Forward (--no-ff)

- Creates merge commit
- Clear branch structure in history
- Better for team collaboration

---

# 🔥 Summary Table

| Command           | Main Purpose                     |
| ----------------- | -------------------------------- |
| git merge         | Merge branch into current branch |
| git merge --no-ff | Merge with explicit merge commit |

---

✅ These commands are used to integrate completed feature branches into main development branches in professional workflows.
