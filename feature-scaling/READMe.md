
# 📊 Feature Scaling using MinMax Normalization

## 🔥 Overview

This project demonstrates **Feature Scaling using MinMaxScaler (Normalization)** on a dataset.
The goal is to transform features into a fixed range **[0, 1]** so that machine learning algorithms perform better.

---

## 🧠 Why Feature Scaling?

In real-world datasets:

* Different features have different ranges

  * Example:

    * Alcohol → 11 to 15
    * Malic Acid → 1 to 5

👉 This causes problems for algorithms like:

* KNN
* SVM
* Gradient Descent

Because they depend on **distance calculations**.

---

## ⚙️ What is MinMax Scaling?

MinMaxScaler transforms values using:

[
X_{scaled} = \frac{X - X_{min}}{X_{max} - X_{min}}
]

👉 Output range: **0 to 1**

---

## 🚀 Steps Performed

### 1. Split Data

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    df.drop('Class label', axis=1),
    df['Class label'],
    test_size=0.3,
    random_state=0
)
```

---

### 2. Apply MinMax Scaling

```python
from sklearn.preprocessing import MinMaxScaler

scaler = MinMaxScaler()

# learn parameters from training data
scaler.fit(X_train)

# transform both train and test data
X_train_scaled = scaler.transform(X_train)
X_test_scaled = scaler.transform(X_test)
```

---

### 3. Convert to DataFrame

```python
import pandas as pd

X_train_scaled = pd.DataFrame(X_train_scaled, columns=X_train.columns)
X_test_scaled  = pd.DataFrame(X_test_scaled, columns=X_test.columns)
```

---

### 4. Visualization (Before vs After Scaling)

```python
import matplotlib.pyplot as plt

fig, (ax1, ax2) = plt.subplots(ncols=2, figsize=(12, 5))

ax1.scatter(X_train['Alcohol'], X_train['Malic acid'], c=y_train)
ax1.set_title("Before Scaling")

ax2.scatter(X_train_scaled['Alcohol'], X_train_scaled['Malic acid'], c=y_train)
ax2.set_title("After Scaling")

plt.show()
```

---

## 📊 Key Observations

* Data range changes to **[0, 1]**
* Shape and distribution remain **same**
* Features become **comparable**
* Model performance improves for distance-based algorithms

---

## ⚠️ Important Notes

* Always **fit scaler only on training data**
* Never use test data during fitting → avoids **data leakage**
* Use the same scaler to transform test data

---

## 🧠 Key Takeaway

Feature scaling ensures:

* Fair contribution of all features
* Faster convergence in ML models
* Better performance

---

## 📌 Conclusion

MinMax Normalization is a simple yet powerful preprocessing technique that is essential for many machine learning algorithms.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib

---

