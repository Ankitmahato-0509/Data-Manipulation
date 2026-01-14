# NumPy Practice and Mini Data Projects

A collection of NumPy learning materials and small data analysis projects using NYC taxi and ice-cream sales datasets.

---

## Overview

This repository focuses on:

* **NumPy Fundamentals**: Array creation, indexing, operations, performance
* **Taxi Trip Analysis**: Basic analytics on NYC taxi rides (speed, tips, airport drop-offs)
* **Ice-Cream Sales Analysis**: Exploring how weather, price, tourists and rain affect ice-cream sales

---

## Contents

## Main Notebooks

### 1. Numpy.ipynb

[View on GitHub](https://github.com/Ankitmahato-0509/Libraries-in-Python/blob/main/Numpy/Numpy.ipynb)

* Comprehensive NumPy tutorial and practice notebook
* Covers:

  * Why NumPy is faster and more memory-efficient than Python lists (contiguous memory, vectorization)
  * Array creation functions: `array`, `zeros`, `ones`, `full`, `empty`, `arange`, `linspace`, `logspace`, `eye`, `identity`
  * Array properties: `shape`, `ndim`, `size`, `dtype`, `nbytes`, `itemsize`
  * Reshaping and layout: `reshape`, `resize`, `ravel`, `flatten`, transpose, `swapaxes`
  * Indexing and slicing: 1D/2D/3D indexing, negative indices, boolean and fancy indexing, `np.take`
  * Iteration helpers: `np.nditer`, `np.ndenumerate`, `flat` iterator
  * Arithmetic and ufuncs: `add`, `subtract`, `multiply`, division variants, power, `sqrt`, `exp`, `sin` (with `np.radians`)
  * Aggregations: `sum`, `mean`, `max`, `min`, `std`, `cumsum`, `cumprod`
  * Random number generation: `rand`, `randn`, `randint`, `default_rng`
  * Views vs copies, saving and loading arrays using `np.savetxt` and `np.loadtxt`

---

### 2. Airport-Cabs.ipynb

[View on GitHub](https://github.com/Ankitmahato-0509/Libraries-in-Python/blob/main/Numpy/Airport%20Cabs.ipynb)

* Mini NumPy project analyzing NYC taxi trip data from `nyc_taxis.csv`
* Highlights:

  * Loads CSV using `numpy.genfromtxt` with named columns
  * Computes average speed as
    **speed = tripdistance / triplength × 3600 (mph)**
  * Counts:

    * Number of rides in February using the `pickupmonth` column
    * Trips with tip amount greater than $50
    * Drop-offs at JFK airport using `dropofflocationcode == 2`

---

### 3. Ice-cream-sales-analysis-temperature-and-weather.ipynb

[View on GitHub](https://github.com/Ankitmahato-0509/Libraries-in-Python/blob/main/Numpy/Ice%20cream%20sales%20analysis%20-%20temperature%20and%20weather.ipynb)

* NumPy and pandas analysis of ice-cream sales vs temperature, price, tourists and rain
* Highlights:

  * Loads data using `np.genfromtxt` and `pandas.read_csv`
  * Splits columns into:

    * Temperature (°F)
    * Ice-cream price
    * Number of tourists (thousands)
    * Ice-cream sales (thousands)
    * Rain indicator (Yes/No)
  * Prints a formatted tabular view of the dataset
  * Computes descriptive statistics:

    * Mean, median, maximum and standard deviation
  * Correlation analysis:

    * Temperature vs price
    * Price vs sales
    * Tourists vs sales (strong positive correlation ≈ 0.93)
  * Time-series style insights:

    * Daily sales trend using `np.diff`
    * Sales variation using standard deviation
    * Outlier detection using mean ± 2×std

---

## Data Files

### 1. nyc_taxis.csv

* NYC taxi trip dataset
* Contains columns such as:

  * Pickup date and time fields
  * Pickup and drop-off location codes
  * Trip distance and trip duration
  * Fare, fees, tolls, tips and total amount
  * Payment type
* Used in `Airport-Cabs.ipynb` for speed, month-wise and tip-based analysis

---

### 2. Icecream-Sales-wr-Rain-and-Temperature.csv

* Small synthetic dataset with 20 rows
* Columns:

  * Temperature (Fahrenheit)
  * Ice-cream price
  * Number of tourists (thousands)
  * Ice-cream sales (thousands)
  * Rain indicator
* Used for correlation and trend analysis

---

## Key Concepts

### NumPy Fundamentals

* Speed and memory advantages over Python lists
* Homogeneous multi-dimensional arrays (`ndarray`)
* Broadcasting, reshaping and vectorized computation

### Taxi Data Analysis

* Loading structured CSV files with `numpy.genfromtxt`
* Boolean masking for filtering data
* Deriving real-world metrics like speed and airport drop-offs

### Ice-Cream Sales Analysis

* Separating dataset columns into individual NumPy arrays
* Descriptive statistics and correlation analysis
* Trend detection and outlier identification

---

## Usage Examples

### Loading NYC Taxi Data

```python
import numpy as np

taxi_data = np.genfromtxt(
    "nyc_taxis.csv",
    delimiter=",",
    names=True,
    dtype=None,
    encoding=None
)

speed = taxi_data["tripdistance"] / taxi_data["triplength"] * 3600
average_speed = np.mean(speed)

feb_rides = taxi_data[taxi_data["pickupmonth"] == 2]
high_tip_rides = taxi_data[taxi_data["tipamount"] > 50]
```

---

### Ice-Cream Statistics with NumPy

```python
import numpy as np

data = np.genfromtxt(
    "Icecream-Sales-wr-Rain-and-Temperature.csv",
    delimiter=",",
    skip_header=1
)

temperatures = data[:, 0]
prices = data[:, 1]
tourists = data[:, 2]
sales = data[:, 3]

avg_temp = np.mean(temperatures)
avg_sales = np.mean(sales)
tourist_sales_corr = np.corrcoef(tourists, sales)[0, 1]
```

---

### Reading CSV with pandas

```python
import pandas as pd

df = pd.read_csv("Icecream-Sales-wr-Rain-and-Temperature.csv")
print(df.head())
```

---

## File Structure

```text
NumPy-Projects/
├── README.md
├── Numpy.ipynb
├── Airport-Cabs.ipynb
├── Ice-cream-sales-analysis-temperature-and-weather.ipynb
├── nyc_taxis.csv
└── Icecream-Sales-wr-Rain-and-Temperature.csv
```

---

## Requirements

* Python 3.8 or higher
* Jupyter Notebook or JupyterLab
* Libraries:

  * `numpy`
  * `pandas`

---

## Learning Outcomes

After completing this repository, you will be able to:

* Understand and apply core NumPy concepts
* Perform efficient numerical computations
* Load and analyze real-world datasets
* Use boolean masking for practical data queries
* Identify trends and outliers in small datasets

---

**Last Updated:** January 2026

---
