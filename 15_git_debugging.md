# Git Debugging Commands

---

# 🐞 Introduction to Git Bisect

`git bisect` is used to find the exact commit that introduced a bug.

It works using a binary search algorithm.
Instead of checking every commit manually, Git automatically narrows down the problem.

This is very powerful in large projects.

---

# 🎯 How git bisect Works (Simple Idea)

1. You tell Git where the bug exists (bad commit).
2. You tell Git where the bug did not exist (good commit).
3. Git automatically checks commits in the middle.
4. You mark each tested commit as good or bad.
5. Git finds the exact commit that caused the issue.

---

# 1️⃣ git bisect start

### 🔹 Command

```bash
git bisect start
```

### 🔹 Purpose

Starts the bisect debugging session.

### 🔹 Simple Explanation

This command tells Git:

> "I want to start searching for a broken commit."

---

# 2️⃣ git bisect bad

### 🔹 Command

```bash
git bisect bad
```

### 🔹 Purpose

Marks the current commit as bad (bug exists here).

### 🔹 Simple Explanation

You run this after confirming that the current version contains the bug.

---

# 3️⃣ git bisect good

### 🔹 Command

```bash
git bisect good <commit-id>
```

### 🔹 Purpose

Marks a specific commit as good (no bug present).

### 🔹 Simple Explanation

This tells Git:

> "At this commit, everything was working correctly."

---

# 4️⃣ git bisect

### 🔹 Command

```bash
git bisect
```

### 🔹 Purpose

Main command that manages the bisect process.

Usually used together with:

```bash
git bisect start
git bisect bad
git bisect good <commit-id>
```

After this, Git automatically checks out a commit in the middle.
You test it and mark it good or bad again.

This continues until Git prints:

```
<commit-id> is the first bad commit
```

---

# 🔄 Ending Bisect Session

After finding the problematic commit:

```bash
git bisect reset
```

This returns you to your original branch.

---

# 🔥 Example Full Workflow

```bash
git bisect start
git bisect bad
git bisect good v1.0
```

Then repeatedly test and mark:

```bash
git bisect good
# or
git bisect bad
```

Until Git identifies the broken commit.

---

# 🔥 Summary Table

| Command          | Main Purpose                         |
| ---------------- | ------------------------------------ |
| git bisect start | Start bug search session             |
| git bisect bad   | Mark current commit as buggy         |
| git bisect good  | Mark commit as working               |
| git bisect       | Binary search for problematic commit |

---

✅ `git bisect` is a professional debugging tool used to quickly identify when a bug was introduced in project history.
