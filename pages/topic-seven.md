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
