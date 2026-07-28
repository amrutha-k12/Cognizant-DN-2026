# 1. Git Hands-On Lab

A beginner-friendly hands-on lab demonstrating the fundamental Git workflow, including repository initialization, Git configuration, file tracking, commits, and remote repository operations. This lab provides practical experience with essential Git commands used in software development. :contentReference[oaicite:0]{index=0}

---

## 📌 Objectives

- Configure Git on a local machine
- Set up Git user information
- Configure Notepad++ as the default Git editor
- Create and initialize a Git repository
- Add files to version control
- Commit changes
- Connect with a remote repository
- Push and pull changes using Git

---

## 🛠️ Technologies Used

- Git
- Git Bash
- GitHub / GitLab
- Notepad++

---

## 📂 Project Structure

```
GitDemo/
│── .git/
│── welcome.txt
└── README.md
```

---

## 🚀 Lab Workflow

### Step 1: Configure Git

Configure your username and email.

```bash
git config --global user.name "Amrutha"
git config --global user.email "amruthakoyyalamudi@gmail.com"
```

Verify configuration:

```bash
git config --global --list
```

---

### Step 2: Configure Default Editor

Set Notepad++ as the default editor.

```bash
git config --global core.editor "notepad++.exe -multiInst -nosession"
```

Verify:

```bash
git config --global -e
```


---

### Step 3: Initialize Repository

Create a new Git repository.

```bash
git init GitDemo
```

Check repository contents.

```bash
ls -al
```


---

### Step 4: Create a File

Create a sample file.

```bash
echo "Welcome to the version control" >> welcome.txt
```

Verify the file.

```bash
cat welcome.txt
```

---

### Step 5: Check Repository Status

```bash
git status
```

---

### Step 6: Stage Files

```bash
git add welcome.txt
```


---

### Step 7: Commit Changes

```bash
git commit
```

Or

```bash
git commit -m "Initial commit"
```

---

### Step 8: Push to Remote Repository

```bash
git remote add origin <repository-url>
git push origin master
```

---

### Step 9: Pull Latest Changes

```bash
git pull origin master
```

---

## 📖 Git Commands Used

| Command | Description |
|----------|-------------|
| `git init` | Initialize a Git repository |
| `git config` | Configure Git settings |
| `git status` | Show repository status |
| `git add` | Stage files |
| `git commit` | Commit changes |
| `git pull` | Fetch and merge changes |
| `git push` | Push commits to remote |
| `git config --global -e` | Open Git configuration |

---

## 📸 Screenshots

<img width="1366" height="439" alt="image" src="https://github.com/user-attachments/assets/537ae90a-329a-49c4-bd76-ed9a72ff4f96" />

<img width="1596" height="1090" alt="image" src="https://github.com/user-attachments/assets/43e3df2d-0ff6-43b4-9df4-bcf48687cea8" />

<img width="1423" height="1026" alt="image" src="https://github.com/user-attachments/assets/75b6bf7c-dda7-45d7-a7c9-1b5a9a9be637" />

<img width="1204" height="1081" alt="image" src="https://github.com/user-attachments/assets/4aef3057-1ad5-4b7a-aefd-1c00949b0563" />

<img width="760" height="298" alt="image" src="https://github.com/user-attachments/assets/e00742bc-c550-4def-8002-9d76f19087a2" />

---
