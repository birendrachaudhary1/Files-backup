---
title: "Important git commands everyone needs to know.🎯"
datePublished: Wed Dec 25 2024 04:15:29 GMT+0000 (Coordinated Universal Time)
cuid: cm53dtgau000009mneb7ldxf5
slug: important-git-commands-everyone-needs-to-know
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1735019195402/a1b074e2-c747-4d0a-9f73-977afff4dba9.jpeg
tags: linux, github, git, gitcommands, branch, linuxsystemadministration

---

### 1\. **Basic Git Commands:**

* **Clone a repository:**  
    `git clone <GitHub-link>`
    
* **Add a file to staging:**  
    `git add <file-name>`
    
* **Add all changes to staging:**  
    `git add .`
    
* **Commit changes with a message:**  
    `git commit -m "<message>"`
    
* **Push changes to the main branch:**  
    `git push origin main`
    

---

### 2\. **Initialize a Repository:**

* **Create a new repo locally:**  
    `git init`
    
* **Connect to a remote repository:**  
    `git remote add origin <link>`
    
* **Verify the remote connection:**  
    `git remote -v`
    
* **Check current branch:**  
    `git branch`
    
* **Rename branch to "main":**  
    `git branch -M main`
    
* **Push changes to "main":**  
    `git push origin main`
    

---

### 3\. **Branch Commands:**

* **Check current branch:**  
    `git branch`
    
* **Rename branch to "main":**  
    `git branch -M main`
    
* **Switch to another branch:**  
    `git checkout <branch-name>`
    
* **Create and switch to a new branch:**  
    `git checkout -b <new-branch-name>`
    
* **Delete a branch:**  
    `git branch -d <branch-name>`
    

---

### 4\. **Merging Code:**

**Way 1:**

* **Compare branches/files:**  
    `git diff <branch-name>`
    
* **Merge branches:**  
    `git merge <branch-name>`
    

**Way 2:**

* **Create a Pull Request (PR):**  
    Use GitHub to review and merge changes.
    
* **Pull latest changes from the remote:**  
    `git pull origin main`
    

---

### 5\. **Resolving Merge Conflicts:**

This happens when Git can't automatically combine code. You'll need to review and fix the conflicting parts manually.

---

### 6\. **Undoing Changes:**

**Case 1: Undo staged changes**

* Reset specific files: `git reset <file-name>`
    
* Reset all staged changes: `git reset`
    

**Case 2: Undo last commit:**

* Undo one commit: `git reset HEAD~1`
    

**Case 3: Undo multiple commits:**

* Reset to a specific commit: `git reset <commit-hash>`
    
* Hard reset (delete all changes after a commit): `git reset --hard <commit-hash>`
    

---

### 7\. **Fork:**

A **fork** is a copy of someone else’s repository. You can use it to make changes independently. It shares the original repo's code and settings.  
Fork is a rough copy.