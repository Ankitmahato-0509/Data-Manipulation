# Data Manipulation : Beginner’s Guide to NumPy & Pandas

Welcome to **Data Manipulation**
This repository is a complete, beginner-friendly guide to data manipulation using **NumPy** and **Pandas** — two of the most essential Python libraries for Data Analysis, Data Science, and Machine Learning.  

Whether you’re new to Python or already familiar with the basics, this guide will help you understand how to **clean, transform, analyze, and prepare data efficiently**.

***

## 📚 Table of Contents
1. [Installation Guide](#installation-guide)  
2. [Introduction to Data Manipulation](#introduction-to-data-manipulation)  
3. [Introduction to NumPy](#introduction-to-numpy)  
4. [NumPy Arrays and Operations](#numpy-arrays-and-operations)  
5. [Indexing, Slicing, and Broadcasting](#indexing-slicing-and-broadcasting)  
6. [Mathematical and Statistical Functions](#mathematical-and-statistical-functions)  
7. [Introduction to Pandas](#introduction-to-pandas)  
8. [Pandas Series and DataFrames](#pandas-series-and-dataframes)  
9. [Data Loading and Exporting](#data-loading-and-exporting)  
10. [Data Cleaning and Preprocessing](#data-cleaning-and-preprocessing)  
11. [Data Filtering and Selection](#data-filtering-and-selection)  
12. [Data Aggregation and Grouping](#data-aggregation-and-grouping)  
13. [Handling Missing Data](#handling-missing-data)  
14. [Merging, Joining, and Concatenation](#merging-joining-and-concatenation)  
15. [Time Series and Categorical Data](#time-series-and-categorical-data)  
16. [Performance Optimization](#performance-optimization)  
17. [Best Practices](#best-practices)  
18. [Recommended Learning Resources](#recommended-learning-resources)  
19. [Exercises and Mini Projects](#exercises-and-mini-projects)  
20. [Conclusion](#conclusion)

***

## ⚙️ Installation Guide

Make sure **Python** is installed on your system.  
Then install **NumPy** and **Pandas** using pip:

```bash
pip install numpy pandas
```

Verify installation:

```bash
python -c "import numpy, pandas; print(numpy.__version__, pandas.__version__)"
```

If versions are displayed without errors — you’re ready to go 

***

##  Introduction to Data Manipulation

Data manipulation involves **cleaning**, **transforming**, **structuring**, and **preparing** data for analysis or machine learning.  

Raw data is often messy or inconsistent. **NumPy** and **Pandas** make it easy to convert that raw data into usable, insightful information.

***

##  Introduction to NumPy

**NumPy (Numerical Python)** is designed for:

- Fast numerical computations  
- Array and matrix operations  
- Mathematical and statistical analysis  

**Why use NumPy?**
- Faster and more efficient than Python lists  
- Uses less memory  
- Optimized for scientific and computational workloads  

***

##  NumPy Arrays and Operations

A NumPy array is a collection of elements of the same type:

```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5])
```

**Common operations:**
- Element-wise addition, subtraction, multiplication  
- Reshaping arrays  
- Matrix operations  

Example:
```python
arr * 2
```

***

##  Indexing, Slicing, and Broadcasting

**Indexing & Slicing**

```python
arr[0]
arr[1:4]
```

**Broadcasting**

Performs operations between arrays of different shapes:

```python
arr + 10
```

***

##  Mathematical and Statistical Functions

NumPy provides many built-in methods for analysis:

```python
np.sum(arr)
np.mean(arr)
np.std(arr)
np.min(arr)
np.max(arr)
```

These are key for performing fast numerical summaries.

***

##  Introduction to Pandas

**Pandas** is built on top of NumPy and focuses on **tabular data management**.  
It’s the go-to tool for **data cleaning**, **analysis**, and **preprocessing**.

### Core Structures
- **Series:** One-dimensional labeled array  
- **DataFrame:** Two-dimensional table  

***

##  Pandas Series and DataFrames

**Series Example:**
```python
import pandas as pd
s = pd.Series([10, 20, 30])
```

**DataFrame Example:**
```python
df = pd.DataFrame({
    "Name": ["A", "B", "C"],
    "Marks": [80, 85, 90]
})
```

***

##  Data Loading and Exporting

**Read Data:**
```python
pd.read_csv("data.csv")
pd.read_excel("data.xlsx")
```

**Write Data:**
```python
df.to_csv("output.csv", index=False)
```

***

##  Data Cleaning and Preprocessing

Real-world data often contains:

- Missing values  
- Duplicates  
- Inconsistent formats  

**Examples:**

```python
df.drop_duplicates()
df.rename(columns={"Marks": "Score"})
```

***

##  Data Filtering and Selection

**Selecting Columns**
```python
df["Score"]
```

**Filtering Rows**
```python
df[df["Score"] > 85]
```

***

##  Data Aggregation and Grouping

Summarize or group data efficiently:

```python
df.groupby("Category")["Sales"].sum()
```

Common functions:
- `sum()`
- `mean()`
- `count()`
- `min()`, `max()`

***

##  Handling Missing Data

**Check Missing Values**
```python
df.isnull().sum()
```

**Fill Missing Values**
```python
df.fillna(0)
```

**Drop Missing Rows**
```python
df.dropna()
```

***

##  Merging, Joining, and Concatenation

**Concatenation**
```python
pd.concat([df1, df2])
```

**Merging (SQL-style JOIN)**
```python
pd.merge(df1, df2, on="id")
```

***

##  Time Series and Categorical Data

**Date Handling**
```python
pd.to_datetime(df["date"])
```

**Categorical Data**
```python
df["category"] = df["category"].astype("category")
```

Helps improve performance and reduce memory usage.

***

##  Performance Optimization

- Use vectorized operations  
- Avoid for-loops when possible  
- Use `category` datatype for labels  
- Work with chunks for large datasets  

Efficient code ensures faster and scalable data analysis.

***

##  Best Practices

- Use clear, meaningful column names  
- Avoid altering raw data directly  
- Add comments for clarity  
- Validate data before analysis  
- Maintain consistent formatting  

***

##  Recommended Learning Resources

**Documentation**
- [NumPy Official Docs](https://numpy.org/doc/)
- [Pandas Official Docs](https://pandas.pydata.org/docs/)

**Online Platforms**
- [Kaggle](https://www.kaggle.com/)
- [W3Schools](https://www.w3schools.com/python/pandas_intro.asp)
- [DataCamp](https://www.datacamp.com/)
- [Coursera](https://www.coursera.org/)

**Practice Sites**
- [HackerRank](https://www.hackerrank.com/)
- [LeetCode](https://leetcode.com/)
- [Kaggle Datasets](https://www.kaggle.com/datasets)

***

##  Exercises and Mini Projects

This repository includes:

- NumPy practice problems  
- Pandas data cleaning exercises  
- CSV-based datasets  

**Mini Projects:**
- Sales analysis 
- Student performance report  
- Data cleaning pipeline  

Practicing regularly will help you master real-world data handling 💪

***

##  Conclusion

Congratulations on completing **Data Manipulation** with **NumPy & Pandas**!  

You now know how to:
- Work with arrays and tables  
- Clean and transform data  
- Prepare datasets for analysis and ML  


***

##Last Updated: January 2026
