# Git Repository Setup Commands

---

# 1️⃣ git init

### 🔹 Command

```bash
git init
```

### 🔹 Purpose

Initializes a new Git repository in your current project folder.

### 🔹 Simple Explanation

This command tells Git:

> "Start tracking this folder as a Git project."

It creates a hidden folder called `.git` which stores all version control information.

### 🔹 What Happens Internally?

- Creates `.git` directory
- Starts tracking changes
- Makes your folder a Git repository

### 🔹 Use Case

When starting a brand-new project:

```bash
mkdir my-project
cd my-project
git init
```

Now Git can track files inside `my-project`.

---

# 2️⃣ git clone

### 🔹 Command

```bash
git clone <repository-url>
```

### 🔹 Purpose

Downloads an existing repository from GitHub (or any remote server) to your local system.

### 🔹 Simple Explanation

This command says:

> "Copy this remote repository to my computer."

### 🔹 Example

```bash
git clone https://github.com/user/project.git
```

### 🔹 What Happens Internally?

- Creates a new folder
- Downloads all files
- Downloads full commit history
- Automatically connects to remote (`origin`)

### 🔹 Use Case

- Working on open-source projects
- Downloading team project
- Continuing work from another system

---

# 3️⃣ git clone --branch

### 🔹 Command

```bash
git clone --branch <branch-name> <repository-url>
```

### 🔹 Purpose

Clones a specific branch instead of the default branch.

### 🔹 Simple Explanation

Instead of downloading the default branch (usually `main`), this command downloads a specific branch.

### 🔹 Example

```bash
git clone --branch feature-login https://github.com/user/project.git
```

### 🔹 What Happens?

- Downloads repository
- Automatically checks out the specified branch

### 🔹 Use Case

- Working on a feature branch
- Testing a specific version
- Avoiding unnecessary branches

---

# 4️⃣ git clone --depth

### 🔹 Command

```bash
git clone --depth <number> <repository-url>
```

### 🔹 Purpose

Performs a shallow clone with limited commit history.

### 🔹 Simple Explanation

This command downloads only the latest commits instead of the full history.

### 🔹 Example

```bash
git clone --depth 1 https://github.com/user/project.git
```

### 🔹 What Happens?

- Downloads only the most recent commit
- Faster download
- Saves storage space

### 🔹 Use Case

- Large repositories
- CI/CD pipelines
- When full history is not needed

---

# 🔥 Comparison Summary

| Command            | Main Purpose                     |
| ------------------ | -------------------------------- |
| git init           | Start a new local repository     |
| git clone          | Copy full repository from remote |
| git clone --branch | Clone specific branch            |
| git clone --depth  | Clone with limited history       |

---

✅ These commands are used to start working with repositories either locally or from remote servers.
