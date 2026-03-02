# Git Reset & Undo Commands

---

# 🔄 Introduction to Reset & Undo

Git provides multiple ways to undo changes.
Some commands modify commit history, while others safely create new commits.

⚠️ Important:

- `reset` rewrites history
- `revert` preserves history

Understanding the difference is critical in professional projects.

---

# 1️⃣ git reset

### 🔹 Command

```bash
git reset <commit-id>
```

### 🔹 Purpose

Moves the current branch pointer (HEAD) to a previous commit.

### 🔹 Simple Explanation

This command says:

> "Go back to this previous version."

By default, it performs a `--mixed` reset.

---

# 2️⃣ git reset --soft

### 🔹 Command

```bash
git reset --soft <commit-id>
```

### 🔹 Purpose

Moves HEAD to previous commit but keeps changes staged.

### 🔹 What Happens?

- Commit history moves back
- Changes remain in staging area

### 🔹 Use Case

Used when you want to modify recent commits but keep changes ready to recommit.

---

# 3️⃣ git reset --mixed

### 🔹 Command

```bash
git reset --mixed <commit-id>
```

### 🔹 Purpose

Moves HEAD and unstages changes but keeps them in working directory.

### 🔹 What Happens?

- Commit removed
- Files become unstaged
- Changes are not deleted

### 🔹 Use Case

Used when you want to uncommit but keep your work.

---

# 4️⃣ git reset --hard

### 🔹 Command

```bash
git reset --hard <commit-id>
```

### 🔹 Purpose

Moves HEAD and completely deletes all changes after that commit.

### 🔹 What Happens?

- Commit removed
- Staged changes deleted
- Working directory changes deleted

⚠️ Dangerous: This permanently deletes work.

### 🔹 Use Case

Used only when you are sure you want to completely discard changes.

---

# 🔥 Reset Comparison Table

| Command | Commit History | Staging Area | Working Directory |
| ------- | -------------- | ------------ | ----------------- |
| --soft  | Moves          | Keeps        | Keeps             |
| --mixed | Moves          | Clears       | Keeps             |
| --hard  | Moves          | Clears       | Deletes           |

---

# 5️⃣ git revert

### 🔹 Command

```bash
git revert <commit-id>
```

### 🔹 Purpose

Creates a new commit that undoes a previous commit.

### 🔹 Simple Explanation

Instead of deleting history, it adds a new commit that reverses changes.

### 🔹 Use Case

Used in shared repositories where history must not be rewritten.

✅ Safe for team projects.

---

# 6️⃣ git clean -f

### 🔹 Command

```bash
git clean -f
```

### 🔹 Purpose

Deletes untracked files from working directory.

### 🔹 Simple Explanation

Removes files that are not being tracked by Git.

⚠️ Only deletes untracked files.

---

# 7️⃣ git clean -fd

### 🔹 Command

```bash
git clean -fd
```

### 🔹 Purpose

Deletes untracked files and untracked directories.

### 🔹 What Happens?

- `-f` → force delete
- `-d` → delete directories

⚠️ Dangerous if not used carefully.

---

# 🔥 Summary Table

| Command           | Main Purpose                       |
| ----------------- | ---------------------------------- |
| git reset         | Move HEAD to previous commit       |
| git reset --soft  | Undo commit, keep staged changes   |
| git reset --mixed | Undo commit, keep unstaged changes |
| git reset --hard  | Completely discard changes         |
| git revert        | Safely undo using new commit       |
| git clean -f      | Delete untracked files             |
| git clean -fd     | Delete untracked files & folders   |

---

✅ These commands give you powerful control over undoing mistakes in Git.
Use carefully in team environments.
