# 4. Git Merge Hands-On Lab

This project demonstrates how to handle and resolve merge conflicts in Git when multiple users modify the same file in different branches. The lab covers creating branches, making conflicting changes, using Git diff and P4Merge to compare changes, resolving conflicts with a 3-way merge, updating `.gitignore`, and maintaining a clean Git history. :contentReference[oaicite:0]{index=0}

---

## 📌 Objectives

- Understand merge conflicts in Git
- Create and work with branches
- Make changes in multiple branches
- Compare branch differences
- Resolve merge conflicts using a 3-way merge
- Update `.gitignore`
- Delete merged branches
- View commit history using Git log

---

## 🛠️ Technologies Used

- Git
- Git Bash
- GitHub / GitLab
- P4Merge



---

# Implementation

## Step 1: Verify Repository Status

Ensure the master branch is in a clean state.

```bash
git status
```

---

## Step 2: Create a New Branch

Create a branch named **GitWork**.

```bash
git branch GitWork
```

Switch to the new branch.

```bash
git checkout GitWork
```

---

## Step 3: Create and Modify a File

Create a new file.

```bash
touch hello.xml
```

Add some content to the file.

Example:

```xml
<message>Hello from GitWork Branch</message>
```

Check repository status.

```bash
git status
```

---

## Step 4: Commit Changes

Stage and commit the file.

```bash
git add hello.xml
git commit -m "Added hello.xml in GitWork branch"
```

---

## Step 5: Switch to Master Branch

```bash
git checkout master
```

---

## Step 6: Modify the Same File

Create or edit **hello.xml** with different content.

Example:

```xml
<message>Hello from Master Branch</message>
```

Commit the changes.

```bash
git add hello.xml
git commit -m "Updated hello.xml in master"
```

---

## Step 7: View Commit History

Display the commit graph.

```bash
git log --oneline --graph --decorate --all
```

---

## Step 8: Compare Changes

Compare differences between the master branch and GitWork.

```bash
git diff master GitWork
```

For a visual comparison using P4Merge:

```bash
git difftool master GitWork
```

---

## Step 9: Merge the Branch

Merge the GitWork branch into master.

```bash
git merge GitWork
```

Since both branches modified the same file, Git reports a merge conflict.

---

## Step 10: Resolve Merge Conflict

Open the conflicting file and resolve the conflict manually or using a 3-way merge tool such as P4Merge.

After resolving the conflict:

```bash
git add hello.xml
git commit -m "Resolved merge conflict"
```

---

## Step 11: Update .gitignore

Add backup files to `.gitignore`.

Example:

```gitignore
*.bak
```

Commit the updated `.gitignore`.

```bash
git add .gitignore
git commit -m "Updated .gitignore"
```

---

## Step 12: List Available Branches

```bash
git branch
```

---

## Step 13: Delete the Merged Branch

```bash
git branch -d GitWork
```

---

## Step 14: View Final Commit History

```bash
git log --oneline --graph --decorate
```

---

# 📖 Git Commands Used

| Command | Description |
|---------|-------------|
| `git status` | Display repository status |
| `git branch` | Create or list branches |
| `git checkout` | Switch branches |
| `git add` | Stage changes |
| `git commit` | Commit staged changes |
| `git diff` | Compare differences between branches |
| `git difftool` | Visual comparison using P4Merge |
| `git merge` | Merge one branch into another |
| `git log --oneline --graph --decorate --all` | Display commit graph |
| `git branch -d` | Delete merged branch |

---

# 📸 Screenshots

<img width="1285" height="823" alt="image" src="https://github.com/user-attachments/assets/907c6b17-d679-4234-832c-c30779316856" />

<img width="1264" height="1132" alt="image" src="https://github.com/user-attachments/assets/6f88e09f-0606-46d6-9a41-5f52ee161606" />

<img width="1305" height="1108" alt="image" src="https://github.com/user-attachments/assets/f2e2f892-bc16-4f72-bee5-047df3df1cca" />

<img width="931" height="1140" alt="image" src="https://github.com/user-attachments/assets/ebb5f6b4-6a03-4e23-94ba-95ad6d6c382d" />

<img width="1216" height="1105" alt="image" src="https://github.com/user-attachments/assets/1ae2cadb-c2af-4fb5-8ead-a039cfa9fbe8" />





---
