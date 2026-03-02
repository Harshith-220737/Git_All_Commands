# Git Repository Status & Inspection Commands (Beginner Friendly)

---

# 1️⃣ git status

### 🔹 Command

```bash
git status
```

### 🔹 Purpose

Shows the current state of your working directory and staging area.

### 🔹 Simple Explanation

This command tells you:

- Which files are modified
- Which files are staged
- Which files are untracked

### 🔹 Use Case

Always run this before committing to see what is happening in your repository.

---

# 2️⃣ git log

### 🔹 Command

```bash
git log
```

### 🔹 Purpose

Displays full commit history.

### 🔹 Simple Explanation

Shows detailed information about all commits including:

- Commit ID
- Author
- Date
- Commit message

### 🔹 Use Case

Used to review project history.

---

# 3️⃣ git log --oneline

### 🔹 Command

```bash
git log --oneline
```

### 🔹 Purpose

Shows commit history in short format.

### 🔹 Simple Explanation

Displays each commit in a single line (short commit ID + message).

### 🔹 Use Case

Quick overview of commit history.

---

# 4️⃣ git log --graph

### 🔹 Command

```bash
git log --graph
```

### 🔹 Purpose

Shows commit history in a branch graph format.

### 🔹 Simple Explanation

Displays a visual tree structure showing branches and merges.

### 🔹 Use Case

Helpful for understanding branching and merge structure.

---

# 5️⃣ git show

### 🔹 Command

```bash
git show <commit-id>
```

### 🔹 Purpose

Shows detailed information about a specific commit.

### 🔹 Simple Explanation

Displays:

- Commit details
- Changes made in that commit

### 🔹 Example

```bash
git show a1b2c3d
```

### 🔹 Use Case

To inspect exactly what changed in a specific commit.

---

# 6️⃣ git diff

### 🔹 Command

```bash
git diff
```

### 🔹 Purpose

Shows differences between working directory and staging area.

### 🔹 Simple Explanation

Displays changes that are not yet staged.

### 🔹 Use Case

Review modifications before adding them.

---

# 7️⃣ git diff --staged

### 🔹 Command

```bash
git diff --staged
```

### 🔹 Purpose

Shows differences between staging area and last commit.

### 🔹 Simple Explanation

Displays changes that are staged but not yet committed.

### 🔹 Use Case

Review staged changes before committing.

---

# 8️⃣ git blame

### 🔹 Command

```bash
git blame <file-name>
```

### 🔹 Purpose

Shows who modified each line of a file.

### 🔹 Simple Explanation

Displays line-by-line author information with commit ID.

### 🔹 Example

```bash
git blame index.html
```

### 🔹 Use Case

Used in teams to identify who made specific changes.

---

# 9️⃣ git reflog

### 🔹 Command

```bash
git reflog
```

### 🔹 Purpose

Shows history of all HEAD movements.

### 🔹 Simple Explanation

Tracks:

- Branch switches
- Commits
- Resets
- Rebases

Even deleted commits can be found here.

### 🔹 Use Case

Recover lost commits after reset or rebase.

---

# 🔟 git shortlog

### 🔹 Command

```bash
git shortlog
```

### 🔹 Purpose

Summarizes commit history by author.

### 🔹 Simple Explanation

Groups commits by contributor name.

### 🔹 Use Case

Used to see contribution summary in team projects.

---

# 🔥 Summary Table

| Command           | Main Purpose                  |
| ----------------- | ----------------------------- |
| git status        | Check repository state        |
| git log           | Full commit history           |
| git log --oneline | Short commit history          |
| git log --graph   | Visual branch history         |
| git show          | Show specific commit details  |
| git diff          | Show unstaged changes         |
| git diff --staged | Show staged changes           |
| git blame         | Show line-by-line author info |
| git reflog        | Show HEAD movement history    |
| git shortlog      | Show commit summary by author |

---

✅ These commands help you inspect, debug, and understand your repository clearly.
