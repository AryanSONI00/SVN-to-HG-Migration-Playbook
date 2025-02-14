# 🎯 **Version Control Workflow: SVN & Mercurial**

## 🌟 **Introduction**
Version control systems (VCS) are essential tools for software development, enabling tracking of changes, collaboration, and efficient management of code. This document provides an insightful comparison of **Mercurial (Hg) 🐍** and **Subversion (SVN) 🏗️**, detailing their workflows, commands, and a comparison to help you choose the best for your project.

---

## 🔥 **What is Mercurial (Hg)?**
Mercurial is a **distributed version control system (DVCS)** that is **fast, scalable, and easy to use**. Unlike SVN, which depends on a central repository, Mercurial allows developers to maintain a full copy of the repository locally.

### ✅ **Advantages of Mercurial**
- 🚀 **Distributed Nature** – Every developer has a complete repository copy.
- ⚡ **High Performance** – Faster operations compared to SVN.
- 🤖 **Easy to Use** – Simpler commands than Git.
- 🔀 **Automatic Merging** – Better branching and merging capabilities.

📸 <img src="images/check-status.png" alt="Mercurial Setup" width="500">


---

## 🏗️ **What is Subversion (SVN)?**
Subversion is a **centralized version control system (CVCS)** where all changes are stored in a central repository. Developers check out a working copy, make changes, and commit them back to the server.

### ✅ **Advantages of SVN**
- 🔒 **Centralized Control** – Best for teams needing strict version control.
- 📁 **Efficient for Large Files** – Handles binary files better than Mercurial.
- 🔧 **Fine-Grained Permissions** – Allows directory-based permissions.

📸 <img src="images/svn-version.png" alt="Mercurial Setup" width="500">

---

## 🛠️ **Mercurial Workflow**
### 1️⃣ **Initializing a Mercurial Repository**
```sh
hg init my_project
cd my_project
echo "Hello, Mercurial" > file.txt
hg add file.txt
hg commit -m "Added file.txt"
```
📸 <img src="/images/check version and init.png.png" alt="Mercurial Setup" width="500">


### 2️⃣ **Branching & Merging**
```sh
hg branch my-branch
hg commit -m "created a new branch"
hg merge my-branch
```
📸  <img src="/images/branch.png" alt="Mercurial Setup" width="500">

### 3️⃣ **Checking Status & Log**
```sh
hg status
hg log
```
📸 <img src="/images/status and log.png" alt="Mercurial Setup" width="500">

---

## 🛠️ **SVN Workflow**
### 1️⃣ **Initializing an SVN Repository**
```sh
svnadmin create D:\svn
svn checkout file:///D:/svn D:\svn_working_copy
cd D:\svn_working_copy
```
📸 <img src="images/svn version.png" alt="Mercurial Setup" width="500">
<img src="images/svn checkout.png.png" alt="Mercurial Setup" width="500">


### 2️⃣ **Adding & Committing a File**
```sh
echo "Hello, SVN" > file.txt
svn add file.txt
svn commit -m "Added file.txt"
```


### 3️⃣ **Creating the SVN Directory Structure**
```sh
foreach ($dir in @("trunk", "branches", "tags")) { mkdir $dir }
svn commit -m "Created SVN directory structure"
```
📸 <img src="images/snv branch.png.png" alt="Mercurial Setup" width="500">


### 4️⃣ **Branching & Merging**
```sh
svn copy file:///D:/svn/trunk file:///D:/svn/branches/my-branch -m "Creating my-branch"
svn merge file:///D:/svn/branches/my-branch
svn commit -m "Merged my-branch into trunk"
```
📸 <img src="images/svn merge.png" alt="Mercurial Setup" width="500">


---

## ⚖️ **🆚 Mercurial vs. SVN: A Comparison**
| Feature        | 🐍 Mercurial (Hg) | 🏗️ Subversion (SVN) |
|--------------|-----------------|-----------------|
| **Type** | Distributed (DVCS) | Centralized (CVCS) |
| **Branching** | Easy and lightweight | More complex |
| **Speed** | Faster for local operations | Slower due to network dependency |
| **Offline Work** | Fully functional | Limited without server access |
| **Merge Handling** | Automatic and efficient | Manual conflict resolution required |
| **Setup Complexity** | Simple | More setup required |

📌 *Mercurial is ideal for distributed teams, while SVN works best for controlled environments.*

---

## 🎯 **Conclusion**
Both **Mercurial and SVN** have their strengths and weaknesses, making them suited for different types of projects. If you need a **fast, distributed workflow**, go for **Mercurial**. If you require **strict, centralized control**, **SVN** is the better option.

### 🚀 **Next Steps:**
✅ Upload this repository to GitHub.  
✅ Add screenshots inside the `screenshots/` folder.  
✅ Experiment with advanced commands like `hg rollback` and `svn revert`.  

📌 **Make sure to add all screenshots before pushing to GitHub!**

---

✍️ **Author:** Aryan Soni  
🔥 *Happy Version Controlling!* 🚀

