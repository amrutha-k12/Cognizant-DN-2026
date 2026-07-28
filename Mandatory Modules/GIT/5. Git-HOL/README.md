# 5. Git Hands-On Lab

This project demonstrates the final steps of a Git workflow by cleaning up the local repository, synchronizing it with a remote repository, and pushing pending changes. The lab covers verifying repository status, listing branches, pulling the latest updates from the remote repository, pushing local commits, and confirming successful synchronization. :contentReference[oaicite:0]{index=0}

---

## 📌 Objectives

- Verify the repository is in a clean state
- List all available branches
- Pull the latest changes from the remote repository
- Push pending commits to the remote repository
- Verify that changes are reflected in the remote repository

---

## 🛠️ Technologies Used

- Git
- Git Bash
- GitHub / GitLab



---


# Implementation

## Step 1: Verify Repository Status

Ensure the working directory is clean.

```bash
git status
```

---

## Step 2: List Available Branches

Display all local branches.

```bash
git branch
```

To display both local and remote branches:

```bash
git branch -a
```

---

## Step 3: Pull Latest Changes

Synchronize the local repository with the remote repository.

```bash
git pull origin master
```

---

## Step 4: Push Pending Changes

Push all committed local changes to the remote repository.

```bash
git push origin master
```

---

## Step 5: Verify Remote Repository

Open the remote GitHub/GitLab repository and verify that the latest commits and files have been successfully uploaded.

You can also verify using:

```bash
git log --oneline
```

or

```bash
git remote -v
```

---

# 📖 Git Commands Used

| Command | Description |
|---------|-------------|
| `git status` | Check the current repository status |
| `git branch` | List local branches |
| `git branch -a` | List local and remote branches |
| `git pull origin master` | Pull the latest changes from the remote repository |
| `git push origin master` | Push local commits to the remote repository |
| `git log --oneline` | Display commit history |
| `git remote -v` | View configured remote repositories |

---

# 📸 Screenshots

<img width="898" height="367" alt="image" src="https://github.com/user-attachments/assets/39cb1b90-ec8a-4ce7-bf79-f0ffb77ae1ce" />

<img width="769" height="772" alt="image" src="https://github.com/user-attachments/assets/695868e0-a536-4cd8-8a94-5d8f6a70d40f" />

---
