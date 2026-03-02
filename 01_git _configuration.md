# Git Configuration Commands (Beginner Friendly)

---

## 1️⃣ git --version

### 🔹 Command

```bash
git --version
```

### 🔹 Purpose

Checks whether Git is installed and shows the installed version.

### 🔹 Simple Explanation

This command asks Git:

> "Which version are you?"

If Git is installed correctly, it will display the version number.

### 🔹 Example Output

```bash
git version 2.43.0
```

### 🔹 Use Case

- Verify Git installation
- Confirm correct version
- First command to run after installing Git

---

## 2️⃣ git config --global user.name "Bandari"

### 🔹 Command

```bash
git config --global user.name "Bandari"
```

### 🔹 Purpose

Sets your name as the author for all commits on your system.

### 🔹 Simple Explanation

Whenever you make a commit, Git will attach this name to it.

### 🔹 Why `--global`?

`--global` means this setting applies to all repositories on your computer.

### 🔹 Use Case

When you run:

```bash
git commit -m "Initial commit"
```

Git stores:

```
Author: Bandari
```

This helps identify who made the changes.

---

## 3️⃣ git config --global user.email "[your_email@example.com](mailto:your_email@example.com)"

### 🔹 Command

```bash
git config --global user.email "your_email@example.com"
```

### 🔹 Purpose

Sets your email address for all commits.

### 🔹 Simple Explanation

Git attaches this email to every commit you make.

### 🔹 Important

Make sure this email matches your GitHub account email. If it matches, your commits will be linked to your GitHub profile.

### 🔹 Use Case

- Identify commit owner
- Connect commits to GitHub profile
- Professional project tracking

---

## 4️⃣ git config --list

### 🔹 Command

```bash
git config --list
```

### 🔹 Purpose

Displays all Git configuration settings currently applied.

### 🔹 Simple Explanation

This command shows everything Git knows about your configuration (name, email, editor, etc.).

### 🔹 Example Output

```bash
user.name=Bandari
user.email=your_email@example.com
core.editor=vim
```

### 🔹 Use Case

- Verify configuration
- Debug incorrect settings
- Confirm name and email are properly set

---

# 🔥 Configuration Levels in Git

| Level  | Flag Used | Scope                   |
| ------ | --------- | ----------------------- |
| System | --system  | Entire computer         |
| Global | --global  | Current user            |
| Local  | (no flag) | Current repository only |

---

✅ These are the basic Git configuration commands every developer should set before starting any project.
