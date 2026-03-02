# Git Tagging Commands

---

# 🏷 Introduction to Tags

Tags in Git are used to mark important points in history.

Commonly used for:

- Release versions (v1.0, v2.0)
- Stable builds
- Production deployments

Unlike branches, tags do not change. They permanently point to a specific commit.

---

# 1️⃣ git tag

### 🔹 Command

```bash
git tag
```

### 🔹 Purpose

Lists all tags in the repository.

### 🔹 Simple Explanation

Shows version markers that exist in the project.

### 🔹 Example Output

```bash
v1.0
v1.1
v2.0
```

### 🔹 Use Case

Used to check available versions of the project.

---

# 2️⃣ git tag -a

### 🔹 Command

```bash
git tag -a <tag-name> -m "Tag message"
```

### 🔹 Purpose

Creates an annotated tag.

### 🔹 Simple Explanation

Annotated tags store:

- Tag name
- Author
- Date
- Message

### 🔹 Example

```bash
git tag -a v1.0 -m "First stable release"
```

### 🔹 Use Case

Used for official project releases.

---

# 3️⃣ git tag -d

### 🔹 Command

```bash
git tag -d <tag-name>
```

### 🔹 Purpose

Deletes a local tag.

### 🔹 Example

```bash
git tag -d v1.0
```

### 🔹 Use Case

Used when a tag was created by mistake.

---

# 4️⃣ git push origin --tags

### 🔹 Command

```bash
git push origin --tags
```

### 🔹 Purpose

Pushes all local tags to the remote repository.

### 🔹 Simple Explanation

By default, `git push` does NOT push tags.
This command uploads all tags to GitHub.

### 🔹 Use Case

Used after creating release versions locally.

---

# 🔥 Important Note

If you want to push a specific tag only:

```bash
git push origin v1.0
```

---

# 🔥 Summary Table

| Command                | Main Purpose            |
| ---------------------- | ----------------------- |
| git tag                | List tags               |
| git tag -a             | Create annotated tag    |
| git tag -d             | Delete local tag        |
| git push origin --tags | Push all tags to remote |

---

✅ Tags are mainly used for versioning and release management in professional projects.
