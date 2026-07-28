# 3. Git Hands-On Lab

This project demonstrates the fundamental Git branching and merging workflow. It covers creating branches, switching between branches, committing changes, comparing differences, merging branches into the main branch, and deleting branches after successful integration. :contentReference[oaicite:0]{index=0}

---

## 📌 Objectives

- Understand Git branching and merging
- Create and manage Git branches
- Switch between branches
- Commit changes in a branch
- Compare differences between branches
- Merge branches into the master branch
- Delete merged branches
- Understand merge requests in GitLab

---

## 🛠️ Technologies Used

- Git
- Git Bash
- GitHub / GitLab
- P4Merge

---




## Step 1: Create a New Branch

```bash
git branch GitNewBranch
```



---

## Step 2: List All Branches

```bash
git branch -a
```

The `*` symbol indicates the currently active branch.


---

## Step 3: Switch to the New Branch

```bash
git checkout GitNewBranch
```



---

## Step 4: Create or Modify Files

Example:

```bash
echo "This is a new feature." >> sample.txt
```

Stage the file:

```bash
git add sample.txt
```

Commit the changes:

```bash
git commit -m "Added sample file in GitNewBranch"
```



---

## Step 5: Verify Repository Status

```bash
git status
```


---

# Merging

## Step 6: Switch Back to Master

```bash
git checkout master
```



---

## Step 7: Compare Branch Differences

View command-line differences.

```bash
git diff master GitNewBranch
```



---

## Step 8: Compare Using P4Merge

```bash
git difftool master GitNewBranch
```



---

## Step 9: Merge the Branch

```bash
git merge GitNewBranch
```



---

## Step 10: View Commit History

```bash
git log --oneline --graph --decorate
```



---

## Step 11: Delete the Branch

```bash
git branch -d GitNewBranch
```

Verify:

```bash
git branch
```


---

## 📖 Git Commands Used

| Command | Description |
|---------|-------------|
| `git branch` | Create or list branches |
| `git checkout` | Switch branches |
| `git add` | Stage changes |
| `git commit` | Commit staged changes |
| `git status` | Display repository status |
| `git diff` | Compare branch differences |
| `git difftool` | Compare branches using P4Merge |
| `git merge` | Merge one branch into another |
| `git log --oneline --graph --decorate` | View commit history graphically |
| `git branch -d` | Delete a merged branch |

---

## 📸 Screenshots

<img width="1204" height="489" alt="image" src="https://github.com/user-attachments/assets/70e9603d-9374-49a3-bea9-4dece1f21b70" />

<img width="1120" height="1129" alt="image" src="https://github.com/user-attachments/assets/6348da22-18f5-465a-a1ee-52b6b0072282" />

<img width="1170" height="1134" alt="image" src="https://github.com/user-attachments/assets/568d0a60-ef7d-4716-85ed-b4aa42b4e9ca" />

<img width="612" height="109" alt="image" src="https://github.com/user-attachments/assets/370b20b1-fe72-485d-b195-30c30619b603" />

---
