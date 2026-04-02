# **Data Ingestion**

## **1. What is Data Ingestion?**

**Data ingestion** is the process of **collecting and importing data from multiple sources into a system** (like a database, data warehouse, or data lake) for storage, processing, and analysis.

👉 In simple terms:

> Data Ingestion = “Bringing raw data into your system for use”

📌 It involves:

* Collecting data from different sources
* Cleaning and transforming it
* Storing it in a centralized location

---
level: 2
hideInToc: true
---

# **Importance of Data Ingestion**

## **1. Flexibility in a Dynamic Data Environment**

Data ingestion systems are designed to **handle diverse and evolving data ecosystems**.

### Key Points:

* ✔ Supports data from **multiple sources** (APIs, databases, files, streams)
* ✔ Handles **different data formats** (CSV, JSON, XML, etc.)
* ✔ Adapts to **new and changing data sources**
* ✔ Scales with increasing:

  * Data volume
  * Data velocity (speed of incoming data)

👉 Ensures your system remains **scalable, flexible, and future-ready**

---
layout: full
hideInToc: true
---

## **2. Enables Powerful Analytics**

Data ingestion is the **foundation for all analytics and data-driven systems**.

### Key Points:

* ✔ Collects and prepares **large datasets** for analysis
* ✔ Powers:

  * Business Intelligence (BI)
  * Machine Learning models
  * Data dashboards
* ✔ Helps identify:

  * Trends
  * Patterns
  * Insights

👉 Converts raw data → **actionable business decisions**

---
layout: full
hideInToc: true
---

## **3. Improves Data Quality**

A strong ingestion process ensures that only **clean, consistent, and useful data** enters the system.

### Key Points:

###  Data Cleaning

* Removes:

  * Errors
  * Duplicates
  * Irrelevant data

###  Standardization

* Ensures consistent:

  * Formats
  * Units
  * Naming conventions

---
layout: full
hideInToc: true
---

###  Normalization

* Reduces redundancy
* Organizes data efficiently

###  Data Enrichment

* Adds additional context to data
* Example:

  * Adding location info from coordinates
  * Combining datasets

👉 Result: **High-quality, reliable data for analysis**

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

# Types of Data

# **Structured Data**

## **1. Definition**

**Structured data** refers to data that is **organized in a predefined schema (structure)**, making it easy to **store, query, and analyze**.

👉 In simple terms:

> Structured Data = “Data in rows and columns with a fixed format”

---
layout: full
hideInToc: true
---

## **2. How Structured Data Looks**

### **Example Table**

| Customer_ID | Name       | Age | City       | Join_Date  |
| ----------- | ---------- | --- | ---------- | ---------- |
| 101         | Ravi Kumar | 30  | Chennai    | 2023-01-15 |
| 102         | Priya Devi | 27  | Coimbatore | 2023-03-22 |

👉 Each row = one record

👉 Each column = one attribute

---
layout: full
hideInToc: true
---

## **3. Key Components of Structured Data**

### **1. Schema**

* Defines the structure of the data
* Includes:

  * Table name
  * Column names
  * Data types
  * Relationships

👉 Example:

```text
Customer(Customer_ID, Name, Email, Phone)
```

---
layout: full
hideInToc: true
---

### **2. Tables (Relations)**

* Data is stored in **tabular format**
* Consists of:

  * Rows → records
  * Columns → attributes

### **3. Data Types**

Each column has a fixed type:

* Integer → Age, Quantity
* Float/Decimal → Price
* String/Text → Name
* Date/Time → Join_Date

👉 Ensures consistency and validation

---
layout: full
hideInToc: true
---

### **4. Relationships**

* Connects multiple tables

**Types:**

* **Primary Key** → Unique identifier
* **Foreign Key** → Links tables

👉 Enables relational data modeling

---
layout: full
hideInToc: true
---

## **4. Characteristics of Structured Data**

* ✔ **Predefined Schema** → Fixed structure
* ✔ **Highly Organized** → Tabular format
* ✔ **Easy Querying** → Uses SQL
* ✔ **High Data Integrity** → Constraints (NOT NULL, UNIQUE)
* ✔ **Consistency** → Same format across records
* ✔ **Efficient Storage** → Optimized databases
* ✔ **Vertical Scalability** → Scale by upgrading system resources

---
layout: full
hideInToc: true
---

## **5. Advantages of Structured Data**

### **1. Easy Analysis**

* Works well with:

  * BI tools
  * Dashboards
  * Reporting systems


### **2. Fast Query Performance**

* Indexing enables quick data retrieval


### **3. Data Accuracy**

* Constraints reduce errors
* Strong validation rules

---
layout: full
hideInToc: true
---

### **4. Standardization**

* Uniform format across systems
* Easy integration


### **5. Strong Security**

* Access control at:

  * Table level
  * Column level

---
layout: full
hideInToc: true
---

## **6. Disadvantages of Structured Data**

* ❌ **Low Flexibility**

  * Hard to change schema

* ❌ **Schema Dependency**

  * Changes require redesign/migration

* ❌ **Limited for Complex Data**

  * Not suitable for:

    * Images
    * Videos
    * Free text

---
layout: full
hideInToc: true
---

## **7. Common Storage Systems**

### **Relational Databases (RDBMS)**

* MySQL
* PostgreSQL
* Oracle Database
* Microsoft SQL Server

### **Spreadsheet Tools**

* Microsoft Excel
* Google Sheets



---
layout: full
hideInToc: true
---

# **Semi-Structured Data**

## **1. Definition**

**Semi-structured data** is data that **does not follow a strict tabular schema**, but still contains **organizational elements like keys, tags, or metadata** that help in understanding and processing it.

👉 In simple terms:

> Semi-Structured Data = “Flexible data with some structure, but not fixed tables”

📌 It acts as a **middle ground** between structured and unstructured data

---
layout: full
hideInToc: true
---

## **2. Example of Semi-Structured Data**

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

👉 Notice:

* No fixed columns
* Nested (hierarchical) structure
* Flexible fields

---
layout: full
hideInToc: true
---

## **3. Key Components of Semi-Structured Data**

### **1. Keys / Tags**

* Data elements are labeled using identifiers
* Example:

```json
{
  "name": "Ravi",
  "age": 30
}
```


### **2. Hierarchical Structure**

* Data is stored in **nested format (parent-child relationships)**
* Common in:

  * JSON
  * XML

👉 Supports complex relationships

---
layout: full
hideInToc: true
---

### **3. Metadata**

* Provides additional information about data
* Helps systems interpret structure and meaning


### **4. Irregular Fields**

* Different records can have different fields
* Example:

  * One record has `"phone"`
  * Another may not

👉 No strict uniformity

---
layout: full
hideInToc: true
---

## **4. Characteristics of Semi-Structured Data**

* ✔ **No Fixed Schema**

  * Structure can change dynamically

* ✔ **Self-Describing**

  * Uses tags/keys to define data

* ✔ **Flexible & Extensible**

  * New fields can be added anytime

* ✔ **Hierarchical / Nested**

  * Supports complex data relationships

* ✔ **Schema-on-Read**

  * Structure is applied when reading, not storing

---
layout: full
hideInToc: true
---

## **5. Advantages of Semi-Structured Data**

### **1. High Flexibility**

* Adapts easily to changing requirements


### **2. Scalability**

* Works well with large and evolving datasets


### **3. Easier Than Unstructured Data**

* Has some structure → easier to parse and analyze



### **4. Efficient Data Exchange**

* Widely used in:

  * APIs
  * Web applications


### **5. Supports Complex Data**

* Ideal for nested and hierarchical data

---
layout: full
hideInToc: true
---

## **6. Disadvantages of Semi-Structured Data**

* ❌ **Complex Querying**

  * Requires tools like:

    * JSONPath
    * XPath


* ❌ **Lower Performance (vs Structured)**

  * Slower for heavy analytical queries


* ❌ **Data Inconsistency**

  * Missing or varying fields across records


* ❌ **Storage Overhead**

  * Extra tags/metadata increase size

---
layout: full
hideInToc: true
---

## **7. Common Storage Systems**

### **NoSQL Databases**

* MongoDB
* CouchDB
* Firebase

### **Big Data Systems**

* Hadoop
* Apache Spark

### **File Formats**

* JSON
* XML
* YAML
* Avro
* Parquet

---
layout: full
hideInToc: true
---

## **8. Key Points to Remember**

###  No Fixed Schema

Flexible structure

###  Uses Keys/Tags

Self-describing data

###  Supports Nesting

Hierarchical relationships

###  Schema-on-Read

Interpret during usage

---
layout: full
hideInToc: true
---

# **Unstructured Data**

## **1. Definition**

**Unstructured data** refers to data that **does not follow any predefined format or schema**, making it difficult to store, search, and analyze using traditional systems like relational databases.

👉 In simple terms:

> Unstructured Data = “Raw data with no fixed structure”

📌 It can exist in many forms such as text, images, videos, and audio 

---
layout: full
hideInToc: true
---


## **2. Examples of Unstructured Data**

### **Text Data**

* Emails
* PDFs
* Word documents
* Chat messages



### **Media Files**

* Images (JPEG, PNG)
* Videos (MP4, AVI)
* Audio files (MP3, WAV)

👉 Also includes:

* Social media posts
* Logs and sensor data 

---
layout: full
hideInToc: true
---


## **3. Key Components of Unstructured Data**

### **1. Raw Content**

* Data exists in its **original natural form**
* Example: text documents, images


### **2. Limited or No Metadata**

* May lack labels or structure
* Requires tagging or annotation for use

---
layout: full
hideInToc: true
---


### **3. Multiple Formats**

* Includes:

  * Text
  * Audio
  * Video
  * Images


### **4. Context-Dependent Meaning**

* Meaning depends on:

  * Language
  * Context
  * Interpretation

👉 Requires intelligent processing

---
layout: full
hideInToc: true
---


## **4. Characteristics of Unstructured Data**

* ✔ **No Predefined Structure**

  * Cannot be stored in tables

* ✔ **Highly Diverse**

  * Exists in many formats

* ✔ **Difficult to Query**

  * Not easily searchable using SQL

* ✔ **Requires Advanced Processing**

  * Needs transformation for analysis

* ✔ **Large Volume**

  * Makes up **majority of real-world data (~80%)** 
---
layout: full
hideInToc: true
---


## **5. Advantages of Unstructured Data**

### **1. Rich Information**

* Contains deep insights:

  * Customer opinions
  * Behavior patterns

### **2. Real-World Representation**

* Captures natural human communication


### **3. High Flexibility**

* No restrictions on format


### **4. Supports Advanced Analytics**

* Enables:

  * Sentiment analysis
  * Image recognition
  * Speech processing

---
layout: full
hideInToc: true
---


## **6. Disadvantages of Unstructured Data**

* ❌ **Difficult to Analyze**

  * Needs specialized tools

* ❌ **Time-Consuming Processing**

  * Requires cleaning and transformation

* ❌ **Storage Challenges**

  * Large storage requirements

* ❌ **Inconsistency**

  * No uniform format

---
layout: full
hideInToc: true
---


## **7. Technologies Used**

### **1. Natural Language Processing (NLP)**

* Extracts meaning from text

### **2. Machine Learning (ML)**

* Finds patterns and predictions

### **3. Computer Vision**

* Processes images and videos

### **4. Big Data Platforms**

* Hadoop
* Apache Spark

### **5. Search & Indexing Tools**

* Elasticsearch

---
layout: full
hideInToc: true
---


## **8. Key Points to Remember**

###  No Structure

Cannot be stored in tables

###  High Variety

Text, images, audio, video

###  Requires AI/ML

To extract meaningful insights

###  Massive Volume

Dominates real-world data
