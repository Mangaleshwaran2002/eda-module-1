# **Strict Type Casting**

## **1. What is Type Casting?**

Type casting is the process of converting data from one data type to another to ensure compatibility, correctness, and efficiency in operations.

### **Types of Casting**

* **Implicit Casting (Automatic)**

  * Done by pandas or Python automatically
  * Example: int → float when needed

* **Explicit Casting (Manual)**

  * Done by the developer using functions like:

    ```python
    df["Age"] = df["Age"].astype(int)
    ```

---
hideInToc: true
level: 2
---

## **2. Why Type Casting is Critical in Pandas**

In pandas, every column has a **dtype (data type)**, which directly affects:

### **a. Memory Usage**

* Smaller dtypes → less memory
* Example:

  * `int64` → 8 bytes
  * `int8` → 1 byte

👉 Choosing correct dtype can reduce memory drastically

---
hideInToc: true
level: 2
---

### **b. Performance (Speed)**

* Efficient dtypes → faster computation
* Numeric operations run faster on numeric dtypes than `object`

👉 Smaller and optimized dtypes improve processing speed 

### **c. Data Accuracy & Correctness**

* Wrong dtype → wrong results
* Example:

  * `"100"` (string) ≠ `100` (integer)

---
hideInToc: true
level: 2
---

### **d. Compatibility**

* Some operations require specific dtypes:

  * Dates → `datetime`
  * Categories → `category`
  * Numeric → `int/float`

---
hideInToc: true
level: 2
---

## **3. Common Pandas Data Types**

| Type       | Example Use Case                   |
| ---------- | ---------------------------------- |
| `int64`    | Age, Count                         |
| `float64`  | Price, Salary                      |
| `object`   | Mixed / string data                |
| `string`   | Text data (modern alternative)     |
| `bool`     | True/False                         |
| `datetime` | Dates, timestamps                  |
| `category` | Repeated values (e.g., city names) |

---
hideInToc: true
level: 2
---

# **Why Schema Enforcement Helps**

<div>

Schema enforcement means **explicitly defining the structure and data types of your dataset at the time of ingestion**, instead of relying on pandas’ automatic type inference.

</div>

👉 In simple terms:
You **control the data types**, not pandas.


## **Schema Enforcement Example**

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

---
hideInToc: true
level: 2
---

## **Why NOT rely on automatic inference?**

When using:

```python
df = pd.read_csv("data.csv")
```

Pandas performs **type inference**, where it guesses data types based on values.

### Problem:

* Mixed values → wrong dtype (`object`)
* Numbers → sometimes converted to `float`
* Dates → not recognized automatically

👉 Pandas follows a hierarchy for inference (bool → int → float → string → object), which can lead to unintended results 


---
hideInToc: true
level: 2
---

# **Deep Benefits of Schema Enforcement**

## **1. Prevents Incorrect Type Inference**

Without schema:

* `"100"` → object (string)
* `100` → int
* Mixed → object

With schema:

* Always consistent → predictable behavior

👉 Explicit `dtype` ensures correct interpretation of columns

---
hideInToc: true
level: 2
---

## **2. Improves Memory Efficiency**

Correct types = **less memory usage**

Example:

* `int64` → 8 bytes
* `int32` → 4 bytes
* `int8` → 1 byte

👉 Optimizing dtypes can **reduce memory usage significantly** and improve performance

---
hideInToc: true
level: 2
---

## **3. Boosts Performance**

* Numeric operations are faster on proper numeric types
* Avoids runtime conversions

👉 Using appropriate dtypes can **speed up computations and reduce overhead**

---
hideInToc: true
level: 2
---

## **4. Ensures Data Consistency**

Schema enforcement guarantees:

* Same column → same dtype across all loads
* No surprises in downstream processing

Example:

```python
# Without schema
salary → sometimes float, sometimes object ❌

# With schema
salary → always float64 ✅
```

---
hideInToc: true
level: 2
---

## **5. Catches Errors Early (Fail Fast Principle)**

If data is invalid:

```python
dtype={"age": "int32"}
```

And data contains:

```
age = "twenty"
```

👉 Pandas will throw an error immediately

✔ This is GOOD:

* Detects bad data early
* Prevents silent failures later

---
hideInToc: true
level: 2
---

## **6. Improves Pipeline Reliability**

In production systems (ETL pipelines):

* Schema = **contract**
* Data must follow structure

Without schema:

* Pipelines break unexpectedly

With schema:

* Stable, predictable pipelines

---
hideInToc: true
level: 2
---

## **7. Better Integration with Downstream Systems**

* Databases expect fixed schema
* ML models expect consistent types

Schema enforcement ensures:

* Smooth integration
* No type mismatches

---
hideInToc: true
level: 2
---

## **8. Enables Optimization Techniques**

Once schema is enforced, you can:

* Downcast integers (`int64 → int32`)
* Use `category` for repeated values
* Use optimized string types

👉 These optimizations are only reliable when schema is controlled


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

## **1. `astype()` Method (Core Tool)**

The `astype()` method is the **primary mechanism for explicit type conversion in pandas**, used to enforce schema and ensure data consistency.

### **What it actually does**

* Converts a column (or entire DataFrame) to a specified dtype
* Supports:

  * Single dtype
  * Column-wise mapping (dict)

👉 Internally, it **casts underlying NumPy/pandas arrays to a target dtype**

---
transition: fade
level: 2
hideInToc: true
---

### **Example**

```python
import pandas as pd

df = pd.DataFrame({
    "age": ["25", "30", "22"]
})

df["age"] = df["age"].astype(int)
```

### **Advanced Usage**

#### Convert multiple columns

```python
df = df.astype({
    "age": "int32",
    "salary": "float32"
})
```

#### Handle errors safely

```python
df["age"] = df["age"].astype(int, errors="ignore")
```

---
level: 2
hideInToc: true
---

### **Key Insights**

* Ensures **strict schema enforcement**
* Prevents incorrect operations:

  * `"10" + "20"` → `"1020"` ❌
  * `10 + 20` → `30` ✅
* Essential in:

  * ETL pipelines
  * Data cleaning workflows


---
transition: fade
level: 2
hideInToc: true
---

### ⚠️ Common Pitfall

If invalid values exist:

```python
"age" = ["25", "abc"]
```

👉 `astype(int)` → ❌ Error

👉 Solution:

```python
pd.to_numeric(df["age"], errors="coerce")
```

---
level: 2
hideInToc: true
---

## **2. Nullable dtypes (Modern Pandas)**

### **Problem (Old Behavior)**

* Missing values (`NaN`) are **float**
* So:

  ```python
  [1, 2, NaN] → float column ❌
  ```

👉 This breaks:

* IDs
* counts
* integer logic


---
transition: fade
level: 2
hideInToc: true
---

### **Solution: Nullable Types**

```python
df["age"] = df["age"].astype("Int64")
```

### **What’s special?**

* Uses `pd.NA` instead of `NaN`
* Keeps column as integer

👉 Pandas introduced this to **avoid forced float conversion**

---
level: 2
hideInToc: true
---

### **Example**

```python
s = pd.Series([1, 2, None], dtype="Int64")
print(s)
```

```
0       1
1       2
2    <NA>
dtype: Int64
```

---
transition: fade
level: 2
hideInToc: true
---

### **Why It Matters**

* Maintains **type integrity**
* Prevents precision issues
* Supports missing values cleanly

👉 Especially critical for:

* IDs
* transaction counts
* categorical encoding

---
level: 2
hideInToc: true
---

## **3. Category Type (Memory + Performance Optimization)**

### **What is it?**

`category` dtype is designed for **low-cardinality data** (repeated values).

Instead of storing strings repeatedly:

* Stores **unique values once**
* Uses integer codes internally

👉 Pandas implements this via `CategoricalDtype`

---
transition: fade
level: 2
hideInToc: true
---

### **Example**

```python
df["department"] = df["department"].astype("category")
```

<br/>

### **How it works internally**

| Original Data | Stored As |
| ------------- | --------- |
| "HR"          | 0         |
| "IT"          | 1         |
| "HR"          | 0         |

---
level: 2
hideInToc: true
---

### **Advantages**

#### ✅ Memory Optimization

* Huge reduction for repeated strings

#### ✅ Faster Operations

* GroupBy
* Sorting
* Filtering

#### ✅ Better Analytics

* Works well in:

  * aggregations
  * reporting


---
transition: fade
level: 2
hideInToc: true
---

## **Comparison Summary**

| Feature          | `astype()`      | Nullable dtypes         | Category                 |
| ---------------- | --------------- | ----------------------- | ------------------------ |
| Purpose          | Convert types   | Handle missing integers | Optimize repeated values |
| Handles missing  | ❌ (basic)       | ✅ (`<NA>`)              | ✅                        |
| Memory efficient | ⚠️ depends      | ✅                       | ✅ (very high)            |
| Use case         | General casting | IDs, counts             | Repeated labels          |

---
transition: fade
level: 2
hideInToc: true
---

# **Type Casting in Polars**

## **1. Schema Definition on Load (Schema-First Approach)**

Polars strongly encourages defining data types **at the time of data ingestion**, rather than fixing them later. This is known as a **schema-first approach**.

Unlike libraries that rely heavily on automatic type inference, Polars ensures correctness and performance by enforcing types upfront.

---
level: 2
hideInToc: true
---

### **Example**

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

### **Why This Matters**

* Prevents incorrect type inference
* Improves performance (no re-processing later)
* Ensures consistency across pipelines
* Reduces downstream errors


---
transition: fade
level: 2
hideInToc: true
---

## **2. Explicit Casting using `cast()`**

Polars provides the `cast()` method to explicitly convert column data types.

It is designed with **strict validation**, ensuring incorrect conversions are not silently ignored.

### **Single Column Casting**

```python
df = df.with_columns(
    pl.col("age").cast(pl.Int32)
)
```

### **Multiple Column Casting**

```python
df = df.cast({
    "age": pl.Int32,
    "salary": pl.Float32
})
```

### **Key Insight**

* Casting modifies the **underlying data type**
* Uses **high-performance Rust execution engine**
* Essential for **data standardization**


---
transition: fade
level: 2
hideInToc: true
---

## **3. Strict vs Non-Strict Casting**

Polars introduces a powerful `strict` parameter to control casting behavior.

### **Strict Mode (Default)**

```python
pl.col("age").cast(pl.Int32)
```

* Raises an error if conversion fails
* Ensures **data correctness**
* Ideal for production pipelines


---
transition: fade
level: 2
hideInToc: true
---

### **Non-Strict Mode**

```python
df = df.with_columns(
    pl.col("age").cast(pl.Int32, strict=False)
)
```

* Invalid values → converted to `null`
* Prevents pipeline crashes
* Useful for **dirty real-world data**

<br/>

### **When to Use What?**

| Mode           | Use Case                   |
| -------------- | -------------------------- |
| `strict=True`  | Clean, validated datasets  |
| `strict=False` | Messy, real-world datasets |


---
transition: fade
level: 2
hideInToc: true
---

## **4. Handling Real-World Data Issues**

In practical scenarios, data is rarely clean. Columns often contain mixed values like:

```
"123", "N/A", "45.6", "unknown"
```

### **Problem**

* Stored as strings
* Cannot perform numeric operations
* Causes failures during aggregation

### **Solution: Clean + Cast**

```python
df = df.with_columns(
    pl.col("amount")
    .str.replace("N/A", None)
    .cast(pl.Float64, strict=False)
)
```
