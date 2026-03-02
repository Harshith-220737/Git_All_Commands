# Git Branch Management Commands

---

# 🌿 Introduction to Branches

A branch in Git is like a separate line of development.
It allows you to work on new features or fixes without affecting the main project.

Default branch is usually `main` (or sometimes `master`).

---

# 1️⃣ git branch

### 🔹 Command

```bash
git branch
```

### 🔹 Purpose

Lists all local branches in the repository.

### 🔹 Simple Explanation

Shows all branches and highlights the current branch with `*`.

### 🔹 Example Output

```bash
* main
  feature-login
```

### 🔹 Use Case

To check which branch you are currently working on.

---

# 2️⃣ git branch -a

### 🔹 Command

```bash
git branch -a
```

### 🔹 Purpose

Lists all branches (local + remote).

### 🔹 Simple Explanation

Shows:

- Local branches
- Remote branches (like origin/main)

### 🔹 Use Case

Useful when working in team projects to see all available branches.

---

# 3️⃣ git branch -d

### 🔹 Command

```bash
git branch -d <branch-name>
```

### 🔹 Purpose

Deletes a local branch safely.

### 🔹 Simple Explanation

Deletes the branch only if it has been merged.

### 🔹 Example

```bash
git branch -d feature-login
```

### 🔹 Use Case

Used after completing and merging a feature branch.

---

# 4️⃣ git branch -D

### 🔹 Command

```bash
git branch -D <branch-name>
```

### 🔹 Purpose

Force deletes a branch.

### 🔹 Simple Explanation

Deletes the branch even if it has NOT been merged.

⚠️ Use carefully — you may lose unmerged work.

### 🔹 Example

```bash
git branch -D feature-login
```

---

# 5️⃣ git checkout

### 🔹 Command

```bash
git checkout <branch-name>
```

### 🔹 Purpose

Switches to another branch.

### 🔹 Simple Explanation

Moves you from one branch to another.

### 🔹 Example

```bash
git checkout feature-login
```

---

# 6️⃣ git checkout -b

### 🔹 Command

```bash
git checkout -b <new-branch-name>
```

### 🔹 Purpose

Creates a new branch and switches to it immediately.

### 🔹 Simple Explanation

This is a shortcut for:

1. Creating a branch
2. Switching to that branch

### 🔹 Example

```bash
git checkout -b feature-dashboard
```

---

# 7️⃣ git switch

### 🔹 Command

```bash
git switch <branch-name>
```

### 🔹 Purpose

Switches branches (modern alternative to checkout).

### 🔹 Simple Explanation

Same as `git checkout` but only used for branch switching.

### 🔹 Example

```bash
git switch main
```

---

# 8️⃣ git switch -c

### 🔹 Command

```bash
git switch -c <new-branch-name>
```

### 🔹 Purpose

Creates and switches to a new branch (modern method).

### 🔹 Simple Explanation

Modern replacement for:

```bash
git checkout -b
```

### 🔹 Example

```bash
git switch -c feature-payment
```

---

# 🔥 Summary Table

| Command         | Main Purpose                       |
| --------------- | ---------------------------------- |
| git branch      | List local branches                |
| git branch -a   | List all branches (local + remote) |
| git branch -d   | Delete merged branch               |
| git branch -D   | Force delete branch                |
| git checkout    | Switch branch (older method)       |
| git checkout -b | Create & switch branch             |
| git switch      | Switch branch (modern)             |
| git switch -c   | Create & switch branch (modern)    |

---

✅ These commands help you manage parallel development using branches professionally.
