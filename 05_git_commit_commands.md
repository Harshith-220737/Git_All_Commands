# Git Commit Commands

---

# 1️⃣ git commit

### 🔹 Command

```bash
git commit
```

### 🔹 Purpose

Creates a new commit using the staged changes.

### 🔹 Simple Explanation

This command tells Git:

> "Save the staged changes as a new version of the project."

After running this command, Git opens a text editor where you must write a commit message.

### 🔹 Use Case

Used when you want to write a detailed commit message in an editor.

---

# 2️⃣ git commit -m

### 🔹 Command

```bash
git commit -m "Your commit message"
```

### 🔹 Purpose

Creates a commit with a message directly from the command line.

### 🔹 Simple Explanation

This is a shortcut version of `git commit` where you provide the message instantly.

### 🔹 Example

```bash
git commit -m "Added login functionality"
```

### 🔹 Use Case

Most commonly used command in daily development because it is fast and simple.

---

# 3️⃣ git commit --amend

### 🔹 Command

```bash
git commit --amend
```

### 🔹 Purpose

Modifies the most recent commit.

### 🔹 Simple Explanation

This command allows you to:

- Change the last commit message
- Add forgotten changes to the last commit

### 🔹 Example Use Case 1: Fix Commit Message

```bash
git commit --amend
```

Git opens the editor to edit the previous message.

### 🔹 Example Use Case 2: Add Forgotten File

```bash
git add forgotten_file.txt
git commit --amend
```

Now the forgotten file becomes part of the last commit.

⚠️ Important: Avoid using this after pushing to a shared repository.

---

# 4️⃣ git commit --no-edit

### 🔹 Command

```bash
git commit --amend --no-edit
```

### 🔹 Purpose

Amends the last commit without changing its commit message.

### 🔹 Simple Explanation

This command says:

> "Update the previous commit, but keep the same message."

### 🔹 Example

```bash
git add small_fix.txt
git commit --amend --no-edit
```

### 🔹 Use Case

Used when you forgot to stage a file but do not want to change the commit message.

---

# 🔥 Summary Table

| Command                      | Main Purpose                                |
| ---------------------------- | ------------------------------------------- |
| git commit                   | Create commit (opens editor)                |
| git commit -m                | Create commit with inline message           |
| git commit --amend           | Modify last commit                          |
| git commit --amend --no-edit | Modify last commit without changing message |

---

✅ These commands control how changes are permanently saved into your Git history.
