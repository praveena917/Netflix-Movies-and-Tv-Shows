# Netflix Dataset - Data Cleaning & Preprocessing

## Project Overview

This project focuses on cleaning and preprocessing the Netflix Movies and TV Shows dataset using Python and Pandas. The objective was to identify and resolve common data quality issues such as missing values, inconsistent formats, duplicate records, and incorrect data types to prepare the dataset for further analysis and visualization.

---

## Dataset

**Dataset Name:** Netflix Movies and TV Shows

The dataset contains information about Netflix content, including:

* Show ID
* Type (Movie/TV Show)
* Title
* Director
* Cast
* Country
* Date Added
* Release Year
* Rating
* Duration
* Genre
* Description

---

## Objectives

* Identify and handle missing values
* Remove duplicate records
* Standardize text values
* Convert date formats to a consistent type
* Rename column headers
* Verify and fix data types
* Export a clean dataset ready for analysis

---

## Tools Used

* Python
* Pandas
* Jupyter Notebook

---

## Data Cleaning Steps Performed

### 1. Missing Value Treatment

Missing values were identified using:

```python
df.isnull().sum()
```

Actions taken:

* Filled missing values in:

  * director → "Unknown"
  * cast → "Unknown"
  * country → "Unknown"
* Filled missing values in:

  * rating → Mode value
  * duration → Mode value
* Removed records with missing date_added values

---

### 2. Duplicate Removal

Duplicate records were checked using:

```python
df.duplicated().sum()
```

Duplicates were removed using:

```python
df.drop_duplicates()
```

---

### 3. Text Standardization

To ensure consistency across textual fields, leading and trailing spaces were removed from:

* type
* title
* director
* cast
* country
* rating
* listed_in

using:

```python
.str.strip()
```

---

### 4. Date Format Conversion

The date_added column was converted from object datatype to datetime format using:

```python
pd.to_datetime()
```

This ensured a consistent and analysis-ready date format.

---

### 5. Column Name Standardization

Column headers were cleaned by:

* Converting all names to lowercase
* Replacing spaces with underscores

Example:

```text
Date Added → date_added
Release Year → release_year
```

---

### 6. Data Type Validation

Data types were verified using:

```python
df.dtypes
```

The date_added column was converted from object to datetime64[ns] to enable proper date operations and analysis.

---

## Outcome

The dataset was successfully cleaned and transformed into a structured format suitable for:

* Exploratory Data Analysis (EDA)
* Data Visualization
* Dashboard Creation
* Machine Learning Applications

---

## Files Included

* Netflix.ipynb – Jupyter Notebook containing all cleaning steps
* netflix.csv – Original dataset
* cleaned_netflix.csv – Cleaned dataset
* README.md – Project documentation

---

## Key Learnings

Through this project, I gained practical experience in:

* Data Cleaning and Preprocessing
* Handling Missing Values
* Removing Duplicates
* Standardizing Data
* Data Type Conversion
* Working with Pandas
* Preparing Real-World Data for Analysis

---

## Author

Praveena Kamanuru

Aspiring Data Analyst | Python | SQL | Excel | Power BI
