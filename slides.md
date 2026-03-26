---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://picsum.photos/id/88/1900/1080?blur=4
# some information about your slides (markdown enabled)
title: EDA Slides
info: |
  ## EDA (Exploratory Data Analysis) Slides
  Exploratory Data Analysis (EDA) is an approach to analyzing datasets using visual methods to summarize their key characteristics, detect outliers, and uncover patterns before applying machine learning models.
# apply UnoCSS classes to the current slide
class: text-center
# https://sli.dev/features/drawing
author: Mangaleshwaran K
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-up
# enable Comark Syntax: https://comark.dev/syntax/markdown
comark: true
# duration of the presentation
duration: 35min
# used for theme customization, will inject root styles as `--slidev-theme-x` for attribute `x`
themeConfig:
  primary: '#5d8392'
# favicon, can be a local file path or URL
favicon: 'https://faceprep.in/wp-content/uploads/2025/01/FACE-Prep-Site-icon-150x150.png'
# fonts will be auto-imported from Google fonts
# Learn more: https://sli.dev/custom/config-fonts.html
#fonts:
#  sans: Roboto
#  serif: Roboto Slab
#  mono: Fira Code
hideInToc: true

# aspect ratio for the slides
aspectRatio: 16/9

# make canvas take full screen
canvasWidth: 980

addons:
  - excalidraw
  - "@cxphoenix/slidev-addon-python-runner"

# Optional configuration for this runner
python:
  # Install packages from PyPI. Default: []
  installs: ["cowsay","pandas"]

  # Code executed to set up the environment. Default: ""
  prelude: |
    GREETING_FROM_PRELUDE = "Hello, Slidev!"

  # Automatically load the imported builtin packages. Default: true
  loadPackagesFromImports: true

  # Disable annoying warning from `pandas`. Default: true
  suppressDeprecationWarnings: true

  # Always reload the Python environment when the code changes. Default: false
  alwaysReload: false

  # Options passed to `loadPyodide`. Default: {}
  loadPyodideOptions: {}

---

# Exploratory Data Analysis (EDA)

#### By DataScience Mentor | FACEPrep Campus


---
layout: intro
hideInToc: true
---

# Module I: Reproducible Environments & Data Ingestion
By DataScience Mentor | FACEPrep Campus

---
layout: two-cols
layoutClass: gap-16
hideInToc: true
---

# Table of contents

![Table content](https://picsum.photos/500/700)

::right::

<Toc text-xs minDepth="1" maxDepth="2" />

---
transition: fade
---

# Exploratory Data Analysis
### What is EDA?
Exploratory Data Analysis is a data analytics process that aims to understand the data in depth and learn its different characteristics, often using visual means. This allows one to get a better feel for the data and find useful patterns.
![EDA image](https://www.simplilearn.com/ice9/free_resources_article_thumb/EDA/EDA_1.png)

--- 
layout: default
hideInToc: true
---
Exploratory data analysis can do all of this. It helps you gather insights, better sense the data, and remove irregularities and unnecessary values.

- Helps you prepare your dataset for analysis.
- Allows a machine learning model to predict our dataset better.
- Gives you more accurate results.
- It also helps us to choose a better machine learning model.

<br/>

### Why Exploratory Data Analysis Important  :
  - Understand dataset structure: number of features, their types, and data distribution
  - Discover patterns: find trends and relationships between variables
  - Detect errors: identify missing values, inconsistencies, and outliers
  - Select important features: focus on variables that impact the model most
  - Guide data preparation: decide on cleaning, scaling, and transformation methods
  - Improve modeling: choose suitable algorithms and tune them for better performance

--- 
layout: default
level: 2
---

# Types of Exploratory Data Analysis (EDA)
  1. Univariate Analysis

      - **Definition:** Focuses on analyzing a single variable at a time.
      - **Purpose:** To understand the variable's distribution, central tendency, and spread.
      - **Techniques:**<br/>
          Descriptive statistics (mean, median, mode, variance, standard deviation).
          Visualizations (histograms, box plots, bar charts, pie charts).

  2. Bivariate Analysis

      - **Definition:** Examines the relationship between two variables.
      - **Purpose:** To understand how one variable affects or is associated with another.
      - **Techniques:**<br/>
          Scatter plots.
          Correlation coefficients (Pearson, Spearman).
          Cross-tabulations and contingency tables.
          Visualizations (line plots, scatter plots, pair plots).

--- 
layout: default
hideInToc: true
---

  3. Multivariate Analysis

      - **Definition:** Investigates interactions between three or more variables.
      - **Purpose:** To understand the complex relationships and interactions in the data.
      - **Techniques:**<br/>
          Multivariate plots (pair plots, parallel coordinates plots).
          Dimensionality reduction techniques (PCA, t-SNE).
          Cluster analysis.

          Heatmaps and correlation matrices.


  4. Descriptive Statistics

      - **Definition:** Summarizes the main features of a data set.
      - **Purpose:** To provide a quick overview of the data.
      - **Techniques:**<br/>
          Measures of central tendency (mean, median, mode).
          Measures of dispersion (range, variance, standard deviation).
          Frequency distributions.

--- 
layout: default
hideInToc: true
---

  5. Graphical Analysis

      - **Definition:** Uses visual tools to explore data.
      - **Purpose:** To identify patterns, trends, and data anomalies through visualization.
      - **Techniques:**<br/>
          Charts (bar charts, histograms, pie charts).
          Plots (scatter plots, line plots, box plots).
          Advanced visualizations (heatmaps, violin plots, pair plots).

  6. Dimensionality Reduction

      - **Definition:** Reduces the number of variables under consideration.
      - **Purpose:** To simplify models, reduce computation time, and mitigate the curse of dimensionality.
      - **Techniques:**<br/>
          Principal Component Analysis (PCA).
          t-Distributed Stochastic Neighbor Embedding (t-SNE).
          Linear Discriminant Analysis (LDA).

--- 
layout: default
hideInToc: true
---


## Steps Involved in Exploratory Data Analysis

<br/>

**1. Understand the Data:** <br/>
  <div style="margin-left:20px">
  Familiarize yourself with the data set, understand the domain, and identify the objectives of the analysis.
  </div>

**2. Data Collection:** <br/>
  <div style="margin-left:20px">
  Collect the required data from various sources such as databases, web scraping, or APIs.
  </div>

**3. Data Cleaning:** <br/>
  <div style="margin-left:20px">
    Handle missing values: Impute or remove missing data.
    Remove duplicates: Ensure there are no duplicate records.
    Correct data types: Convert data types to appropriate formats.
    Fix errors: Address any inconsistencies or errors in the data.
  </div>

**4. Data Transformation:** <br/>
  <div style="margin-left:20px">
    Normalize or standardize the data if necessary.
    Create new features through feature engineering.
    Aggregate or disaggregate data based on analysis needs.
  </div>


--- 
layout: default
hideInToc: true
---

**5. Data Integration:** <br/>

  <div style="margin-left:20px">
  Integrate data from various sources to create a complete data set.
  </div>

**6. Data Exploration:** <br/>

  <div style="margin-left:20px">
    
  - Univariate Analysis: Analyze individual variables using summary statistics and visualizations (e.g., histograms, box plots).
  - Bivariate Analysis: Analyze the relationship between two variables with scatter plots, correlation coefficients, and cross-tabulations.
  - Multivariate Analysis: Investigate interactions between multiple variables using pair plots and correlation matrices.

  </div>

**7. Data Visualization:** <br/>
  <div style="margin-left:20px">
  Visualize data distributions and relationships using visual tools such as bar charts, line charts, scatter plots, heatmaps, and box plots.  
  </div>

--- 
layout: default
hideInToc: true
---

**8. Descriptive Statistics:** <br/>
  <div style="margin-left:20px">
  Calculate central tendency measures (mean, median, mode) and dispersion measures (range, variance, standard deviation).
  </div>


**9. Identify Patterns and Outliers:** <br/>
  <div style="margin-left:20px">
  Detect patterns, trends, and outliers in the data using visualizations and statistical methods.
  </div>

**10. Hypothesis Testing:** <br/>
  <div style="margin-left:20px">
Formulate and test hypotheses using statistical tests (e.g., t-tests, chi-square tests) to validate assumptions or relationships in the data.
  </div>

**11. Data Summarization:** <br/>
  <div style="margin-left:20px">
  Summarize findings with descriptive statistics, visualizations, and key insights.
  </div>


---
layout: default
---

# Python Environment Management

## What is Environmental Management?
Python environment management is
the practice of creating isolated environments for different projects to manage their specific Python interpreters, libraries, and dependencies, thereby preventing version conflicts and ensuring project reproducibility.

<br/>

<div style="margin-left:20px">
Python applications will often use packages and modules that don’t come as part of the standard library. Applications will sometimes need a specific version of a library, because the application may require that a particular bug has been fixed or the application may be written using an obsolete version of the library’s interface.
</div>

---
layout: default
level: 2
hideInToc: true
---


## Why is it Necessary?
In standard Python installations, all projects might share the same site-packages directory. This can lead to conflicts if two projects require different versions of the same library (e.g., Project A needs NumPy 1.10 and Project B needs NumPy 1.20). 
<br/>

Environment management solves this by: 
- Isolation: Each project gets its own dedicated folder containing a specific Python interpreter and its own set of installed packages, separate from the global Python installation.
- Reproducibility: The exact dependencies and versions needed for a project can be recorded (e.g., in a requirements.txt or pyproject.toml file), allowing others to recreate the exact same setup on their own machines.
- System Integrity: It prevents accidental modification or breaking of the system's global Python environment, which might be required for the operating system itself to function correctly. 


---
layout: default
level: 2
hideInToc: true
---


## Key Tools for Environment Management

| Tool       | Type                   | Key Features                                                               | Best For                                                                |
| ---------- | ---------------------- | -------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| venv       | Built-in (Python 3.3+) | Creates lightweight virtual environments using symbolic links              | Simple Python projects needing basic isolation                          |
| virtualenv | Third-party            | More feature-rich than venv, supports older Python versions                | Projects needing backward compatibility and extra features              |
| Conda      | Cross-platform         | Manages Python + non-Python dependencies (CUDA, C libraries, etc.)         | Data science, ML, and complex system dependency projects                |
| Poetry     | Dependency Manager     | Advanced dependency resolution, uses pyproject.toml, auto env management   | Projects needing structured dependency and packaging management         |
| uv         | Fast Package Manager   | Extremely fast (Rust-based), manages virtual envs and dependencies quickly | Modern Python workflows needing speed and efficient dependency handling |


---
layout: default
level: 2
---


## Creating Virtual Environments

The module used to create and manage virtual environments is called **venv**.  venv will install the Python version

- To create a virtual environment, decide upon a directory where you want to place it, and run the venv module as a script with the directory path:

```bash
python -m venv tutorial-env
```

- This will create the tutorial-env directory if it doesn’t exist, and also create directories inside it containing a copy of the Python interpreter and various supporting files.
- A common directory location for a virtual environment is ```.venv``` 

---
layout: default
level: 2
hideInToc: true
---


## Activate Virtual Environments

Once you’ve created a virtual environment, you may activate it.

On Windows, run:

```bash
tutorial-env\Scripts\activate
```

On Unix or MacOS, run:

```bash
source tutorial-env/bin/activate
```

To deactivate a virtual environment, type:

```bash
(tutorial-env) $ deactivate
```

---
layout: default
level: 2
hideInToc: true
---


## Managing Packages with pip

You can use a tool called <code>pip</code> to install, update, and remove Python packages.

To install the most recent version of a package, simply provide its name:

```bash
(tutorial-env) $ python -m pip install pandas
```

If you need a specific version, include the version number using == after the package name:

```bash
(tutorial-env) $ python -m pip install pandas==1.3.4
```

If you run the same install command again, pip will detect that the requested version is already installed and won’t make any changes. To install a different version, specify that version number, or you can upgrade the package to the latest version using:

```bash
(tutorial-env) $ python -m pip install --upgrade pandas
```
To remove packages from your environment:

```bash
(tutorial-env) $ python -m pip uninstall requests
```

---
layout: default
level: 2
hideInToc: true
---


## Managing Packages with pip


Listing Installed Packages

To see all packages installed in your environment:

```bash
(tutorial-env) $ python -m pip list
```

```bash [output]
pandas==1.3.4
numpy==1.9.2
requests==2.7.0
```

Installing from a requirements.txt File

You can save all your environment’s dependencies in a requirements.txt file


```bash
(tutorial-env) $ python -m pip freeze > requirements.txt
```


Other users (or another environment) can install the exact same packages with:

```bash
(tutorial-env) $ python -m pip install -r requirements.txt
```

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
layout: default
level: 2
hideInToc: true
---


## Comparison Table

| Feature                       | **venv**                    | **Poetry**                     | **uv**                     |
| ----------------------------- | --------------------------- | ------------------------------ | -------------------------- |
| **Python Version Management** | ❌ No                        | ❌ No                           | ✅ Yes                      |
| **Project Management**        | ❌ No                        | ✅ Strong                       | ✅ Moderate                 |
| **Tool Integration**          | ❌ None                      | ⚠️ Limited                     | ✅ Replaces multiple tools  |
| **Ease of Use**               | ✅ Very simple               | ⚠️ Moderate learning           | ✅ Simple + powerful        |
| **Flexibility**               | ✅ High (manual control)     | ❌ Opinionated                  | ✅ Very flexible            |
| **Standards Support**         | ⚠️ Basic                    | ⚠️ Partial (legacy formats)    | ✅ Full modern standards    |


---
level: 2
layout: two-cols
layoutClass: gap-10
---


## Managing Python Packages with UV

uv is a fast Python project and package manager developed by Astral. It handles:
  - Project initialization
  - Python version selection
  - Dependency management
  - Isolated environments
  - Tool execution

:: right ::

🚀 1. [Install UV][1]

Before you can use UV, you need to install it.

On macOS / Linux :

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

On Windows (PowerShell):
```bash
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex" 
```


Using PyPI:
```bash
pip install uv
```

Verify installation:
```bash
uv --version
```

[1]: https://docs.astral.sh/uv/getting-started/installation/ "Installing uv"


---
level: 2
hideInToc: true
---


### Creating a New Project & Environment

With UV you can initialize a new project, set up an isolated environment, and manage dependencies from one place.

Create a Project Directory

```bash
mkdir my_uv_project
cd my_uv_project
```

Initialize the Project

```bash
uv init my_uv_project --python 3.11
```

This does a few things for you:
- Creates a project folder
- Generates a pyproject.toml (for dependency tracking)
- Sets up an isolated .venv environment
- Optionally adds a sample Python file

---
level: 2
hideInToc: true
---

### Adding Packages

Instead of using pip install, UV lets you install packages directly into your environment with:

```bash
uv add pandas
```

To install a specific version:

```bash
uv add pandas==1.3.4
```

This will:
- Update your pyproject.toml with the package
- Create/update a lockfile (uv.lock)
- Install the package into the environment

---
level: 2
hideInToc: true
---


### Removing Packages

To remove a package from your project:

```bash
uv remove requests
```

UV will:
- Uninstall the package
- Remove it from your project’s pyproject.toml
- Update the lockfile accordingly

<br/>

#### Installing All Dependencies

If you’ve cloned a project or updated your dependency files, run:

```bash
uv sync
```

This ensures your local environment matches exactly what’s defined in <code>uv.lock</code>.

---
level: 2
hideInToc: true
---


### Upgrading Packages

To upgrade a specific package:

```bash
uv lock --upgrade-package requests
uv sync
```

To upgrade all packages to the latest compatible versions:

```bash
uv lock --upgrade
uv sync
```

This updates the lockfile and applies changes to your environment.

---
level: 2
hideInToc: true
---


### Running Python Scripts

Because UV manages your virtual environment automatically, you can run Python scripts like this:

```bash
uv run python script.py
```

This ensures your script runs inside the project environment with all dependencies installed.

#### Using pip Commands via UV

If you like the familiar pip syntax but want UV’s speed, you can still run:

```bash
uv pip install requests
```

This acts like traditional pip install but inside the UV project context.

UV gives you the simplicity of pip plus the benefits of built‑in environment isolation, better dependency resolution, and reproducible lockfiles — all from a single tool

---
layout: default
---

# Version Control System 

### What is VCS?
A Version Control System (VCS) is software that records changes to files or projects over time, allowing users to track history, revert to previous versions, and collaborate seamlessly. It enables multiple developers to work on the same codebase simultaneously, manage changes, and resolve conflicts, ensuring code safety.

### Key Features & Benefits

- **Version History:** Tracks changes, showing who made changes, what was changed, and when.
- **Reversion:** Revert files or the entire project back to a previous state if errors occur.
- **Branching & Merging:** Developers can create separate branches for new features or experiments, then merge them back into the main codebase safely.
- **Collaboration:** Allows distributed, simultaneous work, eliminating the need to manually manage different file versions (e.g., final_v2.doc).

---
layout: default
level: 2
---

## Types of Version Control Systems

<img src="https://trio.dev/wp-content/uploads/2025/09/img-220-1024x597.png" width=800 style="margin-top:5px">


---
layout: default
level: 2
---

## Types of Version Control Systems
<br/>

1. Local Version Control
<div style="margin-left:20px"> 

  - All changes and history are stored on your own computer; useful for individual work or small projects.
  - This is the simplest form of version control with no collaboration features.

</div>

2. Centralized Version Control (CVCS)
<div style="margin-left:20px"> 

- One central server holds all files and version history; developers connect to it to get or save changes.
- Examples include systems like Subversion (SVN) and CVS.
- Good for smaller teams but depends on the server being available.

</div>
3. Distributed Version Control (DVCS)
<div style="margin-left:20px"> 

- Every developer has a full copy of the project’s history on their machine and can work offline.
- Tools like Git and Mercurial use this model.
- It’s flexible and supports offline commits and branching easily

</div>
 
---
layout: default
level: 2
---

## Git Version Control
<br/>
What is Git? <br/>
<div style="margin-left:20px"> 
Git is a distributed version control system, meaning that it allows developers to work on their own local copies of a project, while still enabling them to push changes to a shared repository.  Git has since become the standard for version control in the software development industry.
</div> 

<div style="margin-left:20px;margin-top:10px"> 

- Git manages and tracks code changes in a decentralized way.
- Every developer has a full copy of the project’s complete history.
- This design makes Git fast, scalable, and resilient to server failures.
- Created by Linus Torvalds in 2005

  To install Git, [click here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) to go official Git installation page.
</div> 
 


---
layout: two-cols
layoutClass: gap-10
level: 2
hideInToc: true
---

## Characteristics of Git:

**Version Control**
- Tracks and manages changes made to files over time.
- Maintains a complete history of modifications.
- Allows reverting to previous versions when needed.

**Distributed**
- Each developer has a full copy of the repository and its history locally.
- Enables work without constant internet access.
- Supports flexible and independent collaboration among developers.

::right::

**Branching**
- Allows creation of lightweight and independent branches.
- Helps isolate work for new features or bug fixes.
- Enables multiple developers to work simultaneously without affecting the main codebase.


**Merging**
- Combines changes from different branches into a single branch.
- Helps integrate completed features into the main project.
- Provides tools to resolve conflicts during integration.

---
layout: default
level: 2
hideInToc: true
---

## Characteristics of Git:

**Remote Repositories**
- Enables pushing and pulling code to/from remote servers.
- Facilitates collaboration among team members.
- Commonly used with platforms like GitHub and Bitbucket.

**Committing**
- Saves changes as snapshots of the project at specific points in time.
- Each commit has a unique ID and includes author and timestamp.
- Helps in tracking and understanding project history.

**External Vendors**
- Platforms like GitHub, GitLab, and Bitbucket host Git repositories.
- Provide features such as issue tracking and code reviews.
- Support project management and team collaboration.

---
layout: default
level: 2
hideInToc: true
---

## Git Workflows:

![git-workflow-image](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*Toe_JSAzbvMeWa4gabpehA.png)

---
layout: default
level: 2
hideInToc: true
---

## Git Workflows:

**Clone** − The first step is cloning a remote repository to your local machine. It creates a local copy of the project's files and history on your computer.

**Branch** − After having a clone of the repository, you can create a new branch to work on a specific task or feature. Branching isolates the local changes from main codebase until it can be merged.

**Work** − Changes that are made to the files in your branch, such as adding new features, fixing bugs, or making alterations.

**Commit** − As changes are made, you periodically commit them to your local repository. Each commit is represented as a snapshot of the project at a particular time.

**Pull** − To incorporate the changes made by other developers, you can pull the latest changes from the remote repository.

**Merge** − Once your work is completed and tested, you can merge the changes into the main branch. This integrates your changes with the rest of the project.

**Push** − The last step is to push your changes or local commits to the remote repository, so that your work is shared with other team members.

---
layout: default
level: 2
hideInToc: true
---

## Basic Git Commands

Once Git Bash is set up, you can start using it to manage your Git repositories. Here are some essential commands to get you started:

### Step 1: Create a Project Folder

Create a folder anywhere on your system.

```bash
mkdir demo
cd demo
```

### Step 2: Initialize a Git Repository

Open the terminal (in VS Code or system terminal) and run:

```bash
git init
```

**Sample Output:**

```bash
Initialized empty Git repository in /path/to/demo/.git/
```

---
layout: default
level: 2
hideInToc: true
---

### Step 3: Create a File and Add Content

Create a file (e.g., demo.txt) and add some text.

```bash
echo "Hello Git" > demo.txt
```

### Step 4: Add File to Staging Area

Add the file to Git staging:

```bash
git add .
```

Check the status:

```bash
git status
```

**Sample Output:**

```bash
On branch master
No commits yet
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   demo.txt
```

---
layout: default
level: 2
hideInToc: true
---

### Step 5: Commit the File

Try committing:

```bash
git commit -m "First commit"
```

### If Git is Not Configured:

You may see this message:

```bash
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address
```

---
layout: default
level: 2
hideInToc: true
---

### Step 6: Configure Git Username and Email

Run the following commands:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

### Step 7: Commit Again

Now retry the commit:

```bash
git commit -m "First commit"
```

**Sample Output:**

```bash
[master (root-commit) abc1234] First commit
 1 file changed, 1 insertion(+)
 create mode 100644 demo.txt
```

---
layout: default
level: 2
hideInToc: true
---

## Git Branch

<div style="margin-left:15px; margin-top:10px">
Git branching is a core feature that allows developers to diverge from the main line of development to work on new features or bug fixes in isolation without affecting the main project. Branches are lightweight pointers to a series of commits, making them fast and easy to create, switch between, and manage. 
</div>

<img src="https://os.novatorsoft.com/nvs-content/medium_branch_nedir_1_a4b3ed668c.webp" height=500 width=600 style="margin:15px" />

---
layout: default
level: 2
hideInToc: true
---

## Basic Git Branching Commands

<div style="margin:15px">

**1. View all branches**

Shows all branches in your project.

```bash
git branch
```

**Sample Output:**

```bash
* master
  feature-login
  bug-fix
```

- ( * ) means you are currently on the main branch.

</div>

---
layout: default
level: 2
hideInToc: true
---

## Basic Git Branching Commands

<div style="margin:15px">

**2. Create a new branch**

Creates a new branch but does **NOT switch** to it.

```bash
git branch feature-payment
git branch
```

**Sample Output:**

```bash
* main
  feature-login
  bug-fix
  feature-payment
```

- ( * ) means you are currently on the main branch.
- You are still on ```main``` .

</div>

---
layout: default
level: 2
hideInToc: true
---

## Basic Git Branching Commands

<div style="margin:15px">

**3. Switch to a branch**

Moves you to another branch.

```bash
git switch feature-payment
```

(or older way)

```bash
git checkout feature-payment
```

**Sample Output:**

```bash
Switched to branch 'feature-payment'
```

</div>

---
layout: default
level: 2
hideInToc: true
---

## Basic Git Branching Commands

<div style="margin:15px">

**4. Create and switch (one step)**

Creates a branch AND switches to it immediately.

```bash
git switch -c feature-cart
```

(or older way)

```bash
git checkout -b feature-cart
```

**Sample Output:**

```bash
Switched to a new branch 'feature-cart'
```

</div>

---
layout: default
level: 2
hideInToc: true
---

## Basic Git Branching Commands

<div style="margin:15px">

**5. Merge a branch**

Combine changes from one branch into another.

**Step 1: Go to main branch**

```bash
git switch main
```

**Step 2: Merge branch**
  
```bash
git merge feature-cart
```

**Sample Output:**

```bash
Updating a1b2c3d..d4e5f6g
Fast-forward
 file1.txt | 2 ++
 1 file changed, 2 insertions(+)
```

</div>

---
layout: default
level: 2
hideInToc: true
---

## Basic Git Branching Commands

<div style="margin:15px">

**6. Delete a branch**

Deletes a branch after merging.

```bash
git branch -d feature-cart
```

**Sample Output:**

```bash
Deleted branch feature-cart (was d4e5f6g).
```

Use force delete if needed:

```bash
git branch -D feature-cart
```

</div>

---
layout: default
level: 2
hideInToc: true
---

## Basic Git Branching Commands

<div style="margin:15px">

**🧠 Quick Summary**

- ```git branch``` → list branches
- ```git branch name``` → create branch
- ```git switch name``` → move to branch
- ```git switch -c name``` → create + switch
- ```git merge name``` → merge branch
- ```git branch -d name``` → delete branch

</div>

---
layout: default
level: 2
hideInToc: true
---

## Git Merge

<div style="margin-left:15px; margin-top:10px">

To merge branches in Git, you typically work on a separate feature branch and then integrate those changes back into your main branch.The process involves switching to your target branch (e.g., main), and then running the ```git merge``` command.

</div>

<img src="https://miro.medium.com/1*iB8lNrITmLvKeL8mnp3qAA.png" height=500 width=400 style="margin:15px" />


---
layout: default
level: 2
hideInToc: true
---

## Basic Git Merge Commands

<div style="margin:15px">

**1. Switch to target branch**

First, go to the branch where you want to add changes (usually main).

```bash
git switch main
```

**Sample Output:**

```bash
Switched to branch 'main'
```

</div>

<div style="margin:15px">

**2. Merge the feature branch**

Now merge your feature branch into main.

```bash
git merge feature-login
```

</div>

---
layout: default
level: 2
hideInToc: true
---

## Basic Git Merge Commands

<div style="margin:15px">

**3. Example (Full Flow)**

```bash
git branch
git switch feature-login
# make changes and commit

git switch main
git merge feature-login
```

**Sample Output:**

```bash
Updating a1b2c3d..d4e5f6g
Fast-forward
 login.js | 5 +++++
 1 file changed, 5 insertions(+)
```

- This means changes from ```feature-login``` are successfully added to main.

</div>

---
layout: two-cols
layoutClass: gap-10
level: 2
hideInToc: true
---

## Basic Git Merge Commands


**4. Merge Conflict (important 🚨)**
Sometimes Git can’t decide which change to keep.

**Sample Output:**

```bash
Auto-merging file.txt
CONFLICT (content): Merge conflict in file.txt
Automatic merge failed; fix conflicts and then commit the result.
```

<br/>

### Fix Conflict Steps:

1. Open the file
2. You’ll see:

```text
This is main branch code
This is feature branch code
```

:: right ::

3. Edit it manually:
```text
This is final correct code
```

4. Then run:

```bash
git add file.txt
git commit
```

---
layout: default
level: 2
hideInToc: true
---

## Git Remote 

<div style="margin-left:15px; margin-top:10px">

Git remote commands let you manage connections to other repositories, usually hosted online (like GitHub, GitLab, Bitbucket). This is how you collaborate with others, push your local changes, and pull their updates into your project.

</div>

<img src="https://flatlogic.com/blog/wp-content/uploads/2022/01/Untitled-2-1024x591.png" height=500 width=600 style="margin:15px" />

---
level: 2
hideInToc: true
---

## Basic Git Remote Commands


<div style="margin:15px">

**1. View Remotes**

Shows you the short names of your remote repositories.

```bash
git remote
```

**Sample Output:**

```bash
origin
```

- ```origin``` is the default name Git gives to the server you cloned from.

</div>

---
level: 2
hideInToc: true
---

## Basic Git Remote Commands


<div style="margin:15px">

**2. View Remotes with URLs**

Shows the short names and the URLs of your remote repositories.

```bash
git remote -v
```

**Sample Output:**

```bash
origin  https://github.com/yourusername/yourrepo.git (fetch)
origin  https://github.com/yourusername/yourrepo.git (push)
```

- You'll usually see two entries per remote: one for fetching (downloading) and one for pushing (uploading).

</div>

---
level: 2
hideInToc: true
---

## Basic Git Remote Commands


<div style="margin:15px">

**3. Add a New Remote**

Connects your local repository to a new remote repository.

```bash
git remote add upstream https://github.com/originalowner/originalrepo.git
git remote -v
```

**Sample Output:**

```bash
origin  https://github.com/yourusername/yourrepo.git (fetch)
origin  https://github.com/yourusername/yourrepo.git (push)
upstream  https://github.com/originalowner/originalrepo.git (fetch)
upstream  https://github.com/originalowner/originalrepo.git (push)
```

- upstream is often used to refer to the original repository you forked from.

</div>

---
level: 2
hideInToc: true
---

## Basic Git Remote Commands


<div style="margin:15px">

**4. Remove a Remote**

Disconnects your local repository from a remote.

```bash
git remote remove upstream
git remote -v
```

**Sample Output:**

```bash
origin  https://github.com/yourusername/yourrepo.git (fetch)
origin  https://github.com/yourusername/yourrepo.git (push)
```

- Careful! This doesn't delete the remote repository itself, just your local connection to it.

</div>

---
level: 2
hideInToc: true
---

## Basic Git Remote Commands


<div style="margin:15px">

**5. Fetch from a Remote**

Downloads new data from a remote repository into your local repository, but doesn't integrate it into your working files.

```bash
git fetch origin
```

**Sample Output:**

```bash
remote: Counting objects: 5, done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/yourusername/yourrepo
 * [new branch]      feature-payment -> origin/feature-payment
```

- This just updates your remote-tracking branches (like origin/main), not your actual main branch.

</div>

---
level: 2
hideInToc: true
---

## Basic Git Remote Commands


<div style="margin:15px">

**6. Pull from a Remote**

Downloads new data AND integrates it into your current local branch. It's essentially git fetch followed by git merge.

```bash
git pull origin main
```

**Sample Output:**

```bash
From https://github.com/yourusername/yourrepo
 * branch            main       -> FETCH_HEAD
Updating a1b2c3d..d4e5f6g
Fast-forward
 file2.txt | 1 +
 1 file changed, 1 insertion(+)
```

- Always git pull before starting new work to get the latest changes!

</div>

---
level: 2
hideInToc: true
---

## Basic Git Remote Commands


<div style="margin:15px">

**7. Push to a Remote**

Uploads your local commits to a remote repository.

```bash
git push origin main
```

**Sample Output:**

```bash
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 369 bytes | 369.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0
To https://github.com/yourusername/yourrepo.git
   a1b2c3d..d4e5f6g  main -> main
```

- You need to be on the branch you want to push, and specify the remote and branch.

</div>

---
layout: default
level: 2
hideInToc: true
---

## Basic Git Remote Commands  

<div style="margin:15px">

**🧠 Quick Summary**  
- `git remote` → list remotes  
- `git remote -v` → list remotes with URLs  
- `git remote add name url` → add new remote  
- `git remote remove name` → remove remote connection  
- `git fetch name` → download updates, don't merge  
- `git pull name branch` → download + merge updates  
- `git push name branch` → upload local commits  

</div>


---
layout: full
---


## What is Gitignore?

<div style="margin-left:15px; margin-top:10px">

The <code>.gitignore</code> file is a crucial part of any Git repository. It tells Git which files or directories to ignore when committing changes, preventing unwanted files (like build artifacts, temporary files, or sensitive information) from being tracked and committed to your repository. This keeps your repository clean and focused on essential project files.

</div>

<img src="https://media2.dev.to/dynamic/image/width=1280,height=720,fit=cover,gravity=auto,format=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fe2t3cfhkql3w6js9jbn8.png" height=500 width=600 style="margin:15px" />

---
layout: default
level: 2
hideInToc: true
---

## Basic Gitignore Configuration

<div style="margin:15px">

**1. Create a <code>.gitignore</code> file**.
This file should be placed in the root directory of your Git repository. You can create it using your text editor or the command line.

```bash
touch .gitignore
```

**Sample Output:**

After creation, your project structure might look like this:
```bash
my-project/
├── .git/
├── .gitignore
├── src/
├── package.json
└── README.md
```

- The <code>.gitignore</code> file itself **should** be committed to your repository.

</div>

---
layout: default
level: 2
hideInToc: true
---

## Basic Gitignore Configuration

<div style="margin:15px">

**2. Ignoring specific files**
Add the exact file name to <code>.gitignore</code> to prevent it from being tracked.

**Sample Output:**
```
# .gitignore
.env
```

If you have <code>.env</code> in your project, Git will ignore it.
</div>


<div style="margin:15px">


**3. Ignoring files by extension**
Use an asterisk (<code>*</code>) as a wildcard to ignore all files with a certain extension.

**Sample Output:**
```
# .gitignore
*.log
*.tmp
```

This will ignore all <code>.log</code> files (like <code>error.log</code>, <code>debug.log</code>) and <code>.tmp</code> files (like <code>tempdata.tmp</code>).

</div>

---
layout: default
level: 2
hideInToc: true
---

## Basic Gitignore Configuration

<div style="margin:15px">

**4. Ignoring directories**
Add the directory name followed by a slash (<code>/</code>) to ignore an entire directory and its contents.

```
# .gitignore
node_modules/
build/
```

✅ Example:

This is super common for project dependencies (<code>node_modules</code>) or compiled output (<code>build</code>). Git will ignore everything inside these folders.

</div>

---
layout: default
level: 2
hideInToc: true
---

## Basic Gitignore Configuration

<div style="margin:15px">

**5. Ignoring all files in a directory except specific ones**
Use a combination of <code>*</code> and exclamation mark (<code>!</code>) to ignore everything in a directory, but re-include specific files.

```
# .gitignore
/logs/*
!/logs/.gitkeep
```

✅ Example:

This will ignore all files within the <code>logs</code> directory, but explicitly track a file named <code>.gitkeep</code> inside <code>logs</code> (often used to keep an empty directory in Git).

</div>

---
layout: default
level: 2
hideInToc: true
---

## Basic Gitignore Configuration


<div style="margin:15px">

**6. Ignoring patterns anywhere in the project**
If you just list a file or directory name without a leading slash, Git will ignore it anywhere in the repository.

```
# .gitignore
.DS_Store
Thumbs.db
```

✅ Example:

This is useful for OS-specific junk files (like macOS <code>.DS_Store</code> or Windows <code>Thumbs.db</code>) that might appear in various subdirectories.

</div>

---
layout: default
level: 2
hideInToc: true
---


<div style="margin:15px">

**🧠 Quick Summary**
- <code>.gitignore</code> → create ignore file
- <code>filename.txt</code> → ignore specific file
- <code>*.ext</code> → ignore files by extension
- <code>directory/</code> → ignore entire directory
- <code>file_anywhere</code> → ignore file pattern anywhere


</div>

---
layout: image-right
image: https://www.tatvasoft.com/blog/wp-content/uploads/2018/10/Importance-of-Code-Quality-2.jpg
---


# Code Quality & Formatting Tools



<div style="margin-left:15px; margin-top:10px">

## What Is Code Quality?


code quality refers to the robustness and reliability of your software’s codebase. A high-quality codebase is not only functional but also easy to read, maintain, and adapt. Conversely, low-quality code leads to bugs, higher maintenance costs, and scaling challenges.

</div>

---
layout: image-left
image: https://www.simform.com/wp-content/uploads/2019/12/characteristics-of-good-quality-code.png
hideInToc: true
---

### Key Characteristics of High-Quality Code:

<div style="margin-left:15px; margin-top:10px">


- **Readability:** Developers can easily read and understand the code, making collaboration simpler.
- **Maintainability:** Changes and updates can be implemented without breaking existing features.
- **Efficiency:** Code executes quickly and uses resources optimally.
- **Testability:** It’s easy to write and execute tests to ensure the code behaves as expected.
- **Security:** The code is robust against vulnerabilities and attacks.

</div>


---
layout: full
level: 2
---

## **Black (Code Formatter)**

**What is it?**

Black is an uncompromising Python code formatter. Think of it like a strict editor for your code that ensures everything looks the same, every time. When you run Black on your code, it automatically reformats it to conform to PEP 8 (Python Enhancement Proposal 8) and other stylistic conventions, making your code easier to read and maintain across different projects and developers.

<img src="https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fi%2Flgkkpq50djrdkd4husxu.png" height=500 width=600 style="margin:15px" />

---
layout: full
hideInToc: true
---


### Auto-formatting Philosophy

- Opinionated, Not Configurable

  - Black has very few configuration options – it dictates the style.
  - This removes the need for teams to decide on formatting rules.


- PEP 8 Compliance & Beyond

  - Strictly adheres to PEP 8 (Python's official style guide).
  - Goes a step further to enhance readability in specific cases.


- Deterministic Output

  - Given the same input, Black always produces the same formatted output.
  - Super important for consistency in CI/CD pipelines.


- Clean Diff Integration

  - Designed to produce minimal and meaningful changes in git diff outputs.


---
layout: two-cols
layoutClass: gap-10
hideInToc: true
---


### Usage in Scripts

**Installation:**

```bash
pip install black
```

**Formatting a File:**

```bash
black your_script.py
```

**Formatting a Directory:**

```bash
black your_project_folder/
```

::right::

**Checking for Changes (No Apply):**

```bash
black --check your_script.py
```

  - Useful in CI/CD to verify formatting.


**Show Differences (No Apply):**

```bash
black --diff your_script.py
```
  - Preview changes before committing.

---
layout: full
hideInToc: true
---

## Integration with IDEs

Seamless Workflow: Format code automatically as you save or type!

**VS Code:**

  -  Install Python extension.
  -  Set python.formatting.provider: "black".
  -  Enable editor.formatOnSave: true for instant formatting.

**PyCharm:**

  -  Built-in support for external formatters.
  -  Configure Black in project settings or use as a file watcher.

**Other Editors (Sublime, Vim, Emacs):**

  -  Plugins and configurations available to integrate Black.

Benefit: Keep your code pristine without even thinking about it!


---
layout: full
level: 2
---

## **Flake8 (Linting Tool)**

**What is it?**

  * [Flake8][1] is a popular, extensible Python linting tool that performs static code analysis to check for style violations, potential bugs, and code complexity. It acts as a single wrapper around three other established tools, providing a comprehensive approach to code quality with a single command. 
* **Combines Multiple Tools**

  * PyFlakes → logical errors
  * pycodestyle → style checks (PEP 8)
  * McCabe → code complexity
* **Purpose:** Improve code quality and consistency.
* **Output:** Displays warnings & errors with line numbers for easy debugging. 

[1]:  https://flake8.pycqa.org/en/latest/ "flake8 docs"

---
layout: full
hideInToc: true
---

## **What is Linting?**

  Linting is the process of using a static code analysis tool (a "linter") to automatically check source code for programmatic errors, potential bugs, security vulnerabilities, and style violations without actually running the code. Flake8 is a popular, extensible Python-specific linter that combines several other tools to provide a comprehensive analysis.

* **Acts Like a Code Reviewer**

  * Similar to spell-check in a text editor.
* **Why It Matters:**

  * Finds issues before runtime
  * Improves readability and maintainability
  * Saves debugging time ([Educative][2])


---
layout: two-cols
hideInToc: true
---

## **Common Linting Errors (Flake8)**

**Syntax / Structural Errors**
  * `E999` → Indentation error
**Style Violations (PEP 8)**
  * `E501` → Line too long
  * `E302` → Missing blank lines


**Whitespace Issues**
  * `W291` → Trailing whitespace


**Logical Issues**
  * `F401` → Unused import
  * Undefined variables

::right::

**Indentation Problems**
  * Mixed tabs & spaces (`E101`)

<div style="margin:12px; border: 1px solid grey; padding:12px">

Flake8 classifies:
* **E** → Errors
* **W** → Warnings
* **F** → Logical issues

</div>

---
layout: two-cols
layoutClass: gap-10
hideInToc: true
---

## **Configuration via `.flake8`**

**Custom Configuration File**

  * Create a `.flake8` file in your project

```ini
[flake8]
max-line-length = 100
ignore = F401
exclude = __pycache__, .git
```


**What You Can Configure:**

  * Ignore specific error codes
  * Set max line length
  * Exclude files/folders
  * Control complexity (`max-complexity`)

::right::

**Other Supported Config Files:**

  * `setup.cfg`
  * `tox.ini`

**Benefit:**

  * Apply consistent rules across the entire project
  * Avoid repeating command-line options 


---
layout: full
level: 2
---

## **Ruff (Modern Linter & Formatter)**

**What is it?**

Ruff is an extremely fast, Rust-based, all-in-one linter and formatter for Python, designed as a drop-in replacement for tools like Flake8, Black, and isort. It boosts productivity by analyzing and formatting code 10–100x faster than traditional tools and supports hundreds of rules to enforce code quality, style, and best practices.

**Key Features of Ruff:**

  -  **Blazing Fast:** Written in Rust, Ruff offers near-instantaneous feedback.
  -  **All-in-One Tool:** Replaces multiple, separate linting (Flake8, pyupgrade) and formatting (Black, isort) tools.
  -  **Comprehensive Rules:** Features over 800 built-in, customizable rules for code quality and style.
  -  **Effortless Adoption:** Offers direct integration with VS Code, pre-commit hooks, and GitHub Actions.
  -  **Auto-Fixing:** Automatically corrects common linting errors with the ruff check --fix command.

---
layout: full
level: 2
hideInToc: true
---

## **Black vs Flake8 vs Ruff (Comparison Table)**

| Feature                            | **Black**                     | **Flake8**                          | **Ruff**                                                 |
| ---------------------------------- | ----------------------------- | ----------------------------------- | -------------------------------------------------------- |
| **Type**                           | Code Formatter                | Linter                              | Linter + Formatter                                       |
| **Purpose**                        | Formats code automatically    | Detects errors, bugs, style issues  | Combines linting + formatting                            |
| **Language**                       | Python                        | Python                              | Rust                                                     |
| **Speed**                          | Fast                          | Moderate (slower on large projects) | Extremely fast (10–100× faster)   |
| **Configuration**                  | Minimal (opinionated)         | Configurable via `.flake8`          | Config via `pyproject.toml`                              |
| **Functionality**                  | Only formatting               | Only linting                        | All-in-one (Flake8 + Black + more) |


---
layout: full
level: 2
hideInToc: true
---

## **Black vs Flake8 vs Ruff (Comparison Table)**

| Feature                            | **Black**                     | **Flake8**                          | **Ruff**                                                 |
| ---------------------------------- | ----------------------------- | ----------------------------------- | -------------------------------------------------------- |
| **Auto Fix**                       | Yes (formats code)            | No (manual fixes needed)            | Yes (`--fix` option) ([X-CMD][2])                        |
| **Rules Support**                  | Style only                    | PEP 8 + plugins                     | Supports Flake8 rules + extras       |
| **Performance in Large Codebases** | Good                          | Slower                              | Excellent (parallel processing)        |
| **Ease of Use**                    | Very simple                   | Requires setup/plugins              | Simple (single tool replaces many)                       |
| **Best Use Case**                  | Enforce consistent formatting | Detect bugs & code issues           | Modern projects needing speed + simplicity               |


---
layout: two-cols
layoutClass: gap-10
level: 2
hideInToc: true
---


## **Configuration (`pyproject.toml`)**

**Centralized Configuration**

  * Uses `pyproject.toml` (modern Python standard)

```toml
[tool.ruff]
line-length = 88
select = ["E", "F"]
ignore = ["E501"]

[tool.ruff.lint]
fixable = ["ALL"]
```

:: right ::

**What You Can Configure:**
  * Line length
  * Rules to enable/disable
  * Auto-fix behavior
  * File exclusions


**Benefits**

  * Single config file for entire project
  * Cleaner than multiple configs (`.flake8`, `black`, etc.) ([py-launch-blueprint.readthedocs.io][4])

---
layout: image-left
image: https://www.scylladb.com/wp-content/uploads/data-ingestion-diagram.png
---


# Data Ingestion

<div>
Data ingestion is the process of collecting and importing data files from various sources into a database for storage, processing and analysis. The goal of data ingestion is to clean and store data in an accessible and consistent central repository to prepare it for use within the organization.
</div>

---
layout: two-cols
layoutClass: gap-10
hideInToc: true
---

# Why is data ingestion important?

<div style="font-size:14px">
Data ingestion is the first step in processing data, where raw information from various sources is collected and brought into a system for analysis and storage. A well‑designed ingestion process ensures the data is accurate and reliable before it reaches analytics tools, enabling effective insights and decision‑making.
</div>

**Importance of Data Ingestion**

**1. Flexibility in a Dynamic Data Environment**
* Handles data from multiple sources with different formats
* Adapts to new and growing data sources
* Supports increasing data volume and speed
* Keeps data architecture scalable and flexible ([IBM][1])

:: right ::

**2. Enables Powerful Analytics**

* Collects and prepares large datasets for analysis
* Helps solve business problems using data insights
* Converts data into actionable decisions ([IBM][1])

**3. Improves Data Quality**

* Performs data cleaning (removes errors and irrelevant data)
* Ensures consistency through standardization
* Reduces redundancy via normalization
* Adds value with enrichment (extra context to data) ([IBM][1])

[1]: https://www.ibm.com/think/topics/data-ingestion?utm_source=chatgpt.com "What is Data Ingestion? | IBM"


---
layout: two-cols
layoutClass: gap-10
level: 2
hideInToc: true
---

## **Batch Ingestion**

**Definition:** Data is collected over a period of time and then transferred/processed all at once. 

**How it works:** Runs on schedules (hourly, daily, weekly). Data accumulates in batches and is processed as a group.

**Key Features**
  * Works with *bounded datasets* (specific time windows).
  * Easier to validate, retry, and backfill. 
  * Lower operational complexity. 

:: right ::

**Drawbacks**
  * Data freshness is limited (data might be stale). 
  * Possible processing spikes during batch runs. 

**Use Cases**

  * Nightly warehouse loads
  * Reporting and accounting
  * Historical analysis

---
layout: two-cols
layoutClass: gap-10
level: 2
hideInToc: true
---
## **Real‑Time (Streaming) Ingestion**

**Definition:** Data is moved continuously from source to destination as it arrives. 

**How it works:** Uses streaming systems/logs where each event is processed as it occurs.

**Key Features**

  * Data is almost always *fresh* or updated within seconds of generation. 
  * Enables event‑driven workflows. 
  * Can maintain *stateful* computations (like running totals).

:: right ::

**Drawbacks**

  * Higher operational complexity
  * Requires always‑on infrastructure
  * Harder to guarantee strict ordering and exactly‑once processing

**Use Cases**

  * Monitoring systems (security, performance)
  * Customer behaviour tracking
  * Personalisation and recommendation engines

---
layout: full
hideInToc: true
---

### **Key Differences At a Glance**

<br/>

| Feature                | Batch                  | Real‑Time               |
| ---------------------- | ---------------------- | ----------------------- |
| Freshness              | Periodic               | Nearly continuous       |
| Processing model       | Bounded, scheduled     | Unbounded, event‑driven |
| Operational complexity | Lower                  | Higher                  |
| Failure handling       | Specific window re‑run | Replay streams          |
| Use cases              | Reporting/analytics    | Live dashboards, alerts |


---
layout: full
hideInToc: true
---

## Types of Data

![image](https://cdn.prod.website-files.com/605c9e03d6553a5d82976ce2/665e09207ffe7aafc0d35f39_semi-structured-data.png)


---
layout: full
hideInToc: true
---

## **Structured Data**

Structured data refers to data that is **organized in a predefined format or schema**, making it easy to store, process, and analyze. It is typically arranged in **rows and columns**, where each field has a specific data type (e.g., text, number, date).

This type of data is commonly stored in **relational database management systems (RDBMS)** and spreadsheets, where relationships between data elements are clearly defined.

### **Examples of Structured Data**

| Customer_ID | Name       | Age | City       | Join_Date  |
| ----------- | ---------- | --- | ---------- | ---------- |
| 101         | Ravi Kumar | 30  | Chennai    | 2023-01-15 |
| 102         | Priya Devi | 27  | Coimbatore | 2023-03-22 |

---
layout: two-cols
layoutClass: gap-10
hideInToc: true
---

### **Key Components of Structured Data**

1. **Schema**

   * A schema defines the structure of the data.
   * Includes table names, column names, data types, and relationships.
   * Example: A customer table with columns like `Customer_ID`, `Name`, `Email`, `Phone`.

2. **Tables (Relations)**

   * Data is stored in tables consisting of rows (records) and columns (fields).
   * Each row represents a unique record.
   * Each column represents a specific attribute.

:: right ::

3. **Data Types**

   * Each column has a predefined data type:

     * Integer (e.g., age, quantity)
     * Float/Decimal (e.g., price)
     * String/Text (e.g., name)
     * Date/Time (e.g., transaction date)

4. **Relationships**

   * Tables can be linked using keys:

     * **Primary Key:** Unique identifier for a record
     * **Foreign Key:** Links one table to another


---
layout: full
hideInToc: true
---

### **Characteristics of Structured Data**

* **Predefined Format:** Data follows a fixed schema.

* **Highly Organized:** Stored in tabular format.

* **Easy to Query:** Can be accessed using SQL (Structured Query Language).

* **Data Integrity:** Constraints ensure accuracy (e.g., NOT NULL, UNIQUE).

* **Consistency:** Same format across records.

* **Efficient Storage:** Optimized for structured storage systems.

* **Scalability (Vertical):** Scales well in traditional database systems.

---
layout: two-cols
layoutClass: gap-10
hideInToc: true
---

### **Advantages of Structured Data**

1. **Ease of Analysis**

   * Supports advanced analytics and reporting tools.
   * Compatible with Business Intelligence (BI) tools like dashboards.

2. **Fast Query Performance**

   * Indexed data allows quick searching and retrieval.

3. **Data Integrity and Accuracy**

   * Validation rules reduce errors and inconsistencies.

:: right ::

4. **Standardization**

   * Uniform structure makes integration across systems easier.

5. **Strong Security**

   * Access control and permissions can be applied at table/column level.


---
layout: full
hideInToc: true
---

### **Disadvantages of Structured Data**

* **Limited Flexibility**

  * Difficult to handle changing data requirements.

* **Schema Dependency**

  * Any change in schema may require redesign or migration.

* **Not Suitable for Complex Data**

  * Cannot efficiently store unstructured data like images, videos, or text documents.

---
layout: full
hideInToc: true
---

### **Common Storage Systems**

* Relational Databases:

  * MySQL
  * PostgreSQL
  * Oracle Database
  * Microsoft SQL Server

* Spreadsheet Tools:

  * Microsoft Excel
  * Google Sheets


---
layout: full
hideInToc: true
---


## **Semi-Structured Data**

Semi-structured data is a type of data that **does not follow a strict tabular schema like structured data**, but still contains **organizational elements such as tags, keys, or metadata** that make it easier to interpret and process.

Unlike structured data, it **does not require a predefined schema before storing data**, allowing more flexibility while still maintaining some level of organization.

### **Examples of Semi-Structured Data**

```json
{
  "customer_id": 101,
  "name": "Priya",
  "orders": [
    { "product": "Laptop", "price": 55000 },
    { "product": "Mouse", "price": 500 }
  ]
}
```

---
layout: two-cols
layoutClass: gap-10
hideInToc: true
---

### **Key Components of Semi-Structured Data**

1. **Tags or Keys**

   * Data elements are labeled using identifiers.
   * Example:

     ```json
     {
       "name": "Ravi",
       "age": 30
     }
     ```

2. **Hierarchical Structure**

   * Data is often nested (parent-child relationships).
   * Common in formats like JSON and XML.

:: right ::

3. **Metadata**

   * Provides information about the data itself.
   * Helps in understanding structure and meaning.

4. **Irregular Fields**

   * Not all records need to have the same fields.
   * Example: One record may have “phone”, another may not.



---
layout: full
hideInToc: true
---

### **Characteristics of Semi-Structured Data**

* **No Fixed Schema**

  * Structure can vary between records.

* **Self-Describing**

  * Uses tags, keys, or attributes to define data.

* **Flexible and Extensible**

  * New fields can be added without redesigning the system.

* **Hierarchical/Nested**

  * Supports complex relationships and nested structures.

* **Schema-on-Read**

  * Structure is interpreted when the data is read, not when stored.

---
layout: two-cols
layoutClass: gap-10
hideInToc: true
---

### **Advantages of Semi-Structured Data**

1. **High Flexibility**

   * Easily adapts to changing data requirements.

2. **Scalability**

   * Works well with large and evolving datasets.

3. **Better Than Unstructured Data for Analysis**

   * Easier to parse and query due to embedded structure.

:: right ::

4. **Efficient Data Exchange**

   * Widely used in APIs and web services.

5. **Supports Complex Data Models**

   * Ideal for representing hierarchical relationships.


---
layout: full
hideInToc: true
---

### **Disadvantages of Semi-Structured Data**

* **Complex Querying**

  * Requires specialized query languages (e.g., XPath, JSONPath).

* **Less Efficient Than Structured Data**

  * Slower for heavy analytical queries.

* **Data Inconsistency**

  * Missing or varying fields across records.

* **Storage Overhead**

  * Tags and metadata increase data size.

---
layout: full
hideInToc: true
---

### **Common Storage Systems**

* **NoSQL Databases**

  * MongoDB (JSON-like documents)
  * CouchDB
  * Firebase

* **Big Data Systems**

  * Hadoop
  * Apache Spark

* **File Formats**

  * JSON, XML, YAML, Avro, Parquet

---
layout: full
hideInToc: true
---


## **Unstructured Data**

Unstructured data refers to data that **does not follow any predefined format, model, or schema**, making it difficult to store, process, and analyze using traditional database systems.

Unlike structured and semi-structured data, it lacks a clear organization (such as rows and columns), and therefore requires **advanced processing techniques like Natural Language Processing (NLP), Machine Learning (ML), and Artificial Intelligence (AI)** to extract meaningful insights.

### **Examples of Unstructured Data**


<div class="grid grid-cols-2 gap-4">
  <div>
    
  * **Text Data**

    * Emails
    * PDFs
    * Word documents
    * Chat messages

  </div>
  <div>
   
  * **Media Files**

    * Images (JPEG, PNG)
    * Videos (MP4, AVI)
    * Audio files (MP3, WAV)

  </div>
</div>


---
layout: two-cols
layoutClass: gap-10
hideInToc: true
---

### **Key Components of Unstructured Data**

1. **Raw Content**

   * Data exists in its original, natural format.
   * Example: text in documents, images, videos.

2. **Lack of Metadata (or Limited Metadata)**

   * May not include clear labels or structure.
   * Requires additional tagging or annotation.

:: right ::

3. **Varied Formats**

   * Data comes in multiple formats and types.
   * Example: text, audio, video, images.

4. **Context-Dependent Meaning**

   * Interpretation depends on context and analysis techniques.

---
layout: two-cols
layoutClass: gap-10
hideInToc: true
---

### **Characteristics of Unstructured Data**

* **No Predefined Structure**

  * Data is not organized in tables or schemas.

* **Highly Diverse**

  * Exists in many formats and forms.

* **Difficult to Search and Query**

  * Cannot be easily queried using traditional SQL.

* **Requires Processing**

  * Needs transformation into structured or semi-structured form for analysis.

:: right ::

* **Large Volume**

  * Makes up the majority of real-world data (estimated 80–90%).

* **Contextual and Complex**

  * Meaning often depends on interpretation.

---
layout: full
hideInToc: true
---

### **Advantages of Unstructured Data**

1. **Rich Information Content**

   * Contains detailed and nuanced insights (e.g., customer opinions).

2. **Real-World Representation**

   * Captures natural human communication and behavior.

3. **Flexibility**

   * No restrictions on format or structure.

4. **Supports Advanced Analytics**

   * Enables AI-driven insights such as sentiment analysis and image recognition.


---
layout: full
hideInToc: true
---

### **Disadvantages of Unstructured Data**

* **Difficult to Analyze**

  * Requires complex tools and techniques.

* **Time-Consuming Processing**

  * Data cleaning and preparation are intensive.

* **Storage Challenges**

  * Requires large storage systems (data lakes).

* **Inconsistency**

  * Lack of uniformity across data sources.

---
layout: full
hideInToc: true
---

### **Technologies Used to Process Unstructured Data**

1. **Natural Language Processing (NLP)**

   * Extracts meaning from text (e.g., sentiment analysis).

2. **Machine Learning (ML)**

   * Identifies patterns and predictions.

3. **Computer Vision**

   * Processes and analyzes images and videos.

4. **Big Data Platforms**

   * Hadoop
   * Apache Spark

5. **Search and Indexing Tools**

   * Elasticsearch

---
layout: full
---


# Introduction to Pandas

<div>

Pandas is a Python library used for data manipulation and analysis. Pandas provides a convenient way to analyze and clean data.

The Pandas library introduces two new data structures to Python - Series and DataFrame, both of which are built on top of NumPy.

**What is Pandas Used for?**

Pandas is a powerful library generally used for:

  -  Data Cleaning
  -  Data Transformation
  -  Data Analysis
  -  Machine Learning
  -  Data Visualization


</div>

---
layout: full
level: 2
hideInToc: true
---


## Why Use Pandas?

<div >

Some of the reasons why we should use Pandas are as follows:

#### **1. Handle Large Data Efficiently**

Pandas is designed for handling large datasets. It provides powerful tools that simplify tasks like data filtering, transforming, and merging.

It also provides built-in functions to work with formats like **CSV, JSON, TXT, Excel, and SQL databases**.

#### **2. Tabular Data Representation**

Pandas DataFrames, the primary data structure of Pandas, handle data in tabular format. This allows easy indexing, selecting, replacing, and slicing of data.

#### **3. Data Cleaning and Preprocessing**

Data cleaning and preprocessing are essential steps in the data analysis pipeline, and Pandas provides powerful tools to facilitate these tasks. It has methods for handling missing values, removing duplicates, handling outliers, data normalization, etc.

</div>

---
layout: full
level: 2
hideInToc: true
---


## Why Use Pandas?

<div >

Some of the reasons why we should use Pandas are as follows:

#### **4. Time Series Functionality**

Pandas contains an extensive set of tools for working with dates, times, and time-indexed data as it was initially developed for financial modeling.

#### **5. Free and Open-Source**

Pandas follows the same principles as Python, allowing you to use and distribute Pandas for free, even for commercial use.

</div>

---
layout: full
level: 2
hideInToc: true
---


# Install Pandas

To install **Pandas**, you first need a working Python environment along with a package manager such as **pip** or **uv**. Below is a more detailed and practical guide, including modern installation methods.

## 1. Install Python and Pip

Before installing Pandas, make sure you have:

* Python installed
* pip (usually included with Python)

### Check installation:

```bash
python --version
pip --version
```

If these commands work, you’re ready.

---
layout: full
level: 2
hideInToc: true
---

## 2. Basic Installation using Pip

Open your terminal or command prompt and run the following command:

```bash
pip install pandas
```

This command will:

* Download the latest version of Pandas
* Install it along with its required dependencies (such as NumPy)
* Make it available for use in your Python environment

After installation, you can confirm that Pandas is installed correctly by checking its version:

```bash
python -c "import pandas as pd; print(pd.__version__)"
```

If Pandas is installed successfully, this command will display the installed version number, such as:

```
2.2.2
```

---
layout: full
level: 2
hideInToc: true
---


## 3. Recommended: Use a Virtual Environment

It is best practice to avoid installing packages globally.

### Create and activate a virtual environment:

```bash
python -m venv venv
```

Activate it:

* Windows:

```bash
venv\Scripts\activate
```

* macOS/Linux:

```bash
source venv/bin/activate
```

Then install Pandas:

```bash
pip install pandas
```

---
layout: full
level: 2
hideInToc: true
---

## 4. Modern Alternative: Install using UV

A faster modern Python package manager is uv.

### Install uv (if not installed):

```bash
pip install uv
```

### Create environment and install Pandas:

Using uv pip:

```bash
uv pip install pandas
```

Or create a project-style setup:

```bash
uv init my_project
cd my_project
uv add pandas
```

---
layout: full
level: 2
hideInToc: true
---


### Import Pandas in Python

We can import Pandas in Python using the import statement.

```py
import pandas as pd
```

* The code above imports the pandas library into our program with the alias <code>pd</code>.
* After this import statement, we can use Pandas functions and objects by calling them with pd.
* For example, you can use Pandas dataframe in your program using <code>pd.DataFrame()</code>.


---
layout: full
level: 2
hideInToc: true
---

## **Reading Data with pandas**

The pandas library provides easy and efficient ways to read data from different file formats into DataFrames for analysis. It supports formats like CSV, Excel, JSON, and more, making it a fundamental tool for data preprocessing and exploration in Python.

<div class="grid grid-cols-2 gap-6">
  <div>

**CSV Files**

CSV files store tabular data in plain text format, where each line represents a row and values are separated by a delimiter (usually a comma).

Example CSV:

```csv
Name,Age,City
Alice,25,New York
Bob,30,London
```

  </div>
  <div>
   
  **read_csv() Basics**

  The `read_csv()` function is used to load CSV data into a pandas DataFrame.

  Syntax:

  ```python
  import pandas as pd

  df = pd.read_csv("file.csv")
  ```

  </div>
</div>



---
layout: full
level: 2
hideInToc: true
---

## **Key Parameters**

### **1. delimiter**

The ```delimiter``` parameter specifies the character used to separate values in a CSV file. While commas are the default, some files may use other characters like semicolons, tabs, or pipes, and this parameter ensures the data is correctly split into columns.


#### Example:

```python
df = pd.read_csv("file.csv", delimiter=";")
```

Use this when your file uses something other than commas (e.g.,<code> ; </code> , ```|```, ```\t```).

---
layout: full
level: 2
hideInToc: true
---

## **Key Parameters**

### **2. encoding**

The ```encoding``` parameter defines how text data is encoded in the file. Since CSV files can contain special characters, specifying the correct encoding (such as UTF-8 or Latin-1) helps prevent errors and ensures that the data is read correctly.

#### Example:

```python
df = pd.read_csv("file.csv", encoding="utf-8")
```

#### Common encodings:

* `utf-8` (default, most common)
* `latin1` (for special characters)
* `cp1252` (Windows encoding)

Use this parameter when you encounter encoding errors like:

---
layout: full
level: 2
hideInToc: true
---

## **Key Parameters**

### **3. header**

The ```header``` parameter determines which row in the file should be treated as the column names. By default, pandas uses the first row, but this can be changed or disabled if the file does not include headers.

#### Examples:

```python
df = pd.read_csv("file.csv", header=0)  # first row as header
df = pd.read_csv("file.csv", header=None)  # no header
```

If no header exists:

```python
df = pd.read_csv("file.csv", header=None)
df.columns = ["Name", "Age", "City"]
```


---
layout: full
level: 2
hideInToc: true
---

## **Key Parameters**

### **4. dtype**

The ```dtype``` parameter allows users to explicitly set the data type for one or more columns while reading the file. This helps improve performance, reduce memory usage, and avoid incorrect automatic type detection by pandas.

#### Example:

```python
df = pd.read_csv("file.csv", dtype={"Age": int})
```

#### Benefits:

* Improves performance
* Prevents incorrect type inference
* Ensures consistency

---
layout: two-cols
layoutClass: gap-10
level: 2
hideInToc: true
---

# **Handling Large CSV**

When working with very large CSV files that don’t fit into memory, use the `chunksize` parameter.

### Example:

```py 
chunk_iter = pd.read_csv("large_file.csv", chunksize=1000)

for chunk in chunk_iter:
    print(chunk.head())
```

### How it works:

* Reads the file in **small chunks (DataFrames)**
* Each chunk contains a specified number of rows
* Useful for:
  * Big data processing
  * Memory-efficient operations

:: right ::

### Example Use Case:

```py
total = 0
for chunk in pd.read_csv("large_file.csv", chunksize=1000):
    total += chunk["Sales"].sum()
print(total)
```

---
layout: full
level: 2
hideInToc: true
---

## **JSON Data**

**JSON (JavaScript Object Notation)** is a lightweight, text-based data format used to **store and exchange data between systems**. It is designed to be **easy for humans to read and write**, and **simple for machines to parse and generate**.

JSON is widely used in **web applications, APIs, and data storage**, especially for communication between a client (browser/mobile app) and a server.

#### **Key Features of JSON**

* **Key–Value Pairs:** Data is organized in simple key–value format for readability.
* **Nested Structures:** Supports objects and arrays for complex, hierarchical data.
* **Language-Independent:** Works across programming languages like Python, Java, and C#.
* **API-Friendly:** Lightweight and widely used in web services and RESTful APIs.
* **Flexible & Extensible:** Easy to add new fields or nested objects without breaking structure.

---
layout: full
level: 2
hideInToc: true
---

## **read_json function**

The ```read_json()``` function in the pandas library is used to read JSON-formatted data and convert it into a pandas DataFrame, which can then be easily analyzed, manipulated, and visualized. It supports both JSON files and JSON strings as input.

#### **Syntax**

```python
pandas.read_json(path_or_buf, orient=None)
```

#### **Parameters:**

  * `path_or_buf`: File path, URL, or JSON string
  * `orient`: Structure of JSON (e.g., 'records', 'columns', 'index')

<div class="grid grid-cols-2 gap-4">
  <div>

#### **Example:**

```py
import pandas as pd

df = pd.read_json("data.json")
print(df)
```

  </div>
  <div>
   

## **Reading JSON from a string:**

```python
import pandas as pd

json_data = '{"name": "John", "age": 25}'
df = pd.read_json(json_data, typ='series')
print(df)
```

  </div>
</div>

---
layout: full
level: 2
hideInToc: true
---

# **Nested JSON Handling**

## **What is Nested JSON?**

Nested JSON contains objects within objects or arrays within objects.

### **Example:**

```json
{
  "id": 1,
  "name": "Alice",
  "contact": {
    "email": "alice@example.com",
    "phone": "1234567890"
  }
}
```
    
**Challenges:**

* Data is not flat
* Difficult to directly convert into tabular format

---
layout: full
level: 2
hideInToc: true
---

## **Handling Nested JSON in Python:**
<br/>

#### **Method 1: Access manually**

```python
import json

data = json.loads(json_string)
email = data["contact"]["email"]
```

#### **Method 2: Convert using pandas**

```python
import pandas as pd

df = pd.read_json("nested.json")
```

* But this may not fully flatten nested fields.


---
layout: full
level: 2
hideInToc: true
---

# **Normalization**

<div>

Normalization in pandas is the process of converting complex, hierarchical JSON data structures into a flat, tabular format (a pandas DataFrame) using the pandas.json_normalize() function.

`json_normalize()` is used to convert **nested JSON into a flat table (DataFrame)**.

</div>

### **Syntax**

```python
pandas.json_normalize(data, record_path=None, meta=None)
```

### **Parameters:**

* `data`: JSON data (dict or list)
* `record_path`: Path to nested list
* `meta`: Fields to keep as metadata


---
layout: full
level: 2
hideInToc: true
---


## **Example 1: Simple Flattening**

```python
import pandas as pd

data = {
    "id": 1,
    "name": "Alice",
    "contact": {
        "email": "alice@example.com",
        "phone": "1234567890"
    }
}

df = pd.json_normalize(data)
print(df)
```

### **Output:**

```
    id   name contact.email     contact.phone
0   1  Alice alice@example.com 1234567890
```

---
layout: full
level: 2
hideInToc: true
---


## **Example 2: Nested List Handling**

```python
data = {
    "id": 1,
    "name": "Alice",
    "skills": [
        {"type": "Programming", "name": "Python"},
        {"type": "Database", "name": "SQL"}
    ]
}

df = pd.json_normalize(data, record_path="skills", meta=["id", "name"])
print(df)
```

### **Output:**

```
          type    name  id   name
0  Programming  Python   1  Alice
1     Database     SQL   1  Alice
```


---
layout: image-right
image: https://img.freepik.com/premium-vector/microsoft-excel-logo-spreadsheet-program-microsoft-office-365-logotype-microsoft-corporation-software-editorial_661108-17045.jpg
level: 2
hideInToc: true
---

# **Excel Files in pandas**

## **What are Excel Files?**

**Excel files** (commonly `.xlsx`, `.xls`) are widely used spreadsheet formats for storing structured data in rows and columns. They support **multiple sheets, formulas, formatting, and data types**, making them a common choice in business and data analysis workflows.

In Python, the **pandas** library provides powerful functions to read, process, and analyze Excel data efficiently.

---
layout: two-cols
layoutClass: gap-10
hideInToc: true
---

## **read_excel Function**

The `read_excel()` function in pandas is used to **load Excel files into a DataFrame** for further analysis and processing.

#### **Syntax**

```python
pandas.read_excel(io, sheet_name=0)
```

#### **Parameters:**

* `io`: File path, URL, or Excel file object
* `sheet_name`: Sheet to read (default = first sheet)

  * Can be sheet name (string) or index (int)

:: right ::

## **Basic Example**

```python
import pandas as pd

df = pd.read_excel("data.xlsx")
print(df)
```

- Reads the **first sheet by default**

--- 
hideInToc: true
level: 2
---

# **Multiple Sheets Handling**

## **What are Multiple Sheets?**

An Excel file can contain **multiple worksheets (tabs)**, each storing different datasets.

Example:

* Sheet1 → Sales Data
* Sheet2 → Customer Data
* Sheet3 → Inventory

## **Reading a Specific Sheet**

```python
df = pd.read_excel("data.xlsx", sheet_name="Sales")
print(df)
```

- Reads a sheet by its **name**

---
hideInToc: true
---

## **Reading a Specific Sheet**

```python
df = pd.read_excel("data.xlsx", sheet_name=1)
print(df)
```

- Reads a sheet by its **index (0-based)**

## **Selecting Columns**

```python
df = pd.read_excel("data.xlsx", usecols=["Name", "Revenue"])
print(df)
```

- Loads only required columns → improves performance

## **Handling Missing Values**

```python
df = pd.read_excel("data.xlsx", na_values=["NA", "Missing"])
```

- Converts specified values into `NaN`

---
hideInToc: true
level: 2
---

## **Reading All Sheets at Once**

```python
import pandas as pd

all_sheets = pd.read_excel("data.xlsx", sheet_name=None)

print(type(all_sheets))
```

- Output: **Dictionary of DataFrames**

## **Accessing Individual Sheets**

```python
sales_df = all_sheets["Sales"]
customers_df = all_sheets["Customers"]
```

- Each key = sheet name

- Each value = DataFrame


---
hideInToc: true
level: 2
---

## **Looping Through All Sheets**

```python
for sheet_name, df in all_sheets.items():
    print(f"Sheet: {sheet_name}")
    print(df.head())
```

- Useful for **batch processing multiple sheets**

## **Reading Multiple Selected Sheets**

```python
dfs = pd.read_excel("data.xlsx", sheet_name=["Sales", "Customers"])
```

- Returns dictionary with selected sheets only

## **Combining Multiple Sheets**

```python
combined_df = pd.concat(all_sheets.values(), ignore_index=True)
print(combined_df)
```

- Merges all sheets into a single DataFrame

---
hideInToc: true
level: 2
---

# **SQL Databases in Python (pandas)**

## **What are SQL Databases?**

**SQL (Structured Query Language) databases** are systems used to **store, manage, and retrieve structured data** using tables.These databases organize data into rows and columns, where each table represents a specific entity (such as users, products, or orders), and each row represents a record.

Popular SQL databases include:

* SQLite (lightweight, file-based)
* MySQL / PostgreSQL (server-based)
* SQL Server / Oracle (enterprise-level)

In Python, SQL databases are commonly accessed using:

* `sqlite3` (built-in, lightweight)
* `SQLAlchemy` (powerful ORM and connection manager)
* `pandas` (for data ingestion and analysis)


---
hideInToc: true
level: 2
---

# **Connecting to SQL Databases**

## **Using sqlite3 (Lightweight & Built-in)**

`sqlite3` is a built-in Python module used to connect to **SQLite databases**.It provides a simple and lightweight way to interact with databases without requiring any external installation or server setup, since SQLite is a file-based database system.

### **Example: Connection**

```python
import sqlite3

conn = sqlite3.connect("example.db")
```

- Creates or connects to a local `.db` file

- No server required

---
hideInToc: true
level: 2
---

## **Using SQLAlchemy**

**SQLAlchemy** provides a more flexible and scalable way to connect to databases. It acts as a powerful toolkit and Object Relational Mapper (ORM) that allows developers to interact with databases using Python classes and objects instead of writing raw SQL queries.

### **Example: Connection**

```python
from sqlalchemy import create_engine

engine = create_engine("sqlite:///example.db")
```

- Recommended for Production

- Supports multiple databases (MySQL, PostgreSQL, etc.)

- Better for large-scale and production systems


---
hideInToc: true
level: 2
---

# **read_sql Function**

<div>

The ```read_sql()``` function in pandas is used to **execute SQL queries and load the result directly into a DataFrame**.It provides a convenient bridge between relational databases and Python’s data analysis ecosystem, This eliminates the need to manually fetch and convert query results into a usable format.
</div>

#### **Syntax**

```python
pandas.read_sql(sql, con)
```

#### **Parameters:**

* `sql`: SQL query or table name
* `con`: Database connection or engine

---
hideInToc: true
level: 2
---

## **Example: Read Entire Table**

```python
import pandas as pd
import sqlite3

conn = sqlite3.connect("example.db")

df = pd.read_sql("SELECT * FROM employees", conn)
print(df)
```

- Loads full table into DataFrame

## **Using SQLAlchemy Engine**

```python
import pandas as pd
from sqlalchemy import create_engine

engine = create_engine("sqlite:///example.db")

df = pd.read_sql("SELECT * FROM employees", engine)
print(df)
```

- Cleaner and more scalable approach


---
hideInToc: true
level: 2
---

# **Query-Based Ingestion**

## **What is Query-Based Ingestion?**

Instead of loading entire tables, you can **retrieve only required data using SQL queries**.
This approach focuses on fetching a subset of data based on specific conditions, rather than importing all records from a database. It helps improve efficiency by reducing memory usage, network transfer, and processing time—especially when working with large datasets.


- Improves performance

- Reduces memory usage

- Enables filtering at source

---
hideInToc: true
level: 2
---

## **Example: Filtering Data**

```python
df = pd.read_sql("""
    SELECT name, salary
    FROM employees
    WHERE salary > 50000
""", conn)

print(df)
```

- Fetches only high-salary employees

## **Example: Aggregation Query**

```python
df = pd.read_sql("""
    SELECT department, AVG(salary) as avg_salary
    FROM employees
    GROUP BY department
""", conn)

print(df)
```

- Performs aggregation directly in SQL


---
hideInToc: true
level: 2
---

## **Example: Join Query**

```python
df = pd.read_sql("""
    SELECT e.name, d.department_name
    FROM employees e
    JOIN departments d
    ON e.dept_id = d.id
""", conn)

print(df)
```

- Combines multiple tables

---
hideInToc: true
level: 2
---

# **Best Practices**

* Prefer **SQL filtering over pandas filtering** for large datasets
* Use `SQLAlchemy` for **scalable and production-ready pipelines**
* Always close connections:

```python
conn.close()
```

* Use indexing in databases for **faster queries**
* Avoid `SELECT *` in large tables → fetch only required columns


---
hideInToc: true
level: 2
---

# **APIs (Application Programming Interfaces)**


## **What is an API?**

An API (Application Programming Interface) is a set of rules or protocols that enables software applications to communicate with each other to exchange data, features and functionality.

### How do APIs work?

It’s useful to think about API communication in terms of a request and response between a client and server. The application submitting the request is the client, and the server provides the response. The API is the bridge establishing the connection between them.

* Used when:

  * Data is **dynamic / real-time**
  * No direct file (CSV/Excel) available


---
hideInToc: true
level: 2
---

## **Fetching Data Using `requests`**

An API (Application Programming Interface) allows applications to communicate with external services and retrieve data. In Python, the `requests` library is commonly used to fetch data from APIs.


<div class="grid grid-cols-2 gap-6">
<div>

### **Example:**

```python
import requests

url = "https://jsonplaceholder.typicode.com/posts"

response = requests.get(url)

if response.status_code == 200:
    print("Data fetched successfully")
else:
    print("Failed to fetch data")
```

</div>
<div>

### **Steps to fetch data:**

1. Import the library
2. Define the API endpoint (URL)
3. Send a request using `requests.get()`
4. Check the response status

</div>
</div>

---
hideInToc: true
level: 2
---

## **Converting API Response to DataFrame**

API responses are usually in JSON format. To analyze this data, we convert it into a Pandas DataFrame.

<div class="grid grid-cols-2 gap-6">
<div>

### **Steps:**

1. Convert response to JSON using `.json()`
2. Pass data into `pandas.DataFrame()`

### **Example:**

```python
import pandas as pd
import requests

url = "https://jsonplaceholder.typicode.com/posts"
response = requests.get(url)

data = response.json()

df = pd.DataFrame(data)

print(df.head())
```

</div>
<div>

### **For Nested JSON:**

If the data is deeply structured, use:

```python
df = pd.json_normalize(data)
```

### **Benefits of DataFrame:**

* Easy data manipulation
* Filtering and grouping
* Data cleaning and analysis

</div>
</div>

---
hideInToc: true
level: 2
---

## **Handling Pagination**

Some APIs return large datasets in multiple pages instead of a single response. This is called pagination. It helps improve performance, reduce server load, and make data transfer more efficient by sending smaller chunks of data that clients can request sequentially, often using parameters like page number, limit, cursor, or offset to navigate through the dataset.

### **Why Pagination is Needed:**

* Avoids large data overload
* Improves performance
* Reduces server load

---
hideInToc: true
level: 2
---

### **Method 1: Page Number-Based Pagination**

```python
import requests
import pandas as pd

url = "https://api.example.com/data"

all_data = []
page = 1

while True:
    response = requests.get(url, params={"page": page})
    data = response.json()

    if not data:  # Stop when no more data
        break

    all_data.extend(data)
    page += 1

df = pd.DataFrame(all_data)
print(df.head())
```


---
hideInToc: true
level: 2
---

### **Method 2: Limit & Offset Pagination**

```python
import requests
import pandas as pd

limit = 10
offset = 0
all_data = []

while True:
    response = requests.get(url, params={"limit": limit, "offset": offset})
    data = response.json()

    if not data:
        break

    all_data.extend(data)
    offset += limit

df = pd.DataFrame(all_data)
```

---
transition: fade
---

# **Introduction to Polars**

### **What is Polars?**

**Polars** is a fast, modern DataFrame library designed for high-performance data processing in Python. It is built using **Rust**, which makes it significantly faster and more memory-efficient than traditional tools.

### **Key Features:**

* **Blazing Fast** – Uses multi-threading by default
* **Memory Efficient** – Optimized for large datasets
* **Lazy Execution** – Executes queries only when needed
* **Columnar Processing** – Based on Apache Arrow format
* **Easy Integration** – Works well with Python ecosystem

---
transition: fade
---

## **Pandas vs Polars Comparison**

| Feature             | Pandas 🐼                | Polars ⚡                |
| ------------------- | ------------------------ | ----------------------- |
| Performance         | Slower (single-threaded) | Faster (multi-threaded) |
| Memory Usage        | Higher                   | Lower                   |
| Execution Model     | Eager                    | Eager + Lazy            |
| Backend             | Python + NumPy           | Rust + Apache Arrow     |
| Large Data Handling | Limited                  | Excellent               |
| Syntax              | Beginner-friendly        | Slightly different      |

---
hideInToc: true
level: 2
---

### **Code Comparison**

<div class="grid grid-cols-2 gap-6">
<div>


#### **Pandas**

```python
import pandas as pd

df = pd.read_csv("data.csv")
result = df[df["age"] > 25]["name"]
```

<br/>

#### ⚠️ Key characteristics of Pandas

* Uses **index-based selection**
* Operations are **eagerly executed** (run immediately) 
* Typically **single-threaded**
* Syntax can feel **imperative and step-by-step**

</div>
<div>

#### **Polars**

```python
import polars as pl

df = pl.read_csv("data.csv")
result = df.filter(pl.col("age") > 25).select("name")
```

<br/>

#### ⚡ Key characteristics of Polars

* Uses **expression-based syntax**
* Supports **lazy execution (optional)** → query optimization 
* **Multi-threaded by default**
* More **functional / pipeline style**

</div>
</div>

---
hideInToc: true
level: 2
---

<div class="grid grid-cols-2 gap-6">
<div>

### **When to Use Polars ⚡**

<br/>

### ✅ **Use Polars When:**

* Working with **large datasets (GBs of data)**
* You need **high-speed data processing**
* Performing **complex transformations**
* Running **data pipelines / ETL workflows**
* Memory optimization is critical

</div>
<div>

### **When to Use Pandas 🐼**

<br/>

### ✅ **Use Pandas When:**


* Dataset is **small to medium**
* You need **quick prototyping**
* Working in **beginner-level projects**
* Heavy reliance on **Pandas-specific ecosystem**

</div>
</div>

---
hideInToc: true
level: 2
---

### **Real-World Scenarios**

**Polars Use Case:**

  * Processing millions of rows from logs or analytics data
  * Building high-performance data pipelines

**Pandas Use Case:**

  * Data cleaning for small datasets
  * Academic or beginner-level analysis

---
hideInToc: true
level: 2
---

### **Lazy vs Eager Execution**

| Feature              | Eager Execution              | Lazy Execution                       |
| -------------------- | ---------------------------- | ------------------------------------ |
| Execution Timing     | Immediate                    | Deferred until needed                |
| Evaluation Strategy  | Executes step-by-step        | Builds a plan, then executes         |
| Optimization         | No optimization              | Query optimization applied           |
| Performance          | Can be slower for large data | Faster for complex/large queries     |
| Memory Usage         | May use more memory upfront  | More efficient memory usage          |
| Debugging            | Easier to debug              | Slightly harder to trace             |
| Use Case             | Small tasks, simple logic    | Big data processing, pipelines       |



---
hideInToc: true
level: 2
---

## **Performance Optimization**

<br/>

#### **1. Memory Efficiency**

Polars uses **Apache Arrow columnar memory format**, which:

* Stores data in columns (not rows)
* Reduces memory overhead
* Improves cache efficiency

### **Example:**

```python
df = pl.read_csv("data.csv", dtypes={"age": pl.Int32})
```

👉 Explicit typing reduces memory usage

---
hideInToc: true
level: 2
---

## **Performance Optimization**

<br/>

#### **2. Parallel Execution**

Polars automatically uses **multi-core CPUs**.

* Operations run in parallel
* No manual configuration needed

### **Example:**

```python
df.groupby("department").agg(
    pl.col("salary").mean()
)
```

👉 Runs faster due to parallel aggregation

---
hideInToc: true
level: 2
---

## **Performance Optimization**

<br/>

#### **3. Query Optimization**

In **lazy mode**, Polars optimizes queries:

* Predicate pushdown (filters early)
* Projection pushdown (select needed columns)
* Avoids unnecessary computations

### **Example:**

```python
df = pl.scan_csv("data.csv")

result = (
    df.filter(pl.col("age") > 25)
      .select(["name"])
      .collect()
)
```

---
transition: fade
layout: image-right
image: https://www.scaler.com/topics/images/what-is-type-casting-in-python_thumbnail.webp
---

# **Strict Type Casting**

## Type Casting

Type casting is the process of converting a variable from one data type (e.g.,int, float, string) to another, either automatically (implicit) or manually (explicit). It ensures data compatibility for operations, such as converting a double to an int to remove decimals, though this may lead to data loss.


---
hideInToc: true
level: 2
---

### **Importance of Data Types**

Data types define how data is stored, processed, and interpreted in a DataFrame. Proper type management is critical for **performance, memory efficiency, and correctness**.

### **Impact on Performance**

Choosing the correct data type has a **direct impact on speed and efficiency**.

#### **Why it matters:**

* Smaller data types → **less memory usage → faster computation**
* Correct types → **optimized operations**
* Avoids unnecessary conversions during execution

---
hideInToc: true
level: 2
---

### **Real Problem (Wrong Type):**
```python
# Inefficient
"age" stored as string → "25"
# Efficient
"age" stored as integer → 25
```

📌 Storing numeric data as strings increases storage and slows queries

<div class="grid grid-cols-2 gap-6">
<div>

### Example:
<br/>

* Storing numbers as `int32` instead of `int64` reduces memory
* Storing numbers as `string` is inefficient and slow

</div>
<div>

#### **Example: Type Optimization**

```python
import pandas as pd

df = pd.read_csv(
    "data.csv",
    dtype={
        "age": "int32",
        "salary": "float32"
    }
)
```

👉 This reduces memory and improves performance

</div>
</div>


---
hideInToc: true
level: 2
---



## **Common Issues:**

<div class="grid grid-cols-2 gap-6 my-4">
<div>

#### ❌ Mixed Types in a Column

```python
["10", 20, "30"]
```

* Leads to unexpected behavior
* Forces system to treat column as generic type (`object`)

👉 This can cause **hidden computational errors**

</div>
<div>

#### ❌ Incorrect Type Inference

* CSV loaders may misinterpret:

  * `"001"` → integer (loses leading zeros)
  * `"2024-01-01"` → string instead of date

<br/>

#### ❌ Invalid Operations

```python
"100" + "200"  # Output: "100200" (string concatenation)
```

Instead of:

```python
100 + 200  # Output: 300
```

</div>
</div>



---
hideInToc: true
level: 2
---

## **Why Schema Enforcement Helps**

Schema enforcement means **defining data types explicitly** instead of relying on automatic inference.


<div class="grid grid-cols-2 gap-6">
<div>

### **Example: Schema Enforcement in Pandas**

```python
import pandas as pd

df = pd.read_csv(
    "data.csv",
    dtype={
        "id": "int32",
        "name": "string",
        "salary": "float64"
    },
    parse_dates=["date"]
)
```

</div>
<div>

### ✅ **Benefits:**

* Prevents incorrect type inference
* Ensures data consistency
* Catches errors early
* Makes pipelines more reliable

</div>
</div>

---
hideInToc: true
level: 2
---

## **Best Practices**

<br/>

### ✅ Always:

* Define schema while loading data
* Use smallest possible data type (`int8`, `int16`, etc.)
* Convert categorical text to efficient types
* Validate data before casting

<br/>

### ❌ Avoid:

* Using generic types like `object`
* Storing numbers as strings
* Relying completely on automatic type inference

---
transition: fade
level: 2
hideInToc: true
---

# **Type Casting in pandas**

## **1. `astype()` Method**

The `astype()` method in pandas is the **primary tool for explicit type conversion**, allowing you to enforce a strict schema on your dataset rather than relying on automatic type inference. In real-world data pipelines, raw data often comes in inconsistent formats (e.g., numbers stored as strings), and `astype()` helps standardize these values into correct types for computation.

<div class="grid grid-cols-2 gap-6">
<div>

### **Example:**

```python
import pandas as pd

df = pd.DataFrame({
    "age": ["25", "30", "22"]
})

df["age"] = df["age"].astype(int)
```

</div>
<div>

### **Key Insights:**

* Enforces **strict type consistency**
* Essential for **data cleaning pipelines**
* Helps avoid incorrect operations (e.g., string concatenation instead of addition)

</div>
</div>

---
hideInToc: true
level: 2
---


## **2. Nullable dtypes**

Traditional pandas had a limitation: when a column contained missing values (`NaN`), integer columns were automatically converted into floating-point types. This created inconsistencies, especially when working with identifiers or counts.

To solve this, pandas introduced **nullable dtypes**, which allow missing values while preserving the original data type. Instead of using `NaN`, pandas uses a special value `<NA>` for missing data.


### **Example:**

```python
df["age"] = df["age"].astype("Int64")
```

<br/>

### **Why It Matters:**

* Maintains **type integrity**
* Handles missing values consistently
* Avoids implicit conversions that can break logic


---
hideInToc: true
level: 2
---

## **3. Category Type Usage**

The `category` dtype is designed for **columns with a limited number of unique values (low cardinality)**. Instead of storing repeated strings multiple times, pandas stores each unique value once and represents the column using integer codes internally.

This significantly reduces memory usage and improves performance for operations like grouping, sorting, and filtering.

### **Example:**

```python
df["department"] = df["department"].astype("category")
```

### **Advantages:**

* Reduced memory footprint
* Faster operations on categorical data
* Ideal for analytical queries

---
transition: fade
level: 2
hideInToc: true
---

# **Type Casting in Polars**

## **1. Schema Definition on Load**

Polars promotes a **schema-first approach**, meaning you define column data types at the time of data loading instead of correcting them later. This is a critical design difference compared to pandas and is one of the reasons Polars is faster and more reliable in production pipelines.

<div class="grid grid-cols-2 gap-6">
<div>

### **Example:**

```python
import polars as pl

df = pl.read_csv(
    "data.csv",
    dtypes={
        "id": pl.Int32,
        "name": pl.Utf8,
        "salary": pl.Float64
    }
)
```

</div>
<div>

### **Why This Matters:**

* Prevents incorrect type inference
* Reduces runtime overhead
* Ensures consistency across pipelines

</div>
</div>

---
transition: fade
level: 2
hideInToc: true
---

## **2. Explicit Casting**

Polars provides the `cast()` method for converting data types explicitly. Unlike pandas, Polars emphasizes **strict validation during casting**, ensuring that invalid conversions do not go unnoticed.

Casting changes the underlying data type of a column and is implemented using efficient computation engines in Rust. ([pola-rs.github.io][4])

### **Example:**

```python
df = df.with_columns(
    pl.col("age").cast(pl.Int32)
)
```

<br/>

### **Multiple Columns:**

```python
df = df.cast({
    "age": pl.Int32,
    "salary": pl.Float32
})
```

---
transition: fade
level: 2
hideInToc: true
---

## **3. Strict vs Non-Strict Casting**

One of the most important features in Polars is the `strict` parameter.

* **strict=True (default):**

  * Raises an error if conversion fails
  * Ensures data correctness

* **strict=False:**

  * Converts invalid values to `null` instead of failing

This behavior is crucial in production systems because it forces developers to explicitly handle data inconsistencies rather than ignoring them.

### **Example:**

```python
df = df.with_columns(
    pl.col("age").cast(pl.Int32, strict=False)
)
```

---
transition: fade
level: 2
hideInToc: true
---

## **4. Handling Real-World Data Issues**

In real datasets, columns often contain mixed or dirty values (e.g., `"123"`, `"N/A"`, `"45.6"`). Polars enforces strict type checking, so such columns must be cleaned before casting.

If numeric values are stored as strings, operations like aggregation or filtering may fail or produce incorrect results unless properly converted.

### **Example:**

```python
df = df.with_columns(
    pl.col("amount").cast(pl.Float64)
)
```

---
transition: fade
---

# **Memory Optimization**

<div>

Memory optimization enhances system performance and efficiency by managing RAM usage, reducing bloat, and preventing leaks. Key techniques include closing background applications, managing startup programs, enabling memory compression, and using efficient data structures.

<img src="https://files.codingninjas.in/article_images/custom-upload-1682956745.webp" width=600>

</div>

---
hideInToc: true
level: 2
---

## **Why Memory Optimization Matters**

Memory optimization is a **critical aspect of data processing**, especially when working with DataFrames in tools like pandas or Polars. Since these libraries load data directly into RAM, inefficient memory usage can quickly become a bottleneck, affecting both performance and system stability.

In real-world data science and data engineering workflows, datasets often scale from thousands to **millions or even billions of rows**. Without proper memory management, operations can slow down drastically or even fail due to insufficient memory.

<img src="https://scrapingant.com/blog/img/blog/memory-optimization-techniques-for-python-applications.png" width=500>   

---
hideInToc: true
level: 2
---

## **1. Large Dataset Handling**

Handling large datasets is one of the primary reasons why memory optimization is essential. Most DataFrame libraries (like pandas) **load the entire dataset into memory**, which means the dataset size must fit within available RAM. ([GeeksforGeeks][1])

When datasets grow beyond a few gigabytes, this approach becomes inefficient or even impossible. Excessive memory usage can lead to:

* System slowdowns
* Memory overflow errors
* Application crashes

<br/>

---
hideInToc: true
level: 2
---

#### **📌 Key Challenge**

* A dataset with millions of rows can consume **GBs of memory**
* Intermediate operations (filtering, joins) may create **temporary copies**, increasing memory usage further 


<br/>

### **Example Scenario**

* CSV file size → 2 GB
* Loaded DataFrame → 5–8 GB (due to overhead and duplication)

👉 This mismatch makes optimization necessary

### **Optimization Techniques**

* Chunk processing (reading data in parts)
* Using efficient data formats (Parquet)
* Reducing data types

---
hideInToc: true
level: 2
---

## **2. Performance Improvement**

Memory optimization is not just about reducing RAM usage—it directly impacts **execution speed and computational efficiency**.

When memory usage is high:

* CPU spends more time managing memory
* Cache efficiency decreases
* Data access becomes slower

Efficient memory usage improves **data locality**, meaning operations can be executed faster because data is easier to access in memory.

###  **Performance Impact**

* Optimized datasets can run **10–100x faster operations** ([ML Journey][3])
* Memory reduction can be as high as **50–90%** ([ML Journey][3])

---
hideInToc: true
level: 2
---


### **Why Performance Improves**

1. **Smaller Data Types → Faster Computation**

   * Less memory → faster processing
   * Example: `int32` vs `int64`

2. **Better Cache Utilization**

   * Compact data fits into CPU cache
   * Reduces memory access time

3. **Reduced Data Movement**

   * Less copying during operations
   * Faster transformations

---
hideInToc: true
level: 2
---

### **Real-World Impact**

<div class="grid grid-cols-2 gap-6">
<div>

**Without Optimization:**

* ⏳ Processing takes hours to complete
* 🔁 Redundant computations slow down performance
* 💻 High CPU and memory usage
* ⚡ Increased energy consumption and operational costs
* 🚧 System bottlenecks and poor scalability
* 😕 Delayed results and poor user experience

</div>
<div>

**With Optimization:**

* ⚡ Processing takes minutes instead of hours
* 🚀 Faster and more efficient execution
* 🧠 Optimal use of CPU, memory, and resources
* 💰 Reduced operational and infrastructure costs
* 📈 Improved scalability and system performance
* 😊 Faster results and better user experience

</div>
</div>


---
hideInToc: true
layout: image-right
image: https://miro.medium.com/v2/1*oHl0vHbvrY5S58Vbuogl8Q.png
level: 2
---

# **Memory Optimization Techniques**

<div>

Memory optimization is not a single step but a **combination of strategies applied during data loading, transformation, and storage**. These techniques help reduce memory footprint, improve performance, and enable handling of large-scale datasets efficiently.

</div>

---
hideInToc: true
level: 2
---

## **1. Downcasting Data Types**

Downcasting refers to converting data types into **smaller, more memory-efficient representations** without losing information.

By default, libraries like pandas use `int64` and `float64`, which consume more memory than necessary. However, many real-world datasets do not require such large ranges.

<div class="grid grid-cols-2 gap-4">
<div>

### 🔹 **Concept**

* `int64 → int32 → int16 → int8`
* `float64 → float32`

This reduces memory usage significantly because smaller types use fewer bytes.

</div>
<div>

### **Example:**

```python
import pandas as pd

df["age"] = pd.to_numeric(df["age"], downcast="integer")
df["salary"] = pd.to_numeric(df["salary"], downcast="float")
```

</div>
</div>


📌 Downcasting can reduce memory usage by up to **75% for numeric columns** when values fit within smaller ranges 

---
hideInToc: true
level: 2
---

## **2. Using Categorical Data**

Categorical encoding is one of the most powerful memory optimization techniques for **string columns with repeated values**.

Instead of storing repeated strings multiple times, the system stores:

* Unique values once
* Integer references for each row

📌 This can reduce memory usage drastically (e.g., **95% reduction in some cases**)

<div class="grid grid-cols-2 gap-6">
<div>

### **Example:**

```python
df["country"] = df["country"].astype("category")
```

**Avoid When:**

* High cardinality (e.g., unique IDs)


</div>
<div>

**When to Use:**

* Low cardinality columns (e.g., gender, city, category)
* Repeated string values


</div>
</div>

---
hideInToc: true
level: 2
---

## **3. Chunk Processing (Out-of-Core Processing)**

Chunking allows you to process large datasets **piece-by-piece instead of loading everything into memory at once**.

This is especially useful when the dataset size exceeds available RAM.

📌 Chunking enables working with datasets **larger than memory** by processing them incrementally


### **Example:**

```python
import pandas as pd

chunks = pd.read_csv("data.csv", chunksize=100000)

for chunk in chunks:
    process(chunk)
```

**How It Works:**

* Load a small portion of data
* Process it
* Move to next chunk


---
hideInToc: true
level: 2
---

## **4. Efficient File Formats (Parquet, Feather)**

Traditional formats like CSV are **row-based and inefficient**, while formats like Parquet are **columnar and optimized for analytics**.

### **Why Parquet is Better:**

* Compression reduces file size
* Columnar storage → load only required columns
* Faster read/write operations

📌 Columnar formats allow selective data loading, reducing memory usage significantly ([neuronovai.com][1])

### **Example:**

```python
df = pd.read_parquet("data.parquet")
```


---
hideInToc: true
level: 2
---

## **5. Dropping Unnecessary Data**

Often, datasets include columns or rows that are irrelevant to the analysis. Retaining such unnecessary data increases memory consumption and can slow down processing.

### **Example:**

```python
df = df.drop(columns=["unused_column"])
```

<div class="grid grid-cols-2 gap-4">
<div>

#### **Best Practices:**

* Use `usecols` while reading data to load only required columns
* Remove intermediate variables that are no longer needed
* Drop unused rows or columns early in the workflow
* Regularly review the dataset to keep only relevant features

</div>
<div>

#### **Impact:**

* Reduces memory usage
* Improves processing speed and efficiency
* Enhances overall performance of data pipelines

📌 Removing unused data helps streamline computation and resource utilization

</div>
</div>

---
hideInToc: true
level: 2
---

## **6. Avoiding Memory Copies**

Certain operations in **pandas** create **hidden copies of data**, increasing memory usage without being obvious. This can significantly slow down your workflow, especially with large datasets.

<div class="grid grid-cols-2 gap-6">
<div>

❌ **Inefficient Approach (Row-wise operation):**

```python
df["flag"] = df.apply(lambda x: x["price"] > 100, axis=1)
```

✅ **Efficient Approach (Vectorization):**

```python
df["flag"] = (df["price"] > 100).astype("int8")
```


</div>
<div>


**Why This Matters:**

- Row-wise operations (`apply` with `axis=1`) create temporary objects
- Hidden memory copies increase RAM usage
- Slower execution due to Python-level loops
- Vectorized operations use optimized, low-level implementations

</div>
</div>

---
hideInToc: true
level: 2
---

**Best Practices:**

*  Avoid `apply()` for row-wise operations when possible
*  Prefer vectorized operations (`+`, `-`, comparisons, etc.)
*  Use built-in pandas methods instead of custom loops
*  Check for unintended copies when chaining operations

📌 Vectorization helps eliminate unnecessary data copies and boosts overall efficiency

---
hideInToc: true
level: 2
---

## **7. Sparse Data Structures**

For datasets with many zero or missing values, **sparse data structures** in **pandas** help save memory by storing only the **non-zero (or non-null) values** instead of the entire dataset.

<div class="grid grid-cols-2 gap-6">
<div>

### **Example:**

```python
df["col"] = pd.arrays.SparseArray(df["col"])
```

**Use Cases:**

* Large datasets with many zero values
* Machine Learning feature matrices (e.g., one-hot encoding)
* Sparse matrices in recommendation systems
* Data with many missing (`NaN`) values

</div>
<div>


**Why This Matters:**

* Stores only meaningful (non-zero) data → reduces memory usage
* Improves performance for large, sparse datasets
* Enables handling of datasets that otherwise wouldn’t fit in memory

📌 Sparse structures are ideal when your data is mostly empty—they store less and compute smarter

</div>
</div>

---
hideInToc: true
level: 2
---

## **8. In-Place Operations & Garbage Collection**

Performing operations **in-place** avoids creating new copies of data.

**Example:**

```python
df.drop("col", axis=1, inplace=True)
```

**Memory Cleanup:**

```python
import gc
del temp_df
gc.collect()
```

**Benefits:**

* Reduces temporary memory usage
* Prevents memory leaks

---
hideInToc: true
level: 2
---

## **Summary**

Memory optimization techniques include:

* **Downcasting** → Reduce numeric memory
* **Categorical types** → Optimize string storage
* **Chunking** → Process large datasets safely
* **Efficient formats (Parquet)** → Reduce I/O + memory
* **Dropping unused data** → Avoid unnecessary overhead
* **Vectorization** → Prevent hidden copies
* **Sparse structures** → Optimize sparse datasets



---
hideInToc: true
layout: image-right
image: https://files.realpython.com/media/Showcase-Polars_Watermarked.4e25d4f6c9a7.jpg
level: 2
---

### **Memory Optimization Techniques in Polars**

<div>

Polars is designed from the ground up for **high-performance and memory-efficient data processing**. Unlike traditional libraries, it combines **columnar data structures, lazy execution, and query optimization** to minimize memory usage while maximizing speed.

</div>


---
hideInToc: true
level: 2
---

## **Efficient Data Structures**

One of the core reasons Polars is memory-efficient is its use of **Apache Arrow-based columnar data structures**.

### 🔹 **Columnar Storage (Apache Arrow)**

In Polars, data is stored **column-wise instead of row-wise**, meaning each column is stored contiguously in memory.

📌 This enables:

* Better compression
* Faster processing
* Reduced memory footprint



---
hideInToc: true
level: 2
---

### 🔹 **Zero-Copy Architecture**

**Polars** leverages **zero-copy memory sharing**, meaning data is reused instead of being duplicated during operations.

<div class="grid grid-cols-2 gap-6">
<div>

**What It Means:**

* Data is **not copied unnecessarily** between operations
* Multiple operations can reference the same underlying memory
* Eliminates overhead from repeated data duplication


</div>
<div>

**Key Benefits:**

* **Minimal memory usage** even with large datasets
* **Faster execution** due to reduced data movement
* **Efficient data pipelines** with less overhead
* Better scalability for high-performance workloads

</div>
</div>

📌 Especially powerful when chaining multiple operations on large datasets without incurring extra memory costs

---
hideInToc: true
level: 2
---

### 🔹 **Selective Data Loading**

Using **Polars**, you can load only the required columns while reading data, which helps reduce memory usage and improve performance.


### **Example:**

```python
import polars as pl

df = pl.read_csv("data.csv", columns=["name", "age"])
```

<div class="grid grid-cols-2 gap-6">
<div>

**What Happens Here:**

* 📂 Only **"name"** and **"age"** columns are loaded
* ❌ Unnecessary columns are ignored during read
* 💾 Memory usage is significantly reduced


</div>
<div>

**Best Practices:**

* 🎯 Always specify `columns` when working with large datasets
* 🔍 Identify required fields before loading data
* 🚀 Combine with other optimizations (like lazy execution in Polars)

</div>
</div>

---
hideInToc: true
level: 2
---

## **2. Lazy Evaluation Benefits**

Lazy evaluation is one of the **most powerful optimization techniques in Polars**.

<div class="grid grid-cols-2 gap-6">
<div>

### 🔹 **What is Lazy Evaluation?**

Lazy evaluation means that operations are **not executed immediately**. Instead:

* Polars builds a `query plan` instead of running each step instantly
* Execution happens only when `.collect()` is called

👉 This avoids unnecessary intermediate computations 

</div>
<div>

### 🔹 **How It Works**

```python
import polars as pl

df = pl.scan_csv("data.csv")  # Lazy loading

result = (
    df.filter(pl.col("age") > 25)
      .select(["name"])
      .collect()
)
```

* No execution happens until `.collect()`
* Entire pipeline is optimized before execution

</div>
</div>

---
hideInToc: true
layout: two-cols
layoutClass: gap-10
level: 2
---


## **Memory Benefits of Lazy Execution**

Lazy evaluation significantly reduces memory usage by avoiding intermediate DataFrames.


### 🔹 **Key Advantages**

<br/>

#### ✅ **1. No Intermediate Copies**

* Eager execution creates multiple temporary DataFrames
* Lazy execution avoids this

📌 Results in **lower memory consumption**

:: right ::

#### ✅ **2. Query Optimization**

Polars applies advanced optimizations like:

* **Predicate Pushdown** → Filter early
* **Projection Pushdown** → Load only required columns
* **Join Optimization** → Efficient joins

📌 These optimizations reduce unnecessary data processing 

---
hideInToc: true
layout: two-cols
layoutClass: gap-10
level: 2
---


#### ✅ **3. Reduced Data Loading**

* Only **required rows and columns** are processed
* Avoids loading the entire dataset into memory
* Minimizes memory usage by skipping unnecessary data
* Improves I/O efficiency and speeds up data access

:: right ::

#### ✅ **4. Faster Execution**

* Entire pipeline is **optimized as a single query**
* Eliminates repeated and redundant computations
* Executes operations more efficiently under the hood
* Delivers significantly faster performance for large workflows

📌 Can lead to **significant speed improvements**



---
layout: full
---

# **Mini Project** 
## **Reproducible Data Ingestion Pipeline**

### **Task:**

Build a complete data pipeline that loads, processes, and saves data in a reproducible way.

<div class="grid grid-cols-2 gap-6 my-5">
<div>

### **Steps to Follow:**

#### **1. Setup Environment (using `uv`)**

* Create a project using `uv`
* Initialize environment and project
* Install required libraries:

  * `pandas`
  * `requests`
  * *(optional)* `polars`


</div>
<div>

Example setup:

```bash
uv venv
uv pip install pandas requests polars
```

</div>
</div>

---
hideInToc: true
layout: full
level: 2
---

### **Steps to Follow:**

<div class="grid grid-cols-2 gap-6 my-5">
<div>

#### **2. Version Control**

* Initialize a `Git` repository
* Create a proper `.gitignore` file
* Ensure you **do NOT track**:

  * raw data
  * virtual environments
  * logs

#### **3. Load Data**

* Read a **CSV file** using pandas
* Fetch data from an **API** using requests


</div>
<div>

#### **4. Clean Data**

* Handle missing values
* Remove duplicate rows
* Standardize column names (lowercase, no spaces)

#### **5. Transform Data**

* Create at least one new column
  *(Example: total_amount = price × quantity)*

#### **6. Apply Type Casting**

* Convert columns to appropriate data types
* Use `category` type where applicable


</div>
</div>

---
hideInToc: true
layout: full
level: 2
---

### **Steps to Follow:**

<div class="grid grid-cols-2 gap-6 my-5">
<div>

### **7. Optimize Memory**

* Downcast numeric columns
* Remove unnecessary columns (if any)


### **8. Save Output**

* Save the processed dataset as:

  * `.csv` **OR**
  * `.parquet`

</div>
<div>

### **9. Make it Reproducible**

Ensure anyone can run your project using:

```bash
uv venv
uv pip install -r requirements.txt
python src/main.py
```

</div>
</div>

---
hideInToc: true
layout: full
level: 2
---

## ✅ Expected Output (Project Deliverables)

### **1. 📁 Project Structure**

<div class="grid grid-cols-2 gap-4">
<div>

The project must follow a clean and modular directory layout:

```
project/
├── README.md
├── requirements.txt
├── .gitignore
├── src/
│   └── main.py
├── data/
│   ├── raw/
│   │   └── (original input datasets go here)
│   └── processed/
│       └── (cleaned / transformed datasets will be saved here)
└── logs/ (optional)
    └── (runtime logs or debug outputs)
```

</div>
<div>

#### ✔️ Structure Rules

* `src/` contains all source code
* `data/raw/` stores untouched input data
* `data/processed/` stores cleaned dataset output
* `main.py` must act as the **single entry point**
* Keep the structure minimal but scalable

</div>
</div>

---

### **2. 🧹 Processed Dataset Output**

A cleaned and transformed dataset must be generated during execution.

#### ✔️ Requirements:

* Must be saved inside:

```
data/processed/
```

#### ✔️ Expected Characteristics:

* Missing values handled
* Duplicates removed (if applicable)
* Standardized formatting (dates, text, numeric fields)
* Final dataset ready for analysis or modeling

#### ✔️ File Format Examples:

* `.csv` (preferred)
* `.json` (if required by pipeline)

---

### **3. ⚙️ Working End-to-End Pipeline**

The project must include a **single executable script**:

```
src/main.py
```

#### ✔️ Responsibilities of `main.py`:

* Load raw data from `data/raw/`
* Perform all preprocessing steps
* Apply transformations / cleaning logic
* Save output to `data/processed/`
* Print execution logs or status messages

#### ✔️ Command to Run:

```bash
python src/main.py
```

---

### **4. 📦 Dependencies File**

A `requirements.txt` file must be included.

#### ✔️ Requirements:

* List all external Python libraries used
* Include version pins for reproducibility (recommended)

#### ✔️ Example:

```
pandas==2.2.0
numpy==1.26.4
scikit-learn==1.4.1
```

---

### **5. 🗂️ Git Repository Standards**

The project must be properly version-controlled.


#### ✔️ .gitignore must include:

```
__pycache__/
*.pyc
.env
data/raw/
data/processed/
venv/
```

*(Adjust based on whether raw/processed data should be tracked or ignored)*

---

### **6. 📘 README.md (Documentation)**

A complete and professional README is required.

#### ✔️ Setup Instructions

```bash
uv venv
uv pip install -r requirements.txt
```

#### ✔️ How to Run the Project

```bash
python src/main.py
```

#### ✔️ Expected Workflow

1. Place raw data in `data/raw/`
2. Run `main.py`
3. Get cleaned dataset in `data/processed/`


---
layout: intro
hideInToc: true
---

# Thank you
