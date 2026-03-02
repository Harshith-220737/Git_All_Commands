# Git Submodule Commands

---

# 📦 Introduction to Git Submodules

A submodule allows you to include one Git repository inside another Git repository.

It is commonly used when:

- You want to reuse another project inside your project
- You want to keep external libraries as separate repositories

Example:
Your main project → includes another project as a submodule.

---

# 1️⃣ git submodule add

### 🔹 Command

```bash
git submodule add <repository-url>
```

### 🔹 Purpose

Adds another Git repository as a submodule inside your current repository.

### 🔹 Simple Explanation

This command says:

> "Include this external repository inside my project."

### 🔹 Example

```bash
git submodule add https://github.com/user/library.git
```

### 🔹 What Happens?

- Creates a folder for that repository
- Adds a `.gitmodules` file
- Tracks the specific commit of that external repository

### 🔹 Use Case

Used when your project depends on another Git-based project.

---

# 2️⃣ git submodule init

### 🔹 Command

```bash
git submodule init
```

### 🔹 Purpose

Initializes submodule configuration after cloning a repository.

### 🔹 Simple Explanation

When someone clones your project, submodules are not automatically downloaded.
This command prepares them for setup.

### 🔹 Use Case

Used after cloning a repository that contains submodules.

---

# 3️⃣ git submodule update

### 🔹 Command

```bash
git submodule update
```

### 🔹 Purpose

Downloads and checks out the correct version of submodules.

### 🔹 Simple Explanation

This command says:

> "Download and match the exact version of submodules used in this project."

### 🔹 Common Combined Usage

```bash
git submodule init
git submodule update
```

Or directly:

```bash
git submodule update --init --recursive
```

### 🔹 Use Case

Used after cloning a repository with submodules to fully set up the project.

---

# 🔥 Summary Table

| Command              | Main Purpose                         |
| -------------------- | ------------------------------------ |
| git submodule add    | Add external repository as submodule |
| git submodule init   | Initialize submodule configuration   |
| git submodule update | Download and sync submodule content  |

---

✅ Submodules are useful for managing external dependencies while keeping repositories independent.
