# Git Rebasing Commands

---

# 🔁 Introduction to Rebase

Rebasing is used to move or reapply commits from one branch onto another.

It is often used to:

- Keep commit history clean
- Avoid unnecessary merge commits
- Maintain a linear project history

⚠️ Important:
Rebase rewrites commit history. Be careful when using it in shared branches.

---

# 1️⃣ git rebase

### 🔹 Command

```bash
git rebase <branch-name>
```

### 🔹 Purpose

Moves your current branch commits on top of another branch.

### 🔹 Simple Explanation

This command says:

> "Take my commits and replay them on top of this branch."

### 🔹 Example

```bash
git switch feature-login
git rebase main
```

### 🔹 What Happens?

- Git temporarily removes your commits
- Updates branch with latest changes
- Reapplies your commits one by one

### 🔹 Use Case

Used to update feature branch with latest changes from main without creating merge commits.

---

# 2️⃣ git rebase -i

### 🔹 Command

```bash
git rebase -i <commit-id>
```

### 🔹 Purpose

Interactive rebase for editing commit history.

### 🔹 Simple Explanation

Allows you to:

- Reorder commits
- Edit commit messages
- Combine (squash) commits
- Delete commits

### 🔹 Example

```bash
git rebase -i HEAD~3
```

This opens editor to modify last 3 commits.

### 🔹 Use Case

Used to clean up commit history before pushing.

---

# 3️⃣ git rebase --continue

### 🔹 Command

```bash
git rebase --continue
```

### 🔹 Purpose

Continues rebase process after resolving conflicts.

### 🔹 Simple Explanation

If Git stops due to conflict during rebase:

1. Fix conflict manually
2. Stage fixed files
3. Run `git rebase --continue`

This tells Git to continue applying remaining commits.

---

# 4️⃣ git rebase --abort

### 🔹 Command

```bash
git rebase --abort
```

### 🔹 Purpose

Cancels the rebase process completely.

### 🔹 Simple Explanation

If something goes wrong during rebase, this command says:

> "Stop everything and return to original state."

### 🔹 Use Case

Used when conflicts become complicated or rebase was started by mistake.

---

# 🔥 Rebase vs Merge (Quick Understanding)

| Merge                     | Rebase                 |
| ------------------------- | ---------------------- |
| Creates merge commit      | No merge commit        |
| Preserves history exactly | Rewrites history       |
| Good for shared branches  | Good for local cleanup |

---

# 🔥 Summary Table

| Command               | Main Purpose                       |
| --------------------- | ---------------------------------- |
| git rebase            | Replay commits on another branch   |
| git rebase -i         | Interactive history editing        |
| git rebase --continue | Continue after conflict resolution |
| git rebase --abort    | Cancel rebase process              |

---

✅ Rebasing is powerful for keeping history clean but must be used carefully in team environments.
