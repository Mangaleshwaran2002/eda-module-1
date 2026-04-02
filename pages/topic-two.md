# **Python Environment Management**

## **1. What is Environment Management?**

### **Definition**

Python Environment Management is the practice of creating **isolated workspaces** for different projects, where each workspace contains:

* Its own **Python interpreter**
* Its own **libraries (packages)**
* Its own **dependency versions**

---
layout: default
level: 2
hideInToc: true
---
# **Python Environment Management**

### **Why this matters**

In real-world projects:

* Applications depend on **external libraries** (not part of Python standard library)
* Different projects may require **different versions of the same library**
* Some projects depend on **older APIs**, while others need **latest updates**

👉 Without isolation, these differences create **dependency conflicts**

---
layout: default
level: 2
hideInToc: true
---

# **Python Environment Management**

## **2. Core Concept (Simple Understanding)**

Think of environment management like:

> 🧪 Each project gets its own **“mini Python setup”** instead of sharing one global setup.

So:

* Project A → Uses NumPy 1.10
* Project B → Uses NumPy 1.20

  ✔ No conflict because they are **separate environments**

---
layout: default
level: 2
hideInToc: true
---
# **Python Environment Management**

## **3. Why is Environment Management Necessary?**

#### **Problem Without Environment Management**

* All projects share:

  * Same Python installation
  * Same `site-packages` folder
* Leads to:

  * Version clashes
  * Breaking changes
  * Unstable projects

---
layout: default
level: 2
hideInToc: true
---
### **Solutions Provided by Environment Management**

## **1. Isolation**

* Each project runs independently
* Packages installed in one project:
  * ❌ Do NOT affect other projects
* Achieved using:
  * `venv`
  * `virtualenv`
  * `conda`
  * `poetry`

---
layout: default
level: 2
hideInToc: true
---
### **Solutions Provided by Environment Management**
## **2. Reproducibility**

* You can **recreate the exact same environment anywhere**
* Ensures:

  * Same behavior across systems
  * No “works on my machine” problem

### Common files:

* `requirements.txt`
* `pyproject.toml`

Example:

```bash
pip install -r requirements.txt
```
---
layout: default
level: 2
hideInToc: true
---
### **Solutions Provided by Environment Management**
## **3. System Integrity**

* Protects global Python environment
* Prevents:

  * OS-level Python breakage
  * Accidental package upgrades/downgrades

👉 Important because:

* Many OS tools depend on system Python

---
layout: default
level: 2
hideInToc: true
---

# **Python Environment Tools – Quick Comparison**

| Tool           | Type                  | Key Features                                      | Best Use Case                      |
| -------------- | --------------------- | ------------------------------------------------- | ---------------------------------- |
| **venv**       | Built-in              | Lightweight, simple virtual environments          | Small projects, basic isolation    |
| **virtualenv** | Third-party           | More features, supports older Python versions     | Legacy projects, extra flexibility |
| **Conda**      | Env + Package Manager | Handles Python & non-Python deps (e.g., CUDA)     | Data science, ML projects          |
| **Poetry**     | Dependency Manager    | Dependency resolution, `pyproject.toml`, lockfile | Structured Python projects         |
| **uv**         | Fast Package Manager  | Very fast, all-in-one env + dependency tool       | Modern workflows, high performance |


---
layout: default
level: 2
---

# **Creating Virtual Environments (venv)**

## **1. What is `venv`?**

* **`venv`** is a built-in Python module used to create **isolated virtual environments**
* Introduced in **Python 3.3+**
* It helps create a **separate workspace** for each project with its own:

  * Python interpreter
  * Installed packages

👉 Each environment is independent and does not interfere with others

---
layout: default
level: 2
hideInToc: true
---

## **2. How to Create a Virtual Environment**

### **Basic Command**

```bash
python -m venv tutorial-env
```

### **Explanation**

* `python -m venv` → Runs the venv module as a script
* `tutorial-env` → Name (or path) of the environment

👉 If the folder doesn’t exist, Python will **automatically create it**

---
layout: default
level: 2
hideInToc: true
---

## **3. What Happens Internally?**

When you run the command, Python:

* Creates a **new directory** for the environment
* Adds:

  * A **copy (or symlink)** of the Python interpreter
  * A **site-packages folder** for dependencies
  * Configuration files like `pyvenv.cfg`

👉 This structure allows Python to use **only the packages inside that environment**

---
layout: default
level: 2
hideInToc: true
---

## **4. Directory Structure (Conceptual)**

```
tutorial-env/
│
├── bin/ (Linux/Mac) or Scripts/ (Windows)
│   └── python (interpreter)
│
├── lib/
│   └── site-packages (installed libraries)
│
└── pyvenv.cfg
```

---
layout: default
level: 2
hideInToc: true
---

## **5. Common Naming Convention**

* A widely used standard name:

  ```bash
  .venv
  ```

### **Why `.venv`?**

* Keeps environment **inside project folder**
* Hidden by default (clean workspace)
* Easy to **ignore in Git**

👉 Recommended structure:

```
project-folder/
│
├── .venv/
├── src/
├── requirements.txt
```

---
layout: default
level: 2
hideInToc: true
---

# **Activating Virtual Environments**

<div>

Activation is the process of **switching your terminal to use the virtual environment** instead of the global Python.

</div>

👉 Technically:

* It modifies the **PATH variable**
* So `python` and `pip` point to the **virtual environment**, not system Python

---
layout: default
level: 2
hideInToc: true
---

## **2. Activation Commands**

<br/>

### **Windows (Command Prompt)**

```bash
tutorial-env\Scripts\activate
```

<br/>

### **Windows (PowerShell)**

```bash
tutorial-env\Scripts\Activate.ps1
```

<br/>

### **Linux / macOS**

```bash
source tutorial-env/bin/activate
```

---
layout: default
level: 2
hideInToc: true
---

## **3. How to Know It’s Activated**

After activation:

```bash
(tutorial-env) $
```

* The environment name appears in **parentheses**
* Indicates you are inside the virtual environment
* All installs (`pip install`) will now go into this environment

---
layout: default
level: 2
hideInToc: true
---


## **4. Why Activation is Important**

Without activation:

* Packages may install in **global Python**
* Can break other projects

With activation:

* ✔ Safe dependency installation
* ✔ Project-level isolation
* ✔ Controlled environment

---
layout: default
level: 2
hideInToc: true
---

## **5. Deactivating the Environment**

To exit the virtual environment:

```bash
deactivate
```

### **What happens after deactivation?**

* Terminal returns to **normal (global Python)**
* `(env-name)` disappears
* PATH is restored to original state

---
layout: default
level: 2
hideInToc: true
---

# **Managing Packages with pip**

## **1. What is `pip`?**

* **`pip`** is Python’s **package manager**
* Used to:

  * Install packages
  * Update packages
  * Remove packages
  * Manage dependencies

👉 It allows you to install libraries from **PyPI (Python Package Index)**

---
layout: default
level: 2
hideInToc: true
---

## **2. Installing Packages**

### **Install Latest Version**

```bash
python -m pip install pandas
```

* Installs the **latest available version**
* Downloads from PyPI and installs into your environment

### **Install Specific Version**

```bash
python -m pip install pandas==1.3.4
```

* Ensures **exact version control**
* Useful for:

  * Compatibility
  * Reproducibility

---
layout: default
level: 2
hideInToc: true
---

### **Re-running Install Command**

* If package already exists:

  * ✔ pip does **nothing (no duplicate install)**
* To change version → specify new version or upgrade

---
layout: default
level: 2
hideInToc: true
---

## **3. Upgrading Packages**

```bash
python -m pip install --upgrade pandas
```

* Updates package to **latest version**
* Does NOT reinstall if already up-to-date
* By default, only upgrades required dependencies when needed ([Pip][2])

## **4. Uninstalling Packages**

```bash
python -m pip uninstall requests
```

* Removes package from environment
* Safe way to clean unused dependencies

---
layout: default
level: 2
hideInToc: true
---

## **5. Listing Installed Packages**

```bash
python -m pip list
```

### **Output Example**

```bash
pandas==1.3.4
numpy==1.9.2
requests==2.7.0
```

* Shows all installed packages
* Human-readable format

👉 Difference:

* `pip list` → readable
* `pip freeze` → reproducible format

---
layout: default
level: 2
hideInToc: true
---

## **6. Creating requirements.txt**

```bash
python -m pip freeze > requirements.txt
```

* Saves all installed packages with versions
* Output format:

  ```
  package==version
  ```

👉 Used for **sharing and recreating environments**

---
layout: default
level: 2
hideInToc: true
---

## **7. Installing from requirements.txt**

```bash
python -m pip install -r requirements.txt
```

* Installs **exact same dependencies**
* Ensures:

  * Same versions
  * Same environment setup

---
layout: default
level: 2
hideInToc: true
---

## Comparison Table

| Feature                       | **venv**                    | **Poetry**                     | **uv**                     |
| ----------------------------- | --------------------------- | ------------------------------ | -------------------------- |
| **Type**                      | Built-in environment tool   | Dependency + project manager   | All-in-one modern tool     |
| **Primary Purpose**           | Create virtual environments | Manage dependencies + projects | Manage env + deps + Python |
| **Dependency Management**     | ❌ Manual (pip)              | ✅ Built-in                     | ✅ Built-in                 |
| **Speed**                     |  Slow (pip-based)         |  Medium                       |  Extremely fast         |
| **Lockfile Support**          | ❌ No                        | ✅ `poetry.lock`                | ✅ `uv.lock`                |
| **Virtual Environment**       | ✅ Yes                       | ✅ Yes                          | ✅ Yes (auto `.venv`)       |
---
level: 2
---

# **Managing Python Packages with UV**

## **1. What is `uv`?**

* **`uv`** is a modern, high-performance Python tool developed by **Astral**
* Written in **Rust**, making it extremely fast
* Designed as an **all-in-one replacement** for tools like:

  * `pip`
  * `venv`
  * `poetry`
  * `pyenv`

👉 It can be **10–100× faster than pip** and combines multiple tools into a single workflow

---
layout: default
level: 2
hideInToc: true
---

## **2. What Can UV Handle?**

`uv` simplifies the entire Python workflow by managing:

* ✅ Project initialization
* ✅ Python version installation & switching
* ✅ Dependency management
* ✅ Virtual environments (auto `.venv`)
* ✅ Running scripts and tools

👉 Essentially, it acts as a **complete project + environment + package manager** in one tool

---
layout: default
level: 2
hideInToc: true
---

## **3. Installing UV**

<br/>

### **macOS / Linux**

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

<br/>

### **Windows (PowerShell)**

```bash
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

<br/>

### **Using pip (Alternative)**

```bash
pip install uv
```

👉 Works like a normal Python package installation

---
layout: default
level: 2
hideInToc: true
---

## **4. Verify Installation**

```bash
uv --version
```

* Confirms that `uv` is installed correctly
* Displays installed version

---
layout: default
level: 2
hideInToc: true
---

## **5. Why Use UV? (Key Advantages)**

<br/>

### 🚀 Performance

* Extremely fast dependency resolution
* Uses caching and Rust-based execution

<br/>

### 🔧 All-in-One Tool

* Replaces multiple tools:

  * `pip` (package install)
  * `venv` (environment)
  * `pyenv` (Python versions)

---
layout: default
level: 2
hideInToc: true
---

### 📦 Modern Workflow

* Uses **lockfiles** and structured dependency management
* Supports scalable projects (workspaces)

<br/>

### ⚡ Developer Productivity

* Less setup, fewer tools to manage
* Cleaner and faster workflow

---
level: 2
hideInToc: true
---

# **Working with UV**

## **1. Creating a New Project & Environment**

### **Step 1: Create Project Folder**

```bash
mkdir my_uv_project
cd my_uv_project
```

---
level: 2
hideInToc: true
---


### **Step 2: Initialize Project**

```bash
uv init my_uv_project --python 3.11
```

### **What `uv init` does internally:**

* Creates a **project structure**
* Generates **`pyproject.toml`** (dependency configuration)
* Prepares environment setup (creates `.venv` when needed)
* Optionally adds starter files like `main.py`

👉 Note: `.venv` and `uv.lock` are often created **lazily** (when you run commands like `uv sync` or `uv run`) 

---
level: 2
hideInToc: true
---

## **2. Adding Packages**

### **Install a Package**

```bash
uv add pandas
```

### **Install Specific Version**

```bash
uv add pandas==1.3.4
```

### **What happens behind the scenes:**

* Updates **`pyproject.toml`**
* Resolves dependencies
* Creates/updates **`uv.lock`**
* Installs package into environment

---
level: 2
hideInToc: true
---


## **3. Removing Packages**

```bash
uv remove requests
```

### **What UV does:**

* Uninstalls the package
* Removes it from `pyproject.toml`
* Updates `uv.lock`

👉 Keeps your project **clean and consistent**

---
level: 2
hideInToc: true
---

## **4. Installing All Dependencies**

```bash
uv sync
```

### **Purpose:**

* Syncs environment with:

  * `pyproject.toml`
  * `uv.lock`

### **Key Behavior:**

* Installs missing packages
* Removes extra/unlisted packages
* Ensures **exact reproducibility**

---
level: 2
hideInToc: true
---


## **5. Upgrading Packages**

### **Upgrade a Specific Package**

```bash
uv lock --upgrade-package requests
uv sync
```

### **Upgrade All Packages**

```bash
uv lock --upgrade
uv sync
```

### **What happens:**

* Updates dependency versions in **lockfile**
* Applies changes to environment

---
level: 2
hideInToc: true
---


## **6. Core Workflow (Mental Model)**

👉 Think of UV workflow like this:

1. **Initialize project**

   ```bash
   uv init
   ```

2. **Add dependencies**

   ```bash
   uv add <package>
   ```

3. **Sync environment**

   ```bash
   uv sync
   ```

4. **Run project**

   ```bash
   uv run main.py
   ```

---
level: 2
hideInToc: true
---


## **7. Key Concepts to Remember**

###  `pyproject.toml` = Intent

* Defines **what you want** (dependencies)

###  `uv.lock` = Exact State

* Stores **exact versions**
* Ensures reproducibility

###  `uv sync` = Environment Builder

* Makes your environment match the lockfile

###  Automatic Environment Management

* `.venv` is handled automatically
* No manual activation required
