# 🚢 Titanic Dataset – Data Cleaning & Preprocessing

This project focuses on cleaning and preprocessing the **Titanic dataset** using Python. The notebook demonstrates common data preprocessing techniques required before applying machine learning models.

The complete implementation is available in the Jupyter Notebook [`Task1.ipynb`](Task1.ipynb).

---

## 🎯 Objectives

- Explore and understand the dataset
- Identify and handle missing values
- Convert categorical data into numerical form
- Detect and remove outliers
- Standardize numerical features
- Visualize important patterns in the dataset
- Prepare the dataset for machine learning

---

## 📊 Dataset

The **Titanic dataset** contains information about passengers aboard the RMS Titanic, including:

- Passenger class
- Gender
- Age
- Number of siblings/spouses
- Number of parents/children
- Ticket information
- Fare
- Port of embarkation
- Survival status

The dataset used in this project is the **Titanic-Dataset.csv** from Kaggle.

---

## 🛠️ Technologies Used

- **Python**
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical operations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical visualization
- **Scikit-learn** – Feature standardization

---

## 🔄 Data Preprocessing Steps

### 1. Dataset Exploration

The dataset was explored using:

- `head()`
- `shape`
- `info()`
- `describe()`
- Missing-value analysis

The original dataset contains **891 rows and 12 columns**.

---

### 2. Handling Missing Values

Missing values were handled using appropriate techniques:

- **Age** → Missing values replaced using the median
- **Embarked** → Missing values replaced using the mode
- **Cabin** → Removed because it contains a large number of missing values

---

### 3. Categorical Encoding

Categorical variables were converted into numerical form:

- `Sex` → Male = 0, Female = 1
- `Embarked` → One-hot encoded

Unnecessary columns such as `Name` and `Ticket` were removed from the dataset.

`PassengerId` was also removed because it is an identifier rather than a useful predictive feature.

---

### 4. Outlier Detection

Outliers were visualized using **boxplots**.

The **Interquartile Range (IQR)** method was used to identify and remove extreme values from continuous numerical features such as:

- Age
- Fare

---

### 5. Feature Standardization

Numerical features were standardized using `StandardScaler` from Scikit-learn.

The following features were standardized:

- Age
- Fare
- SibSp
- Parch

Standardization transforms the features so that they have approximately:

- Mean = 0
- Standard deviation = 1

---

## 📈 Visualizations

The project includes visualizations such as:

- Boxplots for detecting outliers
- Survival rate by gender
- Overall passenger survival distribution

These visualizations help understand patterns and relationships within the dataset.

---

## 📁 Project Structure

```text
Task1/
├── README.md
└── Task1.ipynb
