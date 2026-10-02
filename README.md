# Titanic Dataset – Data Cleaning & Preprocessing

## Overview

This project focuses on cleaning and preparing the Titanic dataset for machine learning.

The dataset is processed using Python and common data science libraries to handle missing values, categorical variables, outliers, and feature scaling.

## Objective

The main objectives are to:

- Explore and understand the dataset
- Identify and handle missing values
- Convert categorical data into numerical form
- Detect and handle outliers
- Standardize numerical features
- Prepare the dataset for machine learning

## Dataset

The Titanic dataset contains information about passengers aboard the Titanic, including:

- Passenger class
- Gender
- Age
- Number of siblings/spouses
- Number of parents/children
- Ticket fare
- Port of embarkation
- Survival status

Dataset source:

[Kaggle – Titanic Dataset](https://www.kaggle.com/datasets/yasserh/titanic-dataset)

## Technologies & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## Data Preprocessing

### 1. Dataset Exploration

- Loaded the dataset using Pandas
- Examined the dataset structure
- Checked data types
- Identified missing values
- Generated statistical summaries

### 2. Missing Value Handling

- Missing `Age` values were replaced using the median.
- Missing `Embarked` values were replaced using the mode.
- The `Cabin` column was removed due to a large proportion of missing values.

### 3. Categorical Encoding

- `Sex` was converted into numerical values:
  - Male → 0
  - Female → 1
- `Embarked` was converted into numerical features using one-hot encoding.

### 4. Feature Cleaning

The following unnecessary columns were removed:

- `PassengerId`
- `Name`
- `Ticket`

### 5. Outlier Detection

Boxplots were used to visualize potential outliers.

The IQR (Interquartile Range) method was used to detect and remove outliers from continuous numerical features.

### 6. Feature Scaling

Numerical features were standardized using `StandardScaler` from Scikit-learn.

The standardized features have approximately:

- Mean = 0
- Standard deviation = 1

## Project Structure

```text
Titanic-Data-Cleaning/
│
├── Task_1_Data_Cleaning.ipynb
├── Titanic_Cleaned.csv
└── README.md
