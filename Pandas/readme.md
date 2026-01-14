

---

#  Pandas Practice and Student Exam Analysis

A hands-on **pandas learning repository** with a mini data analysis project focused on **student study habits and exam performance**.

This project is designed for **beginners to intermediate learners** who want to strengthen their pandas skills using a **realistic CSV dataset**.

---

##  Overview

This repository focuses on:

* **Pandas Fundamentals**
  Working with Series and DataFrames, indexing, filtering, cleaning, and transforming tabular data using real examples.

* **Student Exam Score Analysis**
  Analyzing how **study hours, sleep, attendance, and previous scores** affect exam performance using a structured dataset.

---

## Contents

### Main Notebook

#### `Pandas.ipynb`

[View on GitHub](https://github.com/Ankitmahato-0509/Data-Manipulation/blob/main/Pandas/Pandas.ipynb)

A complete **practice-oriented pandas notebook** covering:

* What pandas is and why it is used
* Difference between pandas and NumPy for tabular data
* Core data structures:

  * **Series** (1D labeled data)
  * **DataFrame** (2D labeled table)
* Creating Series and DataFrames
* Accessing:

  * `.values`
  * `.index`
  * `.columns`
  * `.name`
* Indexing and selection:

  * `[]`
  * `.loc` (label-based)
  * `.iloc` (position-based)
  * Slicing and boolean filtering
* Handling missing data:

  * `isnull`, `notnull`
  * `dropna`
  * `fillna` (mean, forward fill, backward fill)
* Descriptive statistics:

  * `describe`
  * `mean`, `std`, `min`, `max`
  * Quantiles
* Column operations:

  * Creating new columns
  * `apply`
  * `lambda` functions
  * `replace`
* Working with duplicates:

  * `duplicated`
  * `drop_duplicates`
* Combining data:

  * `groupby`
  * `concat`
  * `merge`
* Exporting cleaned data:

  * `to_csv`
  * `to_excel`

---

## Dataset

### `student_exam_scores.csv`

A structured dataset with **200 student records**, used for analysis and practice.

**Columns:**

| Column Name         | Description                          |
| ------------------- | ------------------------------------ |
| `studentid`         | Unique student ID (e.g., S001, S002) |
| `hoursstudied`      | Daily study hours                    |
| `sleephours`        | Daily sleep duration (hours)         |
| `attendancepercent` | Attendance percentage                |
| `previousscores`    | Previous exam scores                 |
| `examscore`         | Current exam score                   |

This dataset is ideal for exploring relationships between **study habits, attendance, and performance**.

---

##  Key Concepts Covered

### 🔹 Pandas Fundamentals

* Labeled data structures for heterogeneous tabular data
* Flexible indexing with `.loc` and `.iloc`
* Efficient data cleaning and transformation workflows

### 🔹 Student Exam Analysis

* Importing CSV files using `pd.read_csv`
* Understanding datasets with:

  * `head()`
  * `tail()`
  * `info()`
* Statistical summaries using `describe()`
* Filtering students based on:

  * Attendance
  * Exam score
  * Previous performance
* Sorting and grouping to identify performance patterns

---

##  Usage Examples

### Load the Dataset

```python
import pandas as pd

df = pd.read_csv("student_exam_scores.csv")

print(df.head())      # First 5 rows
print(df.info())      # Data structure and types
print(df.describe())  # Statistical summary
```

---

### Filter High-Performing Students

```python
# Students with attendance ≥ 80% and exam score ≥ 40
high_perf = df[
    (df["attendancepercent"] >= 80) &
    (df["examscore"] >= 40)
]

print(high_perf.head())
```

---

### Handle Missing Values

```python
# Remove rows where all values are missing
df_clean = df.dropna(how="all")

# Fill missing exam scores with mean value
df["examscore"] = df["examscore"].fillna(df["examscore"].mean())
```

---

##  File Structure

```text
Pandas-Student-Exam-Analysis/
├── README.md
├── Pandas.ipynb
└── student_exam_scores.csv
```

---

## ⚙️ Requirements

* Python **3.8+**
* Jupyter Notebook or JupyterLab
* Required libraries:

  * `pandas`
  * `numpy`

---

## Learning Outcomes

After completing this project, you will be able to:

* Confidently work with **pandas Series and DataFrames**
* Load, inspect, clean, and transform CSV datasets
* Apply boolean filtering and conditional logic
* Generate meaningful statistical insights from real data
* Build a strong foundation for **data analysis and data science projects**

---

 **Last Updated:** January 2026

---


