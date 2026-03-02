# Git Stash Commands

---

# 📦 Introduction to Git Stash

Git stash is used to temporarily save your uncommitted changes without committing them.

It is helpful when:

- You are working on something
- Suddenly need to switch branches
- But your work is not ready to commit

Stash safely stores your changes so you can restore them later.

---

# 1️⃣ git stash

### 🔹 Command

```bash
git stash
```

### 🔹 Purpose

Temporarily saves (stashes) your modified tracked files and reverts working directory to last commit.

### 🔹 Simple Explanation

This command says:

> "Save my current changes somewhere safe and clean my working directory."

### 🔹 Use Case

Used when you need to quickly switch branches without committing unfinished work.

---

# 2️⃣ git stash list

### 🔹 Command

```bash
git stash list
```

### 🔹 Purpose

Displays all saved stashes.

### 🔹 Example Output

```bash
stash@{0}: WIP on main
stash@{1}: WIP on feature-login
```

### 🔹 Use Case

Used to see how many stashes are stored.

---

# 3️⃣ git stash pop

### 🔹 Command

```bash
git stash pop
```

### 🔹 Purpose

Restores the most recent stash and removes it from stash list.

### 🔹 Simple Explanation

This command says:

> "Give me back my last saved changes and delete the stash copy."

### 🔹 Use Case

Used when you want to continue your previous unfinished work.

---

# 4️⃣ git stash apply

### 🔹 Command

```bash
git stash apply
```

### 🔹 Purpose

Restores a stash but keeps it saved in stash list.

### 🔹 Simple Explanation

This command says:

> "Restore my changes, but keep the stash just in case."

### 🔹 Use Case

Used when you may need the same stash again.

---

# 5️⃣ git stash drop

### 🔹 Command

```bash
git stash drop stash@{0}
```

### 🔹 Purpose

Deletes a specific stash entry.

### 🔹 Simple Explanation

Removes one saved stash manually.

### 🔹 Use Case

Used when you no longer need a particular stash.

---

# 6️⃣ git stash clear

### 🔹 Command

```bash
git stash clear
```

### 🔹 Purpose

Deletes all stashes.

### 🔹 Simple Explanation

This command says:

> "Delete every saved stash permanently."

⚠️ This action cannot be undone.

### 🔹 Use Case

Used when you want to clean up all stored stashes.

---

# 🔥 Summary Table

| Command         | Main Purpose                     |
| --------------- | -------------------------------- |
| git stash       | Save current changes temporarily |
| git stash list  | Show all saved stashes           |
| git stash pop   | Restore and remove stash         |
| git stash apply | Restore without removing stash   |
| git stash drop  | Delete specific stash            |
| git stash clear | Delete all stashes               |

---

✅ Git stash helps manage temporary work safely without committing incomplete changes.
