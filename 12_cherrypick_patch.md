# Git Cherry-Pick & Patch Commands

---

# 🍒 Introduction to Cherry-Pick & Patch

These commands allow you to:

- Apply specific commits from one branch to another
- Share changes without merging entire branches
- Transfer commits using patch files

They are commonly used in large or distributed projects.

---

# 1️⃣ git cherry-pick

### 🔹 Command

```bash
git cherry-pick <commit-id>
```

### 🔹 Purpose

Applies a specific commit from another branch into your current branch.

### 🔹 Simple Explanation

This command says:

> "Take this one commit and apply it here."

### 🔹 Example

```bash
git switch main
git cherry-pick a1b2c3d
```

### 🔹 What Happens?

- Git copies that commit
- Applies it as a new commit in current branch

### 🔹 Use Case

Used when:

- You need only one bug fix from another branch
- You don’t want to merge the whole branch

---

# 2️⃣ git format-patch

### 🔹 Command

```bash
git format-patch <commit-id>
```

### 🔹 Purpose

Creates a patch file from commits.

### 🔹 Simple Explanation

This command converts commits into `.patch` files that can be shared.

### 🔹 Example

```bash
git format-patch HEAD~1
```

### 🔹 What Happens?

- Generates a file like:

```
0001-Added-login-feature.patch
```

### 🔹 Use Case

Used in open-source or email-based contribution workflows.

---

# 3️⃣ git apply

### 🔹 Command

```bash
git apply <patch-file>
```

### 🔹 Purpose

Applies changes from a patch file to working directory.

### 🔹 Simple Explanation

This command says:

> "Apply the changes written inside this patch file."

### 🔹 Example

```bash
git apply 0001-Added-login-feature.patch
```

### 🔹 Important

- Does NOT create a commit automatically
- You must stage and commit manually

### 🔹 Use Case

Used when applying changes from external contributors.

---

# 4️⃣ git am

### 🔹 Command

```bash
git am <patch-file>
```

### 🔹 Purpose

Applies a patch file and creates a commit automatically.

### 🔹 Simple Explanation

This command says:

> "Apply this patch and commit it with original author details."

### 🔹 Example

```bash
git am 0001-Added-login-feature.patch
```

### 🔹 Difference from git apply

| git apply                | git am                    |
| ------------------------ | ------------------------- |
| Applies changes only     | Applies and commits       |
| No author info preserved | Preserves commit metadata |

### 🔹 Use Case

Used in professional open-source contribution workflows.

---

# 🔥 Summary Table

| Command          | Main Purpose                   |
| ---------------- | ------------------------------ |
| git cherry-pick  | Apply specific commit          |
| git format-patch | Create patch file from commit  |
| git apply        | Apply patch without committing |
| git am           | Apply patch and commit         |

---

✅ These commands allow selective commit transfer and patch-based collaboration.
