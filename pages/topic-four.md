# **Code Quality & Formatting Tools**

## **1. What is Code Quality?**

### **Definition**

**Code quality** refers to how **reliable, maintainable, and efficient** a codebase is.

👉 In simple terms:

> Code Quality = “How good your code is in terms of readability, performance, and maintainability”



---
layout: default
level: 2
hideInToc: true
---

## **2. Why Code Quality Matters**

* ✔ Reduces bugs and errors
* ✔ Makes code easier to understand
* ✔ Improves collaboration among developers
* ✔ Simplifies maintenance and future updates
* ✔ Helps in scaling applications efficiently

👉 Poor quality code leads to:

* ❌ Technical debt
* ❌ Difficult debugging
* ❌ High maintenance cost


---
layout: default
level: 2
hideInToc: true
---

## **3. Characteristics of High-Quality Code**

### **1. Readability**

* Code is easy to read and understand
* Uses meaningful variable and function names
* Follows consistent formatting

👉 Helps new developers quickly understand the code

<img src="https://images.openai.com/static-rsc-4/WYMrrYbZC90-2MFK0P6x4E_nDtWjjJ2pSRPKwo3r1GnAcLvJquQLgHQHUdQ8lovXd9fmKDTNxmMPwNDNrKPZNvvx4GHM3HQWhxlNGuAaDVbBa3WRJsH2Ntm6s79Mo--MJiSnkT6_wBgNvQrt0KcKXn9M1TAjX2d7fP2gVSExNHEuRnXvDg_o5sqe2pNmUfp7?purpose=fullsize" class="m-2" width=400>



---
layout: default
level: 2
hideInToc: true
---

### **2. Maintainability**

* Code can be easily modified or extended
* Changes do not break existing functionality

👉 Reduces effort during updates and bug fixes


### **3. Efficiency**

* Optimized for:

  * Speed
  * Memory usage
* Avoids unnecessary computations

👉 Ensures better performance


---
layout: default
level: 2
hideInToc: true
---

### **4. Testability**

* Code is structured in a way that:

  * Makes testing easy
  * Supports unit and integration tests

👉 Helps ensure correctness and reliability


### **5. Security**

* Protects against vulnerabilities
* Handles inputs safely
* Follows secure coding practices

👉 Prevents attacks and data breaches


---
layout: default
level: 2
hideInToc: true
---

## **4. Key Points to Remember**

###  Clean Code = High Quality

Readable + maintainable + efficient

###  Focus on Simplicity

Avoid overly complex logic

###  Consistency Matters

Follow coding standards and conventions

###  Think Long-Term

Write code that is easy to scale and maintain


---
layout: full
level: 2
---
# **Black (Python Code Formatter)**

## **1. What is Black?**

### **Definition**

**Black** is an **opinionated Python code formatter** that automatically formats your code to follow **consistent style rules**.

👉 In simple terms:

> Black = “Auto-format your Python code consistently”


---
layout: default
level: 2
hideInToc: true
---

## **2. Why Use Black?**

* ✔ Enforces consistent code style
* ✔ Eliminates formatting debates in teams
* ✔ Improves readability
* ✔ Saves developer time
* ✔ Works well with Git and CI/CD

👉 Focus shifts from formatting → **writing logic**


---
layout: default
level: 2
hideInToc: true
---

## **3. Auto-formatting Philosophy**

### **1. Opinionated (Minimal Configuration)**

* Black enforces a fixed style
* Very few customization options

👉 No arguments in teams about formatting

### **2. PEP 8 Compliance**

* Follows Python’s official style guide (**PEP 8**)
* Enhances readability beyond basic rules


### **3. Deterministic Output**

* Same input → same formatted output
* Ensures consistency across environments

👉 Critical for CI/CD pipelines


---
layout: default
level: 2
hideInToc: true
---

### **4. Clean Git Diffs**

* Produces minimal and meaningful changes
* Avoids unnecessary formatting noise

👉 Easier code reviews


---
layout: default
level: 2
hideInToc: true
---

# **4. Usage in Scripts**

## **1. Installation**

```bash
pip install black
```

## **2. Format a File**

```bash
black your_script.py
```

👉 Automatically reformats the file

## **3. Format a Directory**

```bash
black your_project_folder/
```

👉 Formats all Python files inside the folder


---
layout: default
level: 2
hideInToc: true
---


## **4. Check Formatting (Without Applying)**

```bash
black --check your_script.py
```

👉 Used in CI/CD to validate formatting


## **5. Show Differences (Preview Changes)**

```bash
black --diff your_script.py
```

👉 Displays changes without modifying files


---
layout: default
level: 2
hideInToc: true
---

# **5. IDE Integration**

## **VS Code**

* Install Python extension
* Set:

  ```json
  "python.formatting.provider": "black"
  ```
* Enable:

  ```json
  "editor.formatOnSave": true
  ```

👉 Code formats automatically on save


---
layout: default
level: 2
hideInToc: true
---
## **PyCharm**

* Supports external formatters
* Configure Black in:

  * Settings → Tools → External Tools
  * Or File Watchers

## **Other Editors**

* Supported in:

  * Sublime Text
  * Vim
  * Emacs

👉 Plugins available for integration


---
layout: default
level: 2
hideInToc: true
---

# **6. Key Concepts to Remember**

###  Black = Opinionated Formatter

No need to decide formatting rules

###  Automates Code Style

Saves time and effort

###  Works Best with Git

Clean diffs + better collaboration

###  Ideal for Teams

Ensures consistent coding standards

---
layout: full
level: 2
---

# **Flake8 (Python Linting Tool)**

## **1. What is Flake8?**

### **Definition**

**Flake8** is a **Python linting tool** that performs **static code analysis** to detect:

* Style issues
* Logical errors
* Code complexity problems

👉 In simple terms:

> Flake8 = “Auto code reviewer for your Python code”


---
layout: default
level: 2
hideInToc: true
---

## **2. Core Idea Behind Flake8**

Flake8 is not just one tool — it is a **wrapper that combines multiple tools into one command**:

| Tool            | Responsibility                                               |
| --------------- | ------------------------------------------------------------ |
| **PyFlakes**    | Detects logical errors (unused imports, undefined variables) |
| **pycodestyle** | Checks PEP 8 style violations                                |
| **McCabe**      | Measures code complexity                                     |

👉 This unified approach makes Flake8 **powerful and efficient**

---
layout: default
level: 2
hideInToc: true
---

## **3. What is Linting?**

### **Definition**

Linting is the process of **analyzing code without running it** to find:

* Errors
* Bugs
* Style violations
* Potential security issues

👉 Think of it like:

> “Spell-check + grammar-check for your code”


---
layout: default
level: 2
hideInToc: true
---

## **4. Why Linting Matters**

* ✔ Detects bugs **before runtime**
* ✔ Improves code readability
* ✔ Enforces coding standards
* ✔ Saves debugging time
* ✔ Maintains consistent code quality

👉 Essential for **professional development workflows**


---
layout: default
level: 2
hideInToc: true
---

## **5. Common Flake8 Error Types**

### **1. Syntax / Structural Errors**

* `E999` → Syntax or indentation error


### **2. Style Violations (PEP 8)**

* `E501` → Line too long
* `E302` → Missing blank lines

### **3. Whitespace Issues**

* `W291` → Trailing whitespace


### **4. Logical Issues**

* `F401` → Unused import
* Undefined variables


---
layout: default
level: 2
hideInToc: true
---

### **5. Indentation Problems**

* `E101` → Mixed tabs and spaces

## **6. Error Code Classification**

| Code Prefix | Meaning               |
| ----------- | --------------------- |
| **E**       | Errors (style issues) |
| **W**       | Warnings              |
| **F**       | Logical errors        |

👉 Helps quickly identify the **type of problem**


---
layout: default
level: 2
hideInToc: true
---

## **7. How Flake8 Works**

* Scans your code files
* Applies multiple checks
* Outputs:

  * File name
  * Line number
  * Error code
  * Description

👉 Example:

```bash
app.py:10:1: F401 'os' imported but unused
```


---
layout: default
level: 2
hideInToc: true
---

# **8. Configuration using `.flake8`**

## **Create Config File**

```ini
[flake8]
max-line-length = 100
ignore = F401
exclude = __pycache__, .git
```

## **What You Can Customize**

* Ignore specific errors
* Set max line length
* Exclude folders/files
* Control complexity (`max-complexity`)

👉 Makes linting **project-specific and flexible**


---
layout: default
level: 2
hideInToc: true
---

## **Supported Config Files**

* `.flake8`
* `setup.cfg`
* `tox.ini`

👉 Centralized configuration avoids repeating CLI options

---
layout: default
level: 2
hideInToc: true
---

## **9. Key Concepts to Remember**

###  Flake8 = Linter

Focuses on **code quality, not formatting**


###  Static Analysis

Finds issues **without executing code**


###  Multi-tool Engine

Combines PyFlakes + pycodestyle + McCabe


###  Highly Configurable

Adapt rules based on project needs

---
layout: full
level: 2
---

# **Ruff (Modern Python Linter & Formatter)**

## **1. What is Ruff?**

### **Definition**

**Ruff** is a **high-performance Python linter and formatter** written in Rust that combines multiple tools into a **single, unified solution**.

👉 In simple terms:

> Ruff = “Black + Flake8 + isort + more → in one ultra-fast tool”

📌 It can replace tools like:

* Flake8 (linting)
* Black (formatting)
* isort (import sorting)
* pyupgrade, pydocstyle, etc.

---
layout: default
level: 2
hideInToc: true
---

## **2. Why Ruff is Popular**

* ✔ Eliminates need for multiple tools
* ✔ Extremely fast (10–100× faster)
* ✔ Simplifies project setup
* ✔ Works seamlessly with modern workflows

👉 Designed for **modern Python development (2024+)**


---
layout: default
level: 2
hideInToc: true
---

## **3. Key Features of Ruff**

### **1. Blazing Fast**

* Written in Rust
* Processes large codebases in milliseconds
* Uses parallel execution + caching

👉 Much faster than traditional Python tools

---
layout: default
level: 2
hideInToc: true
---

### **2. All-in-One Tool**

* Combines:

  * Linting
  * Formatting
  * Import sorting
  * Code modernization

👉 Replaces multiple dependencies with **one tool**

---
layout: default
level: 2
hideInToc: true
---

### **3. Comprehensive Rules**

* Supports **800+ rules**
* Includes rules from:

  * Flake8 plugins
  * pycodestyle
  * PyFlakes

👉 Covers both **style + logic issues**

---
layout: default
level: 2
hideInToc: true
---

### **4. Auto-Fix Capability**

```bash
ruff check --fix .
```

* Automatically fixes:

  * Unused imports
  * Formatting issues
  * Simple bugs

👉 Saves manual debugging time


---
layout: default
level: 2
hideInToc: true
---

### **5. Easy Integration**

* Works with:

  * VS Code
  * pre-commit hooks
  * CI/CD pipelines

👉 Can run on **every save / commit**


---
layout: default
level: 2
hideInToc: true
---

# **4. Basic Usage**

```bash
pip install ruff
```

<br/>

### **Lint Code**

```bash
ruff check .
```

<br/>

### **Auto-Fix Issues**

```bash
ruff check --fix .
```

<br/>

### **Format Code (Black alternative)**

```bash
ruff format .
```

---
layout: default
level: 2
hideInToc: true
---

# **5. Configuration (`pyproject.toml`)**

```toml
[tool.ruff]
line-length = 88
select = ["E", "F"]
ignore = ["E501"]

[tool.ruff.lint]
fixable = ["ALL"]
```

### **What You Can Configure**

* Line length
* Rules to enable/disable
* Auto-fix behavior
* File exclusions

👉 Single config replaces multiple config files


---
layout: default
level: 2
hideInToc: true
---

# **6. Black vs Flake8 vs Ruff (Comparison)**

## **Core Differences**

| Feature       | **Black**             | **Flake8**                 | **Ruff**            |
| ------------- | --------------------- | -------------------------- | ------------------- |
| Type          | Formatter             | Linter                     | Linter + Formatter  |
| Purpose       | Code style formatting | Detect bugs & style issues | All-in-one solution |
| Language      | Python                | Python                     | Rust                |
| Speed         | Fast                  | Moderate                   | Extremely fast      |
| Functionality | Formatting only       | Linting only               | Combines both       |


---
layout: default
level: 2
hideInToc: true
---

## **Advanced Comparison**

| Feature         | **Black**              | **Flake8**       | **Ruff**                   |
| --------------- | ---------------------- | ---------------- | -------------------------- |
| Auto Fix        | Yes                    | No               | Yes (`--fix`)              |
| Rules Support   | Style only             | PEP 8 + plugins  | 800+ rules                 |
| Large Codebases | Good                   | Slower           | Excellent                  |
| Config          | Minimal                | Multiple configs | Single config              |
| Best Use Case   | Formatting consistency | Bug detection    | Modern all-in-one workflow |


---
layout: default
level: 2
hideInToc: true
---

# **7. When to Use What?**

### Use **Black**

* If you only need formatting
* Simple projects

### Use **Flake8**

* Legacy projects
* Specific plugin requirements

### Use **Ruff (Recommended)**

* Modern projects
* Need speed + simplicity
* Want single tool instead of multiple

👉 Ruff is increasingly becoming the **default choice**

---
layout: default
level: 2
hideInToc: true
---

# **8. Key Concepts to Remember**

###  Ruff = All-in-One Tool

Replaces multiple tools

###  Extremely Fast

10–100× faster than traditional tools

###  Auto-Fix Support

Fix issues automatically

###  Centralized Config

Single `pyproject.toml`
