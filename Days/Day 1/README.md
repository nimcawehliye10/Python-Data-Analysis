# 📊 Day 01 – Python Data Analysis

## 📚 Overview

Today I started learning **Python for Data Analysis** using the **Pandas** library.

I practiced loading an Excel dataset into Python and performing basic data exploration.

---

## 🛠️ Tools & Library

* Python
* Google Colab
* Pandas
* Excel dataset

---

## 📖 Topics Covered

### 1. Import Pandas

I learned how to import the Pandas library using the alias `pd`.

```python
import pandas as pd
```

### 2. Read Excel Data

I learned how to load an Excel file into a Pandas DataFrame.

```python
data = pd.read_excel(
    "Marketing-Data-Analysis..xlsx",
    header=1
)
```

### 3. View the First Rows

I used `head()` to display the first five rows of the dataset.

```python
data.head()
```

I also practiced displaying the first 10 rows:

```python
data.head(10)
```

### 4. View the Last Rows

I used `tail()` to display the last five rows.

```python
data.tail()
```

### 5. Select a Random Row

I used `sample()` to display a random row from the dataset.

```python
data.sample()
```

### 6. Check Dataset Columns

I used `columns` to view the column names.

```python
data.columns
```

### 7. Check Data Types

I used `dtypes` to check the data type of each column.

```python
data.dtypes
```

### 8. Check Dataset Information

I used `info()` to understand the structure of the dataset, including:

* Number of rows
* Number of columns
* Non-null values
* Data types
* Memory usage

```python
data.info()
```

### 9. Descriptive Statistics

I used `describe()` to generate statistical information about the dataset.

```python
data.describe()
```

I also learned how to include all columns:

```python
data.describe(include="all")
```

### 10. Check Missing Values

I used `isnull().sum()` to identify missing values in each column.

```python
data.isnull().sum()
```

### 11. Check Duplicate Rows

I used `duplicated().sum()` to find duplicate rows.

```python
data.duplicated().sum()
```

The dataset contained **7 duplicate rows**.

---

## 🔍 Data Quality Check

During the initial exploration, I checked:

| Check               | Method                    |
| ------------------- | ------------------------- |
| First rows          | `data.head()`             |
| Last rows           | `data.tail()`             |
| Random row          | `data.sample()`           |
| Columns             | `data.columns`            |
| Data types          | `data.dtypes`             |
| Dataset information | `data.info()`             |
| Statistics          | `data.describe()`         |
| Missing values      | `data.isnull().sum()`     |
| Duplicate rows      | `data.duplicated().sum()` |

---

## 📸 Screenshots

The `screenshots` folder contains screenshots from my Google Colab practice and today's Python Data Analysis lesson.

---

## 🎯 What I Learned

By the end of Day 01, I learned how to:

* Import Pandas
* Read Excel files using Pandas
* Display the first and last rows
* View random data
* Check column names
* Check data types
* Understand dataset information
* Generate descriptive statistics
* Identify missing values
* Identify duplicate rows

---

## 🚀 Next Step

Continue learning Python Data Analysis and practice more Pandas functions.

**Day 01 completed ✅**
