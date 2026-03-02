# Git File Tracking Commands

---

# 1️⃣ git add

### 🔹 Command

```bash
git add <file-name>
```

### 🔹 Purpose

Adds a specific file to the staging area.

### 🔹 Simple Explanation

This command tells Git:

> "I am ready to include this file in the next commit."

### 🔹 Example

```bash
git add index.html
```

### 🔹 Use Case

Used when you want to stage only selected files instead of everything.

---

# 2️⃣ git add .

### 🔹 Command

```bash
git add .
```

### 🔹 Purpose

Adds all modified and new files in the current directory to the staging area.

### 🔹 Simple Explanation

This command tells Git:

> "Stage everything that has changed."

### 🔹 Use Case

Useful when you want to commit all changes at once.

⚠️ Be careful: It stages everything, even unintended changes.

---

# 3️⃣ git add -p

### 🔹 Command

```bash
git add -p
```

### 🔹 Purpose

Allows you to stage changes interactively (in parts).

### 🔹 Simple Explanation

Instead of adding the whole file, Git shows changes piece by piece and asks:

> "Do you want to stage this part? (y/n)"

### 🔹 Use Case

Used in professional projects to create clean and meaningful commits.

---

# 4️⃣ git restore

### 🔹 Command

```bash
git restore <file-name>
```

### 🔹 Purpose

Discards changes in the working directory.

### 🔹 Simple Explanation

This command tells Git:

> "Remove my changes and bring the file back to the last committed version."

### 🔹 Example

```bash
git restore index.html
```

### 🔹 Use Case

Used when you accidentally modify a file and want to undo it.

---

# 5️⃣ git restore --staged

### 🔹 Command

```bash
git restore --staged <file-name>
```

### 🔹 Purpose

Removes a file from the staging area but keeps the changes in the working directory.

### 🔹 Simple Explanation

This command says:

> "Unstage this file, but don’t delete my changes."

### 🔹 Example

```bash
git restore --staged index.html
```

### 🔹 Use Case

Used when you staged a file by mistake.

---

# 6️⃣ git rm

### 🔹 Command

```bash
git rm <file-name>
```

### 🔹 Purpose

Removes a file from both the working directory and Git tracking.

### 🔹 Simple Explanation

This command:

- Deletes the file
- Stages the deletion

### 🔹 Example

```bash
git rm old_file.txt
```

### 🔹 Use Case

Used when you want to permanently delete a file from the repository.

---

# 7️⃣ git mv

### 🔹 Command

```bash
git mv <old-name> <new-name>
```

### 🔹 Purpose

Renames or moves a file and stages the change.

### 🔹 Simple Explanation

This command tells Git:

> "Rename this file and track the change properly."

### 🔹 Example

```bash
git mv index.html home.html
```

### 🔹 Use Case

Used when renaming files so Git tracks history correctly.

---

# 🔥 Summary Table

| Command              | Main Purpose                      |
| -------------------- | --------------------------------- |
| git add              | Stage specific file               |
| git add .            | Stage all changes                 |
| git add -p           | Stage changes interactively       |
| git restore          | Discard file changes              |
| git restore --staged | Unstage file                      |
| git rm               | Remove file and stage deletion    |
| git mv               | Rename/move file and stage change |

---

✅ These commands control how files move between Working Directory → Staging Area → Commit in Git.
