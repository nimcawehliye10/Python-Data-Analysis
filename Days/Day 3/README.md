# Day 3 - Python Data Analysis

## Overview

On Day 3, I practiced using **Pandas** in Python to explore, inspect, and prepare a marketing dataset for data analysis.

## Topics Covered

* Importing Pandas
* Reading Excel files using `pd.read_excel()`
* Viewing the first rows using `head()`
* Viewing the last rows using `tail()`
* Selecting a random sample using `sample()`
* Checking dataset size using `shape`
* Checking column names using `columns`
* Checking data types using `dtypes`
* Inspecting dataset information using `info()`
* Generating descriptive statistics using `describe()`
* Detecting missing values using `isnull()`
* Detecting duplicate rows using `duplicated()`
* Finding rows containing missing values
* Renaming columns using `rename()`
* Converting columns to appropriate data types
* Converting dates using `pd.to_datetime()`
* Converting numeric values using `pd.to_numeric()`

## Dataset

The dataset used in this practice was a **Marketing Campaign dataset** containing:

* Campaign_ID
* Start_Date
* Channel
* Region
* Budget
* Leads
* Conversions

## Data Quality Checks

During the exploration of the dataset, I checked:

* Missing values
* Duplicate records
* Column names
* Data types
* Dataset dimensions
* Descriptive statistics

The dataset contained **301 rows and 7 columns** after loading the Marketing dataset.

I identified missing values and **7 duplicate rows** during the data quality check.

## Data Type Conversion

I practiced converting columns into appropriate data types:

```python
data['Start_Date'] = pd.to_datetime(data['Start_Date'], errors='coerce')
```

```python
data['Budget'] = pd.to_numeric(data['Budget'], errors='coerce')
```

## Main Pandas Functions Practiced

```python
data.head()
data.tail()
data.sample()
data.shape
data.columns
data.dtypes
data.info()
data.describe()
data.isnull().sum()
data.duplicated().sum()
data[data.isnull().any(axis=1)]
data.rename()
pd.to_datetime()
pd.to_numeric()
```

## What I Learned

In Day 3, I learned how to use Pandas to inspect and understand a dataset before performing analysis. I also learned how to identify missing values and duplicate rows, rename columns, and convert data into appropriate data types.

## Tools Used

* Python
* Google Colab
* Pandas
* Excel
* Jupyter Notebook
