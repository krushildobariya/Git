# 📘 Git – Complete Developer Training

A fully detailed, corporate‑quality Git guide including overview, installation, workflow, configuration, branching, remote operations, troubleshooting, and best practices.

---

## 🧩 1. What is Git?

### **Full Form**

**GIT = Global Information Tracker**

### **Overview**

Git is a **Distributed Version Control System (DVCS)** used to track code changes, collaborate with teams, and maintain project history safely.

### **Why Developers Use Git**

* Tracks every version of code
* Enables team collaboration
* Supports branching for safe feature development
* Fast & reliable
* Any Where you can work

---

## 🧩 2. Git vs GitHub vs GitLab

| Tool       | What It Is                   | Use                                            |
| ---------- | ---------------------------- | ---------------------------------------------- |
| **Git**    | Version Control System       | Tracks and manages code locally                |
| **GitHub** | Cloud Hosting Platform       | Stores Git repos, pull requests, collaboration |
| **GitLab** | Cloud Platform + CI/CD Platform | Code Store, Versioning + DevOps pipelines                  |

---

## 🧩 3. Uses of Git

* Manage source code
* Track contributor changes
* Roll back to previous versions
* Develop features separately
* Fix bugs without affecting production
* Integrate into CI/CD pipelines

---

## 🧩 4. Install Git

### **Windows**

Download: [https://git-scm.com/downloads](https://git-scm.com/downloads)

### **MacOS**

```bash
brew install git
```

### **Ubuntu / Linux**

```bash
sudo apt update
sudo apt install git -y
```

### **Check version**

```bash
git --version
```

---

## 🧩 5. Git Workflow

```
Working Directory → Staging Area → Local Repository → Remote Repository
```

### **Explanation**

* **Working Directory:** Where you edit files
* **Staging Area:** Files prepared to commit (`git add`)
* **Local Repository:** Commits saved locally
* **Remote Repository:** Cloud storage (GitHub/GitLab)

---

## 🧩 6. Configure Git (Required Before First Commit)

### **Set username**

```bash
git config --global user.name "Your Name"
```

### **Set email**

```bash
git config --global user.email "you@example.com"
```

### **Verify settings**

```bash
git config --list
```

---

## 🧩 7. Initialize a Repository

### Start a new project

```bash
git init
```

### Clone an existing project

```bash
git clone <repository_url>
```

---

## 🧩 8. Connecting to a Remote Repository

### Add remote origin

```bash
git remote add origin <repo_url>
```

### Push first time

```bash
git push -u origin main
```

### Check remotes

```bash
git remote -v
```

---

## 🧩 9. Checking Repository Status

### Check current changes

```bash
git status
```

Shows:

* Untracked files
* Modified files
* Staged files
* Active branch

---

## 🧩 10. Viewing Commit History

### Full history

```bash
git log
```

### Short history

```bash
git log --oneline
```

### View specific commit

```bash
git show <commit_id>
```

---

## 🧩 11. Branches (Feature, Develop, Staging, Master)

### 🌿 **GitFlow Branching Model**

| Branch          | Purpose                 |
| --------------- | ----------------------- |
| **main/master** | Production-ready code   |
| **Staging**     | Pre-production testing  |
| **Develop**     | Integration branch      |
| **Feature**    | New feature development |

### Branch Commands

**Create**

```bash
git branch feature-login
```

**Switch**

```bash
git checkout feature-login
```

**Create + switch**

```bash
git checkout -b feature-login
```

**List branches**

```bash
git branch
```

**Delete branch**

```bash
git branch -d feature-login
```

---

## 🧩 12. Ignoring Files with .gitignore

The `.gitignore` file prevents unnecessary files from being tracked.

### Common entries

```
node_modules/
.env
*.log
.DS_Store
.vscode/
.idea/
vendor/
```

---

## 🧩 13. Essential Commands: add, commit, push, pull

### Add all files

```bash
git add .
```

### Add specific file

```bash
git add filename
```

### Commit

```bash
git commit -m "Your commit message"
```

### Push to remote

```bash
git push origin main
```

### Pull updates

```bash
git pull origin main
```

---

## 🧩 14. Merge Conflict – How to Fix

Conflicts occur when two people edit the same line of code.

### Example conflict

```
<<<<<<< HEAD
Your changes
=======
Incoming changes
>>>>>>> origin/main
```

### Steps to fix:

1. Open the file
2. Remove conflict markers
3. Keep the correct code
4. Stage the file:

   ```bash
   git add .
   ```
5. Commit the fix:

   ```bash
   git commit -m "Resolved merge conflict"
   ```

---

## 🧩 15. Git Workflow Summary

### **Daily Developer Cycle**

```
git pull
# make code changes
git add .
git commit -m "message"
git push
```

---

## 🧩 16. Best Practices for Developers

* Commit frequently with meaningful messages
* Never commit secrets (.env, API keys)
* Use branches for every feature
* Pull before starting new work
* Review code using pull requests
* Resolve conflicts carefully
* Keep main branch clean & deployment-friendly

---

## 🧩 17. Troubleshooting

### Git not recognized

```
'git' is not recognized
```

Install Git & reboot terminal.

### Permission denied (SSH)

Check SSH key:

```bash
ssh-keygen -t ed25519
```

Add key to GitHub/GitLab.
