# **Version Control System (VCS)**

## **1. What is a Version Control System?**

### **Definition**

A **Version Control System (VCS)** is software that **tracks and manages changes** to files (such as source code) over time.

* It stores every modification in a structured way
* Allows you to **review, compare, and restore previous versions**
* Supports **multiple users working on the same project simultaneously**

👉 In simple terms:

> VCS = “History + Collaboration + Safety for your code”


---
level: 2
hideInToc: true
---


## **2. Why VCS is Important**

Without VCS:

* Developers overwrite each other’s work
* No proper backup or history
* Hard to track bugs

With VCS:

* ✔ Safe and structured development
* ✔ Easy collaboration
* ✔ Full traceability of changes

---
level: 2
hideInToc: true
---


## **3. Key Features & Benefits**

### **1. Version History**

* Tracks every change made to the project
* Stores details like:

  * Author
  * Timestamp
  * Description (commit message)

👉 Helps in debugging and auditing changes

---
level: 2
hideInToc: true
---

### **2. Reversion (Rollback)**

* Allows reverting:

  * A file
  * Or the entire project
* Useful when:

  * Bugs are introduced
  * Features break the system

👉 You can restore a **stable previous state instantly**

---
level: 2
hideInToc: true
---


### **3. Branching & Merging**

* **Branching**:

  * Create separate copies of code for:

    * Features
    * Experiments
    * Bug fixes

* **Merging**:

  * Combine changes back into main codebase

👉 Enables **parallel development without conflicts**

---
level: 2
hideInToc: true
---


### **4. Collaboration**

* Multiple developers can:

  * Work simultaneously
  * Share updates
  * Avoid overwriting each other’s work

👉 Eliminates problems like:

```
final_v1.py
final_v2.py
final_final.py 😅
```

---
level: 2
hideInToc: true
---

## **4. Core Concepts**

* **Repository (Repo)** → Storage of project + history
* **Commit** → Snapshot of changes
* **Branch** → Independent line of development
* **Merge** → Combining branches

👉 These concepts form the backbone of tools like **Git**

---
level: 2
hideInToc: true
---

## **5. Key Points to Remember**

###  VCS = Change Tracking System

Tracks every modification over time

###  Acts as a Safety Net

You can always go back to a working version


###  Enables Team Collaboration

Multiple developers → one codebase → no conflicts


###  Essential for Modern Development

Used in:
* Software engineering
* Data science projects
* DevOps workflows

---
layout: default
level: 2
---

# **Types of Version Control Systems**

## **1. Local Version Control System (Local VCS)**

### **Definition**

A Local VCS stores all project files and version history **only on your personal computer**.

### **Key Characteristics**

* All changes are saved in a **local database**
* No internet or server required
* Single-user system (no collaboration)

### **Use Case**

* Individual developers
* Small personal projects

### **Limitations**

* ❌ No collaboration support
* ❌ Risk of data loss if system fails

---
level: 2
hideInToc: true
---


## **2. Centralized Version Control System (CVCS)**

### **Definition**

A Centralized VCS uses a **single central server** to store all files and version history. Developers connect to this server to access and update code.

### **Key Characteristics**

* One **central repository (server)**
* Developers **pull (update)** and **commit changes** to the server
* All history is stored centrally

### **Advantages**

* ✔ Easy collaboration
* ✔ Central control and access management

### **Limitations**

* ❌ Server dependency (single point of failure)
* ❌ Cannot work fully offline

---
level: 2
hideInToc: true
---


## **3. Distributed Version Control System (DVCS)**

### **Definition**

A Distributed VCS allows every developer to have a **complete copy of the repository**, including full history, on their own machine.

### **Key Characteristics**

* Each developer has a **full local repository**
* Supports **offline work**
* Changes are shared via **push/pull operations**

### **Advantages**

* ✔ No single point of failure
* ✔ Faster operations (local commits, branching)
* ✔ Full offline capability

### **Limitations**

* ⚠️ Slightly more complex than CVCS


---
level: 2
hideInToc: true
---


## **4. Quick Comparison**

| Feature       | Local VCS        | CVCS                | DVCS                  |
| ------------- | ---------------- | ------------------- | --------------------- |
| Storage       | Local machine    | Central server      | Local + shared        |
| Collaboration | ❌ No             | ✅ Yes               | ✅ Yes                 |
| Offline Work  | ✅ Yes            | ❌ Limited           | ✅ Yes                 |
| Risk          | High (data loss) | Server failure risk | Low (multiple copies) |
| Complexity    | Simple           | Moderate            | Advanced              |
 
---
layout: default
level: 2
---

# **Git Version Control**

## **1. What is Git?**

### **Definition**

**Git** is a **Distributed Version Control System (DVCS)** that allows developers to:

* Work on their own **local copies** of a project
* Track changes efficiently
* Collaborate by sharing updates through a shared repository

👉 In simple terms:

> Git = “Distributed system for tracking and managing code changes”


---
level: 2
hideInToc: true
---


### **Key Highlights**

* Decentralized (no single dependency on server)
* Each developer has a **complete copy of project history**
* Fast, scalable, and reliable
* Created by **Linus Torvalds** in 2005

👉 Git is now the **industry standard for version control**

---
level: 2
hideInToc: true
---

## **2. Why Git is Powerful**

* ✔ No single point of failure
* ✔ Supports offline work
* ✔ Efficient handling of large projects
* ✔ Enables seamless team collaboration


---
level: 2
hideInToc: true
---

# **3. Core Characteristics of Git**

## **1. Version Control**

* Tracks changes to files over time
* Maintains **complete history of modifications**
* Allows rollback to previous stable versions

👉 Helps in debugging and auditing


---
level: 2
hideInToc: true
---


## **2. Distributed Nature**

* Every developer has:

  * Full repository
  * Complete history

* Enables:

  * Offline commits
  * Independent workflows

👉 Makes Git **highly resilient and fast**


---
level: 2
hideInToc: true
---


## **3. Branching**

* Create separate branches for:

  * Features
  * Bug fixes
  * Experiments

* Branches are:

  * Lightweight
  * Independent

👉 Multiple developers can work simultaneously without conflicts


---
level: 2
hideInToc: true
---


## **4. Merging**

* Combines changes from different branches
* Integrates completed work into main branch

👉 Includes tools to **resolve merge conflicts**


---
level: 2
hideInToc: true
---


## **5. Remote Repositories**

* Store code on remote servers
* Enable collaboration across teams

### Common Platforms:

* GitHub
* GitLab
* Bitbucket

👉 Supports:

* Push (upload changes)
* Pull (download updates)


---
level: 2
hideInToc: true
---


## **6. Committing**

* Saves changes as **snapshots (commits)**
* Each commit includes:

  * Unique ID (hash)
  * Author
  * Timestamp
  * Message

👉 Acts like a **checkpoint system**


---
level: 2
hideInToc: true
---


## **7. External Vendors / Hosting Services**

* Provide additional features:

  * Code reviews
  * Issue tracking
  * CI/CD pipelines

👉 Extend Git into a **complete collaboration platform**


---
level: 2
hideInToc: true
---


## **4. Key Concepts to Remember**

###  Git = Distributed System

Not dependent on a central server

###  Commit = Snapshot

Each commit represents a version of the project

###  Branch = Parallel Work

Independent development line

###  Merge = Integration

Combine work safely

###  Remote = Collaboration Layer

Share and sync code across teams

---
layout: default
level: 2
hideInToc: true
---

# **Git Workflow**

<div>

Git workflow defines the **standard sequence of actions** developers follow while working on a project using Git.

</div>

👉 In simple terms:

> Git Workflow = “How code moves from your system → to the team repository”

---
layout: default
level: 2
hideInToc: true
---


## **1. Clone**

### **Definition**

* Copy a remote repository to your local machine

### **Purpose**

* Get full project code + history

### **Command**

```bash
git clone <repository-url>
```

👉 Creates a **local working copy** of the project

---
layout: default
level: 2
hideInToc: true
---


## **2. Branch**

### **Definition**

* Create a separate line of development

### **Purpose**

* Work on features or fixes **without affecting main code**

### **Command**

```bash
git branch feature-name
git checkout feature-name
```

👉 Keeps your changes **isolated and safe**

---
layout: default
level: 2
hideInToc: true
---


## **3. Work**

### **Definition**

* Modify project files

### **Examples**

* Add new features
* Fix bugs
* Update existing code

👉 Changes are still **unstaged (not tracked yet)**

---
layout: default
level: 2
hideInToc: true
---


## **4. Commit**

### **Definition**

* Save changes as a **snapshot** in local repository

### **Purpose**

* Track progress step-by-step

### **Command**

```bash
git add .
git commit -m "Added new feature"
```

👉 Each commit includes:

* Unique ID
* Author
* Timestamp
* Message

---
layout: default
level: 2
hideInToc: true
---


## **5. Pull**

### **Definition**

* Fetch and merge latest changes from remote repository

### **Purpose**

* Stay updated with team changes

### **Command**

```bash
git pull origin main
```

👉 Prevents conflicts before pushing

---
layout: default
level: 2
hideInToc: true
---


## **6. Merge**

### **Definition**

* Combine your branch changes into another branch (usually main)

### **Purpose**

* Integrate completed work

### **Command**

```bash
git merge feature-name
```

👉 May require **conflict resolution** if changes overlap

---
layout: default
level: 2
hideInToc: true
---


## **7. Push**

### **Definition**

* Upload your commits to remote repository

### **Purpose**

* Share your work with team

### **Command**

```bash
git push origin feature-name
```

👉 Makes your code available for:

* Review
* Collaboration
* Deployment

---
layout: default
level: 2
hideInToc: true
---

## **8. Real-World Flow (Simplified)**

```bash
git clone repo-url
cd project

git checkout -b feature-login

# Work on code
git add .
git commit -m "Login feature added"

git pull origin main
git push origin feature-login
```

---
layout: default
level: 2
hideInToc: true
---

# **Basic Git Commands (Step-by-Step Guide)**

This section explains how to **create a project, track changes, and commit them using Git**.

## **Step 1: Create a Project Folder**

```bash
mkdir demo
cd demo
```

### **Explanation**

* `mkdir demo` → Creates a new folder
* `cd demo` → Moves into that folder

👉 This will be your **working directory (project space)**

---
layout: default
level: 2
hideInToc: true
---

## **Step 2: Initialize a Git Repository**

```bash
git init
```

### **What happens?**

* Converts your folder into a **Git repository**
* Creates a hidden `.git/` directory to store history

👉 This is where Git stores all version data

---
layout: default
level: 2
hideInToc: true
---

## **Step 3: Create a File and Add Content**

```bash
echo "Hello Git" > demo.txt
```

### **Explanation**

* Creates a file `demo.txt`
* Adds text content inside it

👉 This file is currently **untracked by Git**

---
layout: default
level: 2
hideInToc: true
---

## **Step 4: Add File to Staging Area**

```bash
git add .
```

### **Explanation**

* Moves files from:

  * Working Directory → **Staging Area**
* `.` means **add all files**

👉 Staging allows you to **select what goes into the next commit**

---
layout: default
level: 2
hideInToc: true
---

### **Check Status**

```bash
git status
```

👉 Shows:

* Current branch
* Staged files
* Untracked files

---
layout: default
level: 2
hideInToc: true
---

## **Step 5: Commit the File**

```bash
git commit -m "First commit"
```

### **Explanation**

* Saves changes as a **snapshot (commit)**
* `-m` → message describing the change

👉 A commit records:

* What changed
* Who changed it
* When it was changed

---
layout: default
level: 2
hideInToc: true
---

## **Step 6: Configure Git (If Required)**

If Git is not configured, you’ll see an identity error.

### **Fix it using:**

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

### **Why this is needed?**

* Git attaches **author information** to each commit

---
layout: default
level: 2
hideInToc: true
---

## **Step 7: Commit Again**

```bash
git commit -m "First commit"
```

### **Sample Output**

```bash
[master (root-commit) abc1234] First commit
 1 file changed, 1 insertion(+)
 create mode 100644 demo.txt
```

👉 Indicates:

* First commit created
* File successfully tracked

---
layout: default
level: 2
hideInToc: true
---

# **Core Concept: File Lifecycle in Git**

```bash
Untracked → Staged → Committed
```

* `git add` → moves to **Staged**
* `git commit` → moves to **Committed**

👉 This is the **core Git workflow**

---
layout: default
level: 2
hideInToc: true
---

## **Key Points to Remember**

###  `git init`

* Starts version control

###  `git add`

* Prepares files for commit

###  `git commit`

* Saves snapshot of changes

###  `git status`

* Shows current state

---
layout: default
level: 2
hideInToc: true
---

# **Git Branch**

## **1. What is a Git Branch?**

### **Definition**

A **Git branch** is a **lightweight pointer to a sequence of commits**, allowing developers to work on different features or fixes **independently from the main codebase**.

👉 In simple terms:

> Branch = “Separate workspace to develop without affecting main code”


---
layout: default
level: 2
hideInToc: true
---



## **2. Why Branching is Important**

* ✔ Enables **parallel development**
* ✔ Keeps main branch (**main/master**) stable
* ✔ Allows safe experimentation
* ✔ Simplifies collaboration

👉 Branching is one of Git’s most powerful features


---
layout: default
level: 2
hideInToc: true
---



## **3. How Branching Works (Conceptual)**

<img src="https://images.openai.com/static-rsc-4/3iCNgN4B3DsSUEVNAaj9PVACy1oSkOZWtH2StHxpP8X0LYHMKICgsG211xDy2Q2hKZ_a1owXiR9Kpr8rozJcG-YRWID3KK24LWJlJ2d0wEydFJGr1ootyied--D1p5IdvqetkPUvTQIVQiIz2f829r0VdTxtrAiv6IJz4qrtdKjWos3vlWZLUPxwMmn0Cv13?purpose=fullsize" class="m-2" />

* Each branch points to a **commit**
* New commits move the branch forward
* Branches can later be **merged back together**


---
layout: default
level: 2
hideInToc: true
---



# **4. Basic Git Branch Commands**

## **1. View All Branches**

```bash
git branch
```

### **Output Example**

```bash
* main
  feature-login
  bug-fix
```

* `*` → Current active branch


---
layout: default
level: 2
hideInToc: true
---



## **2. Create a New Branch**

```bash
git branch feature-payment
git branch
```

### **Output Example**

```bash
* main
  feature-login
  feature-payment
  bug-fix
```

### **Key Point**

* Creates branch but **does NOT switch to it**
* You remain on the current branch (`main`)


---
layout: default
level: 2
hideInToc: true
---



## **3. Switch to a Branch**

```bash
git switch feature-payment
```

### **Alternative (older)**

```bash
git checkout feature-payment
```

### **Output Example**

```bash
  main
  feature-login
*  feature-payment
  bug-fix
```

👉 Moves your working directory to that branch


---
layout: default
level: 2
hideInToc: true
---



## **4. Create and Switch (One Step)**

```bash
git switch -c feature-cart
```

### **Alternative**

```bash
git checkout -b feature-cart
```


### **Output Example**

```bash
  main
*  feature-cart
  feature-login
  bug-fix
```


👉 Most commonly used command in real projects


---
layout: default
level: 2
hideInToc: true
---



## **5. Merge a Branch**

### **Step 1: Switch to main**

```bash
git switch main
```

### **Step 2: Merge**

```bash
git merge feature-cart
```

### **What happens?**

* Combines feature branch into main
* May result in:

  * ✔ Fast-forward merge
  * ⚠️ Merge conflicts (if overlapping changes)


---
layout: default
level: 2
hideInToc: true
---



## **6. Delete a Branch**

```bash
git branch -d feature-cart
```

### **Force Delete**

```bash
git branch -D feature-cart
```

### **Output Example**

```bash
* main
  feature-login
  bug-fix
```

👉 Used after merging to keep repo clean


---
layout: default
level: 2
hideInToc: true
---



# **5. Branch Workflow (Real-World)**

```bash
git checkout -b feature-login
# work on code
git add .
git commit -m "Login feature"

git checkout main
git merge feature-login
git branch -d feature-login
```


---
layout: default
level: 2
hideInToc: true
---



## **6. Key Concepts to Remember**

###  Branch = Pointer

Not a copy of files, just a reference to commits

###  Lightweight & Fast

Creating branches is **instant in Git**

###  Isolation

Work safely without affecting main code


###  Merge = Integration

Combine completed work into main branch


---
layout: default
level: 2
hideInToc: true
---



## **7. Quick Summary**

* `git branch` → list branches
* `git branch name` → create branch
* `git switch name` → switch branch
* `git switch -c name` → create + switch
* `git merge name` → merge branch
* `git branch -d name` → delete branch

---
layout: default
level: 2
hideInToc: true
---

# **Git Merge**

## **1. What is Git Merge?**

### **Definition**

**Git merge** is the process of **combining changes from one branch into another**.

👉 In simple terms:

> Merge = “Bring feature work back into main branch”

---
layout: default
level: 2
hideInToc: true
---

## **2. Why Do We Use Merge?**

* Integrate completed features into main branch
* Combine work from multiple developers
* Maintain a **single, updated codebase**

---
layout: default
level: 2
hideInToc: true
---

## **3. How Merge Works (Conceptual)**

<img src="https://images.openai.com/static-rsc-4/sP6-d6NDB3C9kotd6RjH632lzZ5-Pw82WCQ3vVqGW5mbPSWyJMiQlw7R_DYC-lfz43TxYAzSJrtIlBYmYvBUzsNQfg_afIQ5zNSFnOSOHF5_nx3nS3jWIdYsSxlT7zU0ttKZeCtoiBkDdQx9uWbpLxAh_LDHvvyMDQVvTBRybBCpMs0J0j66pmKJDUBM1bwb?purpose=fullsize" class="m-2" width=600>

* Two branches diverge
* Changes are made independently
* Merge combines them into one branch

---
layout: default
level: 2
hideInToc: true
---

# **4. Basic Git Merge Commands**

## **1. Switch to Target Branch**

```bash
git switch main
```

### **Explanation**

* Move to the branch where you want changes added
* Usually the **main branch**

---
layout: default
level: 2
hideInToc: true
---

## **2. Merge the Feature Branch**

```bash
git merge feature-login
```

### **What happens?**

* Git combines changes from `feature-login` into `main`
* Updates commit history

---
layout: default
level: 2
hideInToc: true
---

## **3. Full Example Workflow**

```bash
git branch
git switch feature-login
# make changes and commit

git switch main
git merge feature-login
```

### **Sample Output**

```bash
Updating a1b2c3d..d4e5f6g
Fast-forward
 login.js | 5 +++++
 1 file changed, 5 insertions(+)
```

👉 **Fast-forward merge** means:

* No conflicts
* Direct linear update

---
layout: default
level: 2
hideInToc: true
---

# **5. Merge Conflict**

## **What is a Merge Conflict?**

Occurs when:

* Two branches modify the **same part of a file**
* Git cannot decide which change to keep

### **Sample Conflict Output**

```bash
Auto-merging file.txt
CONFLICT (content): Merge conflict in file.txt
Automatic merge failed; fix conflicts and then commit the result.
```

---
layout: default
level: 2
hideInToc: true
---

## **6. How to Resolve Conflicts**

### **Step 1: Open the File**

You will see:

```text
This is main branch code
=======
This is feature branch code
```

### **Step 2: Edit Manually**

Choose or combine:

```text
This is final correct code
```

### **Step 3: Mark as Resolved**

```bash
git add file.txt
```

### **Step 4: Commit**

```bash
git commit
```

👉 Conflict resolved and merge completed

---
layout: default
level: 2
hideInToc: true
---

# **7. Types of Merge**

### **1. Fast-Forward Merge**

* No divergence
* Simple linear update

### **2. Three-Way Merge**

* Branches diverged
* Creates a **merge commit**

---
layout: default
level: 2
hideInToc: true
---

## **8. Key Concepts to Remember**

###  Merge = Integration

Combines changes from branches

###  Always Switch First

Merge into the branch you are currently on

###  Conflicts are Normal

Handled manually when needed

###  Commit After Conflict

Merge completes only after resolving conflicts

---
layout: default
level: 2
hideInToc: true
---

## **9. Quick Summary**

* `git switch main` → go to target branch
* `git merge branch-name` → merge changes
* Resolve conflicts if any
* Commit final result

---
layout: default
level: 2
hideInToc: true
---

# **Git Remote**

## **1. What is Git Remote?**

### **Definition**

A **Git remote** is a **reference (connection) to another repository** hosted outside your local system (usually on platforms like GitHub, GitLab, etc.).

👉 In simple terms:

> Remote = “Your project stored somewhere else (server/cloud)”

---
layout: default
level: 2
hideInToc: true
---

### **Why Remote is Important**

* Enables **team collaboration**
* Allows:

  * Push (upload your code)
  * Pull (download others’ code)
* Keeps projects **synchronized across developers**

📌 Git uses remotes to **transfer data between repositories**

---
layout: default
level: 2
hideInToc: true
---

# **2. How Remote Works (Conceptual)**


* Local repository → your system
* Remote repository → server (GitHub, GitLab, etc.)
* Communication happens via:

  * `push`
  * `pull`
  * `fetch`

---
layout: default
level: 2
hideInToc: true
---

# **3. Basic Git Remote Commands**

## **1. View Remotes**

```bash
git remote
```

### **Output Example**

```bash
origin
```

### **Explanation**

* Lists remote names (shortnames)
* `origin` = default name for cloned repository

---
layout: default
level: 2
hideInToc: true
---

## **2. View Remotes with URLs**

```bash
git remote -v
```

### **Output Example**

```bash
origin  https://github.com/user/repo.git (fetch)
origin  https://github.com/user/repo.git (push)
```

### **Explanation**

* Shows:

  * Remote name
  * Remote URL
* Separate entries for:

  * Fetch (download)
  * Push (upload)

---
layout: default
level: 2
hideInToc: true
---

## **3. Add a New Remote**

```bash
git remote add upstream https://github.com/original/repo.git
git remote -v
```

### **Explanation**

* Connects your repo to another remote
* Common naming:

  * `origin` → your repo
  * `upstream` → original repo

👉 Useful in **fork workflows**

---
layout: default
level: 2
hideInToc: true
---

## **4. Remove a Remote**

```bash
git remote remove upstream
git remote -v
```

### **Explanation**

* Removes connection from local repo
* ❗ Does NOT delete actual remote repository

---
layout: default
level: 2
hideInToc: true
---

## **5. Fetch from Remote**

```bash
git fetch origin
```

### **What it does**

* Downloads latest changes
* Does NOT modify your working files

👉 Updates **remote-tracking branches only**

---
layout: default
level: 2
hideInToc: true
---

## **6. Pull from Remote**

```bash
git pull origin main
```

### **What it does**

* Fetch + Merge

👉 Updates your local branch with latest changes

---
layout: default
level: 2
hideInToc: true
---

## **7. Push to Remote**

```bash
git push origin main
```

### **What it does**

* Uploads your commits to remote

👉 Makes your code available to team

---
layout: default
level: 2
hideInToc: true
---

# **4. Key Concepts to Remember**

###  Remote = External Repository

Stored outside your local machine

###  origin (Default Remote)

* Automatically created during clone
* Acts as shortcut for remote URL

###  fetch vs pull

* `fetch` → download only
* `pull` → download + merge

###  push = Share Your Work

Uploads local commits

---
layout: default
level: 2
hideInToc: true
---

# **5. Quick Summary**

* `git remote` → list remotes
* `git remote -v` → show URLs
* `git remote add name url` → add remote
* `git remote remove name` → remove remote
* `git fetch` → download changes
* `git pull` → download + merge
* `git push` → upload changes


---
layout: full
---

# **What is `.gitignore`?**

## **1. Definition**

A **`.gitignore`** file is a configuration file used in **Git** to specify **which files and directories should NOT be tracked** by Git.

👉 In simple terms:

> `.gitignore` = “Tell Git what to ignore”

📌 It ensures that unnecessary or sensitive files are **excluded from version control**

---
layout: default
level: 2
hideInToc: true
---

## **2. Why Do We Use `.gitignore`?**

### **Main Purpose**

* Keep repository **clean and focused**
* Avoid committing:

  * Temporary files
  * Build outputs
  * Sensitive data

👉 Only important files (code + config) are tracked

---
layout: default
level: 2
hideInToc: true
---

## **3. Common Files to Ignore**

*  Temporary files → `.tmp`, `.log`
*  Build folders → `build/`, `dist/`
*  Dependencies → `node_modules/`
*  Environment files → `.env`
*  OS/IDE files → `.DS_Store`, `Thumbs.db`

👉 Prevents clutter and accidental exposure of sensitive data


---
layout: default
level: 2
hideInToc: true
---

## **4. How `.gitignore` Works**

<img src="https://media2.dev.to/dynamic/image/width=1280,height=720,fit=cover,gravity=auto,format=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fe2t3cfhkql3w6js9jbn8.png" class="m-2" width=400/>

* Git checks `.gitignore` before tracking files
* If a file matches a rule:

  * ❌ It is **ignored (not tracked)**
* Works using **pattern matching (rules)** 
---
layout: default
level: 2
hideInToc: true
---

# **5. Basic `.gitignore` Configuration**

## **1. Create `.gitignore` File**

```bash
touch .gitignore
```

### **Project Structure**

```bash
my-project/
├── .git/
├── .gitignore
├── src/
├── README.md
```

👉 `.gitignore` should be **committed to the repository**


---
layout: default
level: 2
hideInToc: true
---

## **2. Ignore Specific Files**

```bash
.env
```

👉 Git will ignore `.env` file completely



## **3. Ignore by Extension**

```bash
*.log
*.tmp
```

👉 Ignores all `.log` and `.tmp` files


---
layout: default
level: 2
hideInToc: true
---

## **4. Ignore Directories**

```bash
node_modules/
build/
```

👉 Ignores entire folders and their contents


## **5. Ignore Everything Except One File**

```bash
logs/*
!/logs/.gitkeep
```

👉 Ignore all files in `logs/` except `.gitkeep`


## **6. Ignore Files Anywhere**

```bash
.DS_Store
Thumbs.db
```

👉 Ignores these files in **any directory**


---
layout: default
level: 2
hideInToc: true
---

# **6. Important Rules**

###  Only Works for Untracked Files

* If file is already tracked:

  * `.gitignore` won’t affect it
* You must untrack first:

```bash
git rm --cached filename
```

👉 Then add it to `.gitignore`

---
layout: default
level: 2
hideInToc: true
---

###  Pattern-Based System

* Uses wildcards (`*`, `/`, `!`)
* Each line = one rule

###  Can Be Global or Local

* Project-level → `.gitignore`
* Global → system-wide ignore file


---
layout: default
level: 2
hideInToc: true
---

## **7. Quick Summary**

* `.gitignore` → ignore unwanted files
* Keeps repo:

  * Clean
  * Secure
  * Efficient
* Uses:

  * File names
  * Extensions
  * Directory rules
* Works only on **untracked files**
