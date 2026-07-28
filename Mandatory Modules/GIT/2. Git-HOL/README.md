# 2. Git Hands-On Lab

A hands-on Git project demonstrating the essential concepts of version control, including Git configuration, repository initialization, file tracking, commits, remote repository management, and `.gitignore`. This lab provides practical experience with commonly used Git commands for managing source code efficiently. :contentReference[oaicite:0]{index=0} :contentReference[oaicite:1]{index=1}

---

## 📌 Objectives

- Configure Git on a local machine
- Set up Git username and email
- Configure Notepad++ as the default Git editor
- Initialize a Git repository
- Create and manage project files
- Stage and commit changes
- Connect to a remote repository
- Push and pull changes
- Ignore unwanted files and folders using `.gitignore`

---

## 🛠️ Technologies Used

- Git
- Git Bash
- GitHub / GitLab
- Notepad++

---

## 🚀 Getting Started

### Clone the Repository

```bash
git clone [https://github.com/your-username/GitDemo.git](https://github.com/amrutha-k12/GitDemo.git)
```

Navigate into the project directory:

```bash
cd GitDemo
```

---

# Implementation

## Step 1: Configure Git

Configure your Git username and email.

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Verify the configuration.

```bash
git config --global --list
```


---

## Step 2: Configure Notepad++ as Default Editor

Set Notepad++ as the default editor.

```bash
git config --global core.editor "notepad++.exe -multiInst -nosession"
```

Verify the editor configuration.

```bash
git config --global -e
```


---

## Step 3: Initialize Git Repository

Create a new Git repository.

```bash
git init GitDemo
```

Check repository contents.

```bash
ls -al
```


---

## Step 4: Create a File

Create a sample file.

```bash
echo "Welcome to the version control" >> welcome.txt
```

Display file contents.

```bash
cat welcome.txt
```


---

## Step 5: Check Repository Status

Check the current repository status.

```bash
git status
```


---

## Step 6: Stage Files

Stage the file.

```bash
git add welcome.txt
```

Verify the status.

```bash
git status
```

---

## Step 7: Commit Changes

Commit the staged changes.

```bash
git commit -m "Initial Commit"
```

Verify the commit.

```bash
git log
```


---

## Step 8: Connect Remote Repository

Add the remote repository.

```bash
git remote add origin https://github.com/your-username/GitDemo.git
```

Verify remote.

```bash
git remote -v
```


---

## Step 9: Push Changes

Push local commits to GitHub.

```bash
git push -u origin master
```


---

## Step 10: Pull Latest Changes

Retrieve updates from the remote repository.

```bash
git pull origin master
```


---

# Git Ignore

Create a `.gitignore` file.

```gitignore
*.log
log/
```

This configuration ignores:

- All `.log` files
- Any folder named `log`

Verify ignored files.

```bash
git status
```


---

# Git Commands Used

| Command | Description |
|---------|-------------|
| `git init` | Initialize a new Git repository |
| `git config` | Configure Git settings |
| `git status` | Display repository status |
| `git add` | Stage files for commit |
| `git commit` | Commit staged changes |
| `git log` | View commit history |
| `git remote` | Manage remote repositories |
| `git push` | Push commits to remote repository |
| `git pull` | Fetch and merge changes |
| `.gitignore` | Ignore unwanted files and folders |

---

# Screenshots

<img width="1164" height="576" alt="image" src="https://github.com/user-attachments/assets/07df91f3-5dc9-46b1-8481-c7a4d8911a0a" />

<img width="967" height="504" alt="image" src="https://github.com/user-attachments/assets/d437a410-99a6-4b47-9efa-1bb5dc01e7fb" />

<img width="949" height="565" alt="image" src="https://github.com/user-attachments/assets/cb305d3b-34fc-4dcd-a7e6-05f2c4cc2b05" />


---
