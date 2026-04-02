# **Introduction to Pandas**

## **1. What is Pandas?**

**Pandas** is an **open-source Python library** used for **data manipulation, cleaning, and analysis**.

👉 In simple terms:

> Pandas = “Tool to work with data easily in Python”

📌 It provides powerful data structures like:

* **Series** → 1D data
* **DataFrame** → 2D tabular data

These structures make it easy to work with data similar to **Excel tables or SQL tables**

---
layout: full
level: 2
hideInToc: true
---

## **2. Core Idea Behind Pandas**

Pandas is designed to:

* Handle **real-world messy data**
* Convert raw data → clean, structured format
* Perform **analysis efficiently**

👉 It acts as the **foundation of data analysis in Python**

---
layout: two-cols
layoutClass: gap-5
level: 2
hideInToc: true
---


## **3. What is Pandas Used For?**

Pandas is widely used in:

* ✔ **Data Cleaning**

  * Handling missing values
  * Removing duplicates

* ✔ **Data Transformation**

  * Filtering
  * Sorting
  * Aggregation

* ✔ **Data Analysis**

  * Statistical analysis
  * Insights generation

:: right ::

* ✔ **Machine Learning (Preprocessing)**

  * Preparing datasets

* ✔ **Data Visualization**

  * Works with libraries like Matplotlib

👉 It allows you to **load, clean, transform, and analyze data in just a few lines of code**


---
layout: full
level: 2
hideInToc: true
---


## **4. Why Use Pandas?**

### **1. Efficient Handling of Large Data**

* Designed for large datasets
* Supports multiple formats:

  * CSV
  * JSON
  * Excel
  * SQL databases

👉 Makes data loading and processing easy


---
layout: full
level: 2
hideInToc: true
---

### **2. Tabular Data Representation**

* Uses **DataFrames (rows & columns)**
* Supports:

  * Indexing
  * Slicing
  * Filtering

👉 Similar to working with spreadsheets


### **3. Data Cleaning & Preprocessing**

* Built-in methods for:

  * Missing values (NaN handling)
  * Duplicate removal
  * Data normalization

👉 Essential for real-world datasets


---
layout: full
level: 2
hideInToc: true
---

### **4. Time Series Support**

* Handles:

  * Dates
  * Time-based indexing
  * Financial data

👉 Widely used in **finance and analytics**


### **5. Free & Open Source**

* Completely free to use
* Supported by a large community
* Continuously updated

---
layout: full
level: 2
hideInToc: true
---

## **5. Key Features of Pandas**

* ✔ Easy handling of missing data
* ✔ Powerful **groupby operations**
* ✔ Data merging and joining
* ✔ Flexible reshaping (pivot, melt)
* ✔ Fast performance (built on NumPy)

---
layout: full
level: 2
hideInToc: true
---


## **6. Key Points to Remember**

###  Built on NumPy

Uses fast numerical operations

###  Two Main Structures

* Series (1D)
* DataFrame (2D)

###  Works with Real Data

Handles messy, large datasets

###  Industry Standard

Used in:

* Data Science
* Machine Learning
* Analytics


---
layout: full
level: 2
hideInToc: true
---

# **Install Pandas**

## **1. Prerequisites**

Before installing **Python** Pandas, ensure your system has:

* ✔ **Python installed**
* ✔ **pip (Python package manager)**

### **Verify Installation**

```bash
python --version
pip --version
```

👉 If both commands return versions, your environment is ready.


---
layout: full
level: 2
hideInToc: true
---

## **2. Install Pandas using pip**

The simplest way to install Pandas is using pip:

```bash
pip install pandas
```

### **What happens internally?**

* Downloads the latest Pandas version
* Installs required dependencies (like **NumPy**)
* Makes Pandas available in your environment

### **Verify Installation**

```bash
python -c "import pandas as pd; print(pd.__version__)"
```

📌 Expected output:

```
2.x.x
```

👉 Confirms Pandas is installed successfully.


---
layout: full
level: 2
hideInToc: true
---

## **3. Recommended Approach: Virtual Environment**

Installing packages globally can create dependency conflicts.
👉 Best practice = Use isolated environments

### **Create Virtual Environment**

```bash
python -m venv venv
```

### **Activate Environment**

**Windows**

```bash
venv\Scripts\activate
```

**macOS / Linux**

```bash
source venv/bin/activate
```

---
layout: full
level: 2
hideInToc: true
---

### **Install Pandas Inside Environment**

```bash
pip install pandas
```

📌 This ensures:

* Clean project setup
* No version conflicts
* Reproducibility


---
layout: full
level: 2
hideInToc: true
---

## **4. Modern & Faster Method: Using UV**

A modern alternative to pip is **uv**, known for its speed and efficiency.

### **Install UV**

```bash
pip install uv
```

<br/>

### **Install Pandas using UV**

```bash
uv pip install pandas
```

---
layout: full
level: 2
hideInToc: true
---

### **Project-Based Setup (Recommended)**

```bash
uv init my_project
cd my_project
uv add pandas
```

👉 This will:

* Create project structure
* Setup `.venv` automatically
* Manage dependencies via `pyproject.toml`


---
layout: full
level: 2
hideInToc: true
---

## **5. Import Pandas in Python**

After installation, import Pandas using:

```python
import pandas as pd
```

### **Why use `pd`?**

* Standard alias used globally
* Makes code shorter and readable

### **Example Usage**

```python
import pandas as pd

df = pd.DataFrame({
    "Name": ["Ravi", "Priya"],
    "Age": [30, 27]
})

print(df)
```


---
layout: full
level: 2
hideInToc: true
---

## **6. Key Points to Remember**

*  Use **pip** for simple installation
*  Use **virtual environments** for best practice
*  Use **uv** for faster and modern workflows
*  Always verify installation
*  Import using `import pandas as pd`


---
layout: full
level: 2
hideInToc: true
---

# **Reading Data with Pandas**

## **Overview**

**Pandas** provides powerful and flexible functions to read data from multiple file formats into a **DataFrame**, which is the core structure used for analysis.

### **Supported Formats**

* CSV (most common)
* Excel (`.xlsx`)
* JSON
* SQL databases
* Text files

👉 This makes Pandas a **central tool in data ingestion and preprocessing pipelines**.

---
layout: full
level: 2
hideInToc: true
---

## **Reading CSV Files**

### **What is a CSV File?**

* Plain text file storing **tabular data**
* Each row = record
* Values separated by a delimiter (default: comma `,`)

### **Example CSV**

```csv
Name,Age,City
Alice,25,New York
Bob,30,London
```

---
layout: full
level: 2
hideInToc: true
---

## **Basic Usage: `read_csv()`**

```python
import pandas as pd

df = pd.read_csv("file.csv")
```

### **What happens here?**

* Reads file
* Parses rows & columns
* Converts into a **DataFrame**

---
layout: full
level: 2
hideInToc: true
---

# **Key Parameters (Must Know)**

## **1. `delimiter`**

### **Purpose**

Defines how values are separated in the file.

### **When to use**

* When file is NOT comma-separated

### **Example**

```python
df = pd.read_csv("file.csv", delimiter=";")
```

### **Common delimiters**

* `,` → default
* `;` → semicolon
* `\t` → tab
* `|` → pipe

---
layout: full
level: 2
hideInToc: true
---

## **2. `encoding`**

### **Purpose**

Specifies how characters are encoded in the file.

### **Why important?**

Prevents errors like:

```
UnicodeDecodeError
```

### **Example**

```python
df = pd.read_csv("file.csv", encoding="utf-8")
```

### **Common encodings**

* `utf-8` → standard (recommended)
* `latin1` → special characters
* `cp1252` → Windows files

---
layout: full
level: 2
hideInToc: true
---

## **3. `header`**

### **Purpose**

Specifies which row should be treated as column names.

### **Examples**

```python
df = pd.read_csv("file.csv", header=0)      # default
df = pd.read_csv("file.csv", header=None)   # no header
```

### **Manual column naming**

```python
df = pd.read_csv("file.csv", header=None)
df.columns = ["Name", "Age", "City"]
```

---
layout: full
level: 2
hideInToc: true
---

## **4. `dtype`**

### **Purpose**

Explicitly define column data types.

### **Example**

```python
df = pd.read_csv("file.csv", dtype={"Age": int})
```

### **Why use it?**

* Improves performance
* Reduces memory usage
* Avoids incorrect type inference

---
layout: full
level: 2
hideInToc: true
---

# **Handling Large CSV Files**

## **Problem**

Large files may not fit into memory ❌

## **Solution → `chunksize`**

### **Example**

```python
chunk_iter = pd.read_csv("large_file.csv", chunksize=1000)

for chunk in chunk_iter:
    print(chunk.head())
```

## **How It Works**

* Reads file in **small batches (chunks)**
* Each chunk = separate DataFrame
* Processes data incrementally

---
layout: full
level: 2
hideInToc: true
---

## **Real Use Case: Aggregation**

```python
total = 0

for chunk in pd.read_csv("large_file.csv", chunksize=1000):
    total += chunk["Sales"].sum()

print(total)
```

👉 Efficient for:

* Big data processing
* Memory-constrained systems
* Streaming-style computations

---
layout: full
level: 2
hideInToc: true
---

# **Key Takeaways**

* `read_csv()` is the **entry point for most data workflows**
* Always validate:

  * delimiter
  * encoding
  * header
  * dtype
* Use `chunksize` for **large datasets**
* Convert raw data → structured DataFrame → ready for analysis

---
layout: full
level: 2
hideInToc: true
---

# JSON Data & Pandas – Clear Explanation

## What is JSON?

**JSON (JavaScript Object Notation)** is a lightweight data format used to **store and exchange data between systems**, especially in APIs and web applications.

👉 In simple terms:

JSON = **structured text format using key–value pairs**

### Example:

```json
{
  "name": "John",
  "age": 25
}
```

---
layout: full
level: 2
hideInToc: true
---

##  Key Features of JSON

* **Key–Value Structure** → Easy to read and interpret
* **Nested Support** → Objects inside objects / arrays
* **Language Independent** → Works across Python, Java, etc.
* **API Standard** → Widely used in web communication
* **Flexible** → No strict schema required

---
layout: full
level: 2
hideInToc: true
---

# `read_json()` in Pandas

##  What is `read_json()`?

`read_json()` is used to **convert JSON data into a pandas DataFrame** for analysis. ([GeeksforGeeks][1])

👉 Think of it as:
JSON → DataFrame (table format)


##  Syntax

```python
pandas.read_json(path_or_buf, orient=None)
```

---
layout: full
level: 2
hideInToc: true
---

##  Important Parameters

### 1. `path_or_buf`

* File path, URL, or JSON string

<br/>

### 2. `orient` (Very Important)

Defines **how JSON is structured** so pandas knows how to convert it into a table.

---
layout: full
level: 2
hideInToc: true
---

### Common `orient` values:

| Orient    | Description                        |
| --------- | ---------------------------------- |
| `records` | List of dictionaries (most common) |
| `index`   | Keys = index                       |
| `columns` | Keys = column names                |
| `split`   | Separate index, columns, data      |
| `values`  | Only raw values                    |

👉 Example:

```python
df = pd.read_json("data.json", orient="records")
```

Why needed?
Pandas must understand **how to map JSON → rows & columns**

---
layout: full
level: 2
hideInToc: true
---

##  Basic Examples

### Read from file

```python
import pandas as pd

df = pd.read_json("data.json")
print(df)
```

### Read from string

```python
json_data = '{"name": "John", "age": 25}'

df = pd.read_json(json_data, typ='series')
print(df)
```

---
layout: full
level: 2
hideInToc: true
---

# Nested JSON Handling

## What is Nested JSON?

JSON that contains **objects inside objects or arrays inside objects**

### Example:

```json
{
  "id": 1,
  "name": "Alice",
  "contact": {
    "email": "alice@example.com"
  }
}
```

## ❌Problem with Nested JSON

* Not flat (hierarchical structure)
* Cannot directly convert to table
* Needs transformation

---
layout: full
level: 2
hideInToc: true
---

## Methods to Handle Nested JSON

### Method 1: Manual Access

```python
import json

data = json.loads(json_string)
email = data["contact"]["email"]
```

✔ Good for small data
❌ Not scalable

### Method 2: Using pandas

```python
df = pd.read_json("nested.json")
```

✔ Works partially
❌ Nested fields remain complex (not flattened)

---
layout: full
level: 2
hideInToc: true
---

# JSON Normalization (Most Important)

## What is Normalization?

Normalization is the process of converting **nested JSON → flat table (DataFrame)** using:

```python
pd.json_normalize()
```

👉 It “flattens” hierarchical data into columns.


## Syntax

```python
pandas.json_normalize(data, record_path=None, meta=None)
```

## Parameters

* `data` → JSON input
* `record_path` → path to nested list
* `meta` → additional fields to retain

---
layout: full
level: 2
hideInToc: true
---

## Example 1: Simple Flattening

```python
df = pd.json_normalize(data)
```

### Output:

```
id  name  contact.email  contact.phone
1   Alice  alice@example.com 1234567890
```

✔ Nested keys become column names

✔ Uses dot notation

---
layout: full
level: 2
hideInToc: true
---

## Example 2: Nested List Handling

```python
df = pd.json_normalize(
    data,
    record_path="skills",
    meta=["id", "name"]
)
```

### Output:

```
type         name   id   name
Programming  Python 1    Alice
Database     SQL    1    Alice
```

---
layout: full
level: 2
hideInToc: true
---

# 🧠 Key Concepts to Remember

* JSON = flexible, hierarchical data format
* `read_json()` → converts JSON → DataFrame
* `orient` → defines structure mapping
* Nested JSON cannot be directly tabular
* `json_normalize()` → **most important for real-world data**


---
level: 2
hideInToc: true
---

# **Excel Files in pandas**

## **What are Excel Files?**

Excel files (`.xlsx`, `.xls`) are widely used spreadsheet formats for storing **structured data in tabular form (rows & columns)**.

They support:

* Multiple sheets (tabs)
* Formulas and calculations
* Formatting and styling
* Different data types (text, numbers, dates)

Because of this, Excel is heavily used in **business reporting, analytics, and data exchange**.

---
hideInToc: true
level: 2
---

## **read_excel() Function**

The `read_excel()` function in **pandas** is used to **load Excel data into a DataFrame**.

### **Syntax**

```python
pandas.read_excel(io, sheet_name=0)
```

### **Key Parameters**

* `io` → File path, URL, or file-like object
* `sheet_name` → Sheet to read

  * `0` → First sheet (default)
  * `"Sheet1"` → By name
  * `None` → Load all sheets

---
hideInToc: true
level: 2
---

## **Basic Example**

```python
import pandas as pd

df = pd.read_excel("data.xlsx")
print(df)
```

* Reads the **first sheet by default**
* Converts Excel → DataFrame

---
hideInToc: true
level: 2
---

# **Working with Multiple Sheets**

## **Why Multiple Sheets Matter**

Excel files often store **different datasets in different sheets**:

* Sales Data
* Customer Data
* Inventory

---
hideInToc: true
level: 2
---

## **Read Specific Sheet**

```python
df = pd.read_excel("data.xlsx", sheet_name="Sales")
```

OR

```python
df = pd.read_excel("data.xlsx", sheet_name=1)
```

## **Read Only Required Columns**

```python
df = pd.read_excel("data.xlsx", usecols=["Name", "Revenue"])
```

✅ Improves performance
✅ Reduces memory usage


## **Handle Missing Values**

```python
df = pd.read_excel("data.xlsx", na_values=["NA", "Missing"])
```

* Converts specified values → `NaN`

---
hideInToc: true
level: 2
---

# **Reading All Sheets**

## **Load All Sheets**

```python
all_sheets = pd.read_excel("data.xlsx", sheet_name=None)
```

* Returns: **Dictionary of DataFrames**

```python
print(type(all_sheets))
# <class 'dict'>
```


## **Access Individual Sheets**

```python
sales_df = all_sheets["Sales"]
customers_df = all_sheets["Customers"]
```

---
hideInToc: true
level: 2
---

## **Loop Through Sheets**

```python
for sheet_name, df in all_sheets.items():
    print(f"Sheet: {sheet_name}")
    print(df.head())
```

## **Read Selected Sheets**

```python
dfs = pd.read_excel("data.xlsx", sheet_name=["Sales", "Customers"])
```

## **Combine All Sheets**

```python
combined_df = pd.concat(all_sheets.values(), ignore_index=True)
```

---
hideInToc: true
level: 2
---

# **SQL Databases in Python (pandas)**

## **What are SQL Databases?**

SQL databases store **structured data in tables (rows & columns)** and use queries to retrieve data.

Popular databases:

* SQLite → Lightweight (file-based)
* MySQL / PostgreSQL → Server-based
* SQL Server / Oracle → Enterprise

---
hideInToc: true
level: 2
---

# **Connecting to Databases**

## **Using sqlite3 (Beginner-Friendly)**

```python
import sqlite3

conn = sqlite3.connect("example.db")
```

* Creates/opens a `.db` file
* No server required

---
hideInToc: true
level: 2
---

## **Using SQLAlchemy (Recommended)**

```python
from sqlalchemy import create_engine

engine = create_engine("sqlite:///example.db")
```

* More scalable
* Supports multiple databases
* Preferred in production

---
hideInToc: true
level: 2
---

# **read_sql() Function**

Used to **execute SQL queries and load results into a DataFrame**

### **Syntax**

```python
pandas.read_sql(sql, con)
```

## **Example: Read Full Table**

```python
df = pd.read_sql("SELECT * FROM employees", conn)
```

---
hideInToc: true
level: 2
---

## **Example: Filter Data**

```python
df = pd.read_sql("""
SELECT name, salary
FROM employees
WHERE salary > 50000
""", conn)
```

## **Example: Aggregation**

```python
df = pd.read_sql("""
SELECT department, AVG(salary) as avg_salary
FROM employees
GROUP BY department
""", conn)
```

---
hideInToc: true
level: 2
---

## **Example: Join Tables**

```python
df = pd.read_sql("""
SELECT e.name, d.department_name
FROM employees e
JOIN departments d
ON e.dept_id = d.id
""", conn)
```

---
hideInToc: true
level: 2
---

# **Query-Based Ingestion (Important Concept)**

Instead of loading entire tables:

👉 Fetch only required data using SQL

### **Why this matters:**

* Improves performance
* Reduces memory usage
* Faster pipelines

---
hideInToc: true
level: 2
---

# **Best Practices (Real-World Use)**

* ✅ Use SQL filtering instead of pandas filtering for large data
* ✅ Prefer `SQLAlchemy` in production
* ✅ Avoid `SELECT *` → fetch only needed columns
* ✅ Use indexing in DB for faster queries
* ✅ Always close connections

```python
conn.close()
```

---
hideInToc: true
level: 2
---

# **APIs (Application Programming Interfaces)**

## **What is an API?**

An **API (Application Programming Interface)** is a defined set of rules that allows different software systems to communicate and exchange data.

Think of it as a **bridge between client and server**:

* **Client** → sends request (your Python script / app)
* **Server** → processes request
* **API** → defines how communication happens
* **Response** → data returned (usually JSON)


---
hideInToc: true
level: 2
---

## **How APIs Work (Request–Response Cycle)**

1. Client sends a request (GET, POST, etc.)
2. API endpoint receives the request
3. Server processes it
4. API sends back a response (usually JSON)


---
hideInToc: true
level: 2
---

## **When to Use APIs?**

Use APIs when:

* Data is **real-time or frequently updated**
* No static files (CSV/Excel) are available
* Data is hosted on external systems (e.g., weather, payments, social media)


---
hideInToc: true
level: 2
---

# **Fetching Data Using `requests`**

The Requests library is the most commonly used Python package to interact with APIs.

## **Basic API Call**

```python
import requests

url = "https://jsonplaceholder.typicode.com/posts"

response = requests.get(url)

if response.status_code == 200:
    print("Data fetched successfully")
else:
    print("Failed to fetch data")
```


---
hideInToc: true
level: 2
---

## **Understanding Response Object**

* `response.status_code` → HTTP status (200 = success)
* `response.json()` → converts response to Python object
* `response.text` → raw response


---
hideInToc: true
level: 2
---

# **Converting API Data to DataFrame**

API data is usually in **JSON format**, which can be converted into a Pandas DataFrame.

### **Example**

```python
import pandas as pd
import requests

url = "https://jsonplaceholder.typicode.com/posts"
response = requests.get(url)

data = response.json()

df = pd.DataFrame(data)

print(df.head())
```


---
hideInToc: true
level: 2
---

## **Why Convert to DataFrame?**

* Easy filtering (`df[df["userId"] == 1]`)
* Aggregation (`groupby`)
* Cleaning & transformation
* Integration with ML pipelines


---
hideInToc: true
level: 2
---

# **Handling Nested JSON**

Real-world APIs often return **nested JSON**, which is not directly tabular.


## **Solution: `json_normalize()`**

```python
df = pd.json_normalize(data)
```

### **Example**

```python
df = pd.json_normalize(data, record_path="items", meta=["id"])
```


## **When to Use `json_normalize()`**

* Nested objects
* Arrays inside JSON
* API responses with hierarchy 

---
hideInToc: true
level: 2
---

# **Handling Pagination**

APIs often return data in **chunks (pages)** instead of all at once.


## **Why Pagination?**

* Prevents overload
* Improves performance
* Reduces memory usage


---
hideInToc: true
level: 2
---

## **Method 1: Page-Based Pagination**

```python
import requests
import pandas as pd

url = "https://api.example.com/data"

all_data = []
page = 1

while True:
    response = requests.get(url, params={"page": page})
    data = response.json()

    if not data:
        break

    all_data.extend(data)
    page += 1

df = pd.DataFrame(all_data)
```


---
hideInToc: true
level: 2
---

## **Method 2: Limit & Offset**

```python
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
hideInToc: true
level: 2
---

# **Best Practices for API Data Ingestion**

### **1. Always Check Status Code**

```python
if response.status_code != 200:
    raise Exception("API request failed")
```


### **2. Handle Errors Gracefully**

* Timeouts
* Invalid responses
* Rate limits


---
hideInToc: true
level: 2
---

### **3. Use Parameters Instead of Hardcoding**

```python
params = {"userId": 1}
requests.get(url, params=params)
```

### **4. Respect Rate Limits**

* Add delays (`time.sleep`)
* Avoid excessive calls

### **5. Secure API Keys**

* Never hardcode credentials
* Use environment variables


---
hideInToc: true
level: 2
---

# **Real-World Use Cases**

* Weather data ingestion
* Stock market analysis
* Social media analytics
* Payment system integrations
* ETL pipelines (Extract → Transform → Load)


---
hideInToc: true
level: 2
---

# **🧠 Quick Summary**

* API = communication bridge between systems
* Use `requests` to fetch data
* Convert JSON → DataFrame using Pandas
* Use `json_normalize()` for nested data
* Handle pagination for large datasets
* Follow best practices for production-ready pipelines
