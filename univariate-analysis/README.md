# 📊 Understanding Data & Univariate Analysis

## 📌 Overview

This project focuses on understanding the dataset and performing univariate analysis using Python. It involves exploring the structure of the data, identifying data types, handling missing values, and analyzing individual features. Visualization techniques such as count plots, histograms, and bar charts are used to understand the distribution of variables and extract meaningful insights.

---

## 🎯 Objectives

* Understand the dataset structure
* Identify numerical and categorical features
* Handle missing values
* Analyze individual variables
* Visualize data distributions

---

## 🛠️ Tools & Libraries

* Python 🐍
* Pandas
* NumPy
* Matplotlib
* Seaborn

---

## 🔍 Steps Performed

### 1. Data Understanding

* Viewed dataset using `head()` and `tail()`
* Checked data types using `info()`
* Generated statistical summary using `describe()`

---

### 2. Handling Missing Values

* Identified missing values using `isnull().sum()`
* Understood which columns need cleaning

---

### 3. Univariate Analysis

#### 📊 Categorical Data

* Used `value_counts()` to get frequency
* Used `countplot()` for visualization

Example:

```python
sns.countplot(x='Survived', data=df)
plt.show()
```

---

#### 🔢 Numerical Data

* Used histogram to check distribution
* Used boxplot to detect outliers

Example:

```python
df['Age'].hist()
plt.show()
```

---

## 📈 Key Insights

* Distribution of categorical variables can be easily visualized using count plots
* Numerical features help in identifying spread and outliers
* Missing values play an important role in data analysis
* Univariate analysis helps in understanding each feature independently

---

## 🚀 Conclusion

Univariate analysis is an important step in exploratory data analysis (EDA). It helps in understanding the characteristics of individual variables, detecting patterns, and preparing data for further analysis such as bivariate analysis and machine learning models.

---

## 📎 Future Work

* Bivariate Analysis
* Multivariate Analysis
* Feature Engineering
* Model Building

---

## 👩‍💻 Author

* Your Name

---
