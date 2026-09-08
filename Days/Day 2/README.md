# 🐍 Python Data Analysis – Day 2

## 📌 Day 2: Data Cleaning & Transformation

This is **Day 2** of my Python Data Analysis learning journey.

In this practice, I focused on **Data Cleaning and Transformation using Pandas** in Google Colab.

The main goal was to learn how to inspect a dataset, identify data-quality problems, clean the data, and prepare it for further analysis.

---

## 🎯 Learning Objectives

In Day 2, I practiced how to:

* Load an Excel dataset using Pandas
* Inspect the dataset
* Understand rows and columns
* Check data types
* Identify missing values
* Find duplicate records
* Clean column names
* Remove unnecessary spaces
* Convert data types
* Handle missing values
* Remove unnecessary columns
* Create new columns
* Prepare clean data for analysis

---

## 🛠️ Tools & Technologies

* 🐍 Python
* 📊 Pandas
* 📓 Google Colab
* 📁 Microsoft Excel
* 🔗 GitHub

---

## 📂 Dataset

The dataset was loaded from an Excel file stored in Google Drive.

```python
import pandas as pd

data = pd.read_excel(
    '/content/drive/MyDrive/Colab Notebooks/Marketing-Data-Analysis..xlsx'
)
```

---

## 🔍 Data Inspection

I first inspected the dataset to understand its structure and contents.

Examples of the commands used:

```python
data.head()
```

```python
data.tail()
```

```python
data.shape
```

```python
data.columns.tolist()
```

```python
data.info()
```

```python
data.describe()
```

These commands helped me understand the number of rows, columns, data types, and basic statistics of the dataset.

---

## 🧹 Data Cleaning

### 1. Checking Missing Values

I checked the dataset for missing values using:

```python
data.isnull().sum()
```

This helped me identify which columns contained missing data.

---

### 2. Checking Duplicate Records

I checked for duplicate rows using:

```python
data.duplicated().sum()
```

I also inspected duplicate records:

```python
data[data.duplicated()]
```

If duplicates were unnecessary, I removed them using:

```python
data = data.drop_duplicates()
```

---

### 3. Cleaning Column Names

I cleaned column names by removing unnecessary spaces:

```python
data.columns = data.columns.str.strip()
```

This makes column names easier and safer to use in Python.

---

### 4. Cleaning Text Data

For text columns, unnecessary spaces can be removed using:

```python
text_cols = data.select_dtypes(include='object').columns

data[text_cols] = data[text_cols].apply(
    lambda col: col.str.strip()
)
```

This helps keep categorical data consistent.

---

### 5. Checking Data Types

I checked the data types using:

```python
data.dtypes
```

Understanding data types is important before performing analysis or calculations.

---

### 6. Handling Missing Values

After identifying missing values, I handled them according to the type and meaning of the data.

For example, numerical missing values can sometimes be replaced using the median:

```python
data['Column_Name'] = data['Column_Name'].fillna(
    data['Column_Name'].median()
)
```

> **Note:** The actual column name should be replaced with the correct column from the dataset.

---

### 7. Removing Unnecessary Columns

If a column is not useful for the analysis, it can be removed:

```python
data = data.drop(columns=['Column_Name'])
```

Only unnecessary columns should be removed after checking the dataset.

---

## 🔄 Data Transformation

After cleaning the data, I practiced transforming the dataset into a format that is easier to analyze.

Transformation may include:

* Creating new columns
* Converting data types
* Standardizing text
* Formatting dates
* Calculating new metrics
* Preparing data for visualization

Example:

```python
data['New_Column'] = data['Column1'] / data['Column2']
```

---

## ✅ Final Data Check

After cleaning and transformation, I checked the dataset again:

```python
data.head()
```

```python
data.shape
```

```python
data.isnull().sum()
```

```python
data.duplicated().sum()
```

This helped me confirm that the dataset was ready for the next stage of analysis.

---

## 💾 Saving the Cleaned Dataset

The cleaned dataset can be saved as a new Excel file:

```python
data.to_excel(
    '/content/drive/MyDrive/Colab Notebooks/Marketing-Data-Cleaned.xlsx',
    index=False
)
```

---

## 📚 What I Learned

Through this Day 2 practice, I learned that data cleaning is an important part of Data Analysis.

I learned how to:

* Inspect raw data
* Identify data-quality problems
* Handle missing values
* Remove duplicates
* Clean text
* Check data types
* Transform data
* Prepare a dataset for analysis

---

## 🚀 Next Step

**Day 3 – Exploratory Data Analysis (EDA)**

In Day 3, I will explore the cleaned dataset using:

* Descriptive statistics
* Grouping
* Filtering
* Aggregation
* Data visualization
* Charts and graphs

---

## 👩‍💻 Author

**Nimca Abdirahim Wehliye**

Python Data Analysis Learning Journey

**Day 2 – Data Cleaning & Transformation**

