
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
