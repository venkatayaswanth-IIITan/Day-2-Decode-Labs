# 🎓 SGPA to CGPA Prediction Using Linear Regression

🚀 A beginner-friendly Machine Learning project that predicts a student's **CGPA** based on their **SGPA** using the **Linear Regression** algorithm.

📚 This project demonstrates the complete Machine Learning workflow including:

✅ Data Collection  
✅ Data Understanding  
✅ Data Visualization  
✅ Data Preprocessing  
✅ Model Training  
✅ Prediction  
✅ Performance Evaluation  

---

## 🚀 Open in Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1vcCJq7p5PyIetJG4HWZOHfLwl_Uu2WTK?usp=sharing)

---

## 🛠️ Technologies Used

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-purple?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-blue?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Linear%20Regression-orange?logo=scikitlearn)
![Google Colab](https://img.shields.io/badge/Google-Colab-yellow?logo=googlecolab)

---

## 📌 Project Overview

🎯 **Goal:** Predict CGPA from SGPA using Machine Learning.

This project uses a simple Linear Regression model to learn the relationship between Semester Grade Point Average (SGPA) and Cumulative Grade Point Average (CGPA).

---

## 🔄 Project Workflow

```text
📂 Dataset Collection
        ↓
📖 Dataset Understanding
        ↓
🧹 Data Cleaning
        ↓
📊 Data Visualization
        ↓
✂️ Train-Test Split
        ↓
🤖 Linear Regression Model
        ↓
📈 Prediction
        ↓
📋 Model Evaluation
```

---

## 📂 Dataset

The dataset contains academic records of students.

| Column | Description |
|----------|------------|
| SGPA | Semester Grade Point Average |
| CGPA | Cumulative Grade Point Average |

### 📊 Sample Dataset

| SGPA | CGPA |
|------|------|
| 7.2 | 7.20 |
| 7.5 | 7.35 |
| 7.8 | 7.50 |
| 8.0 | 7.62 |
| 8.2 | 7.74 |

---

## 📦 Installation

Install the required libraries using:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## 📚 Import Libraries

```python
import pandas as pd
import numpy as np

import matplotlib.pyplot as plt
import seaborn as sns

from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression

from sklearn.metrics import (
    mean_absolute_error,
    mean_squared_error,
    r2_score
)
```

---

## 📥 Load Dataset

```python
df = pd.read_csv("sgpa_cgpa.csv")
```

---

## 🔍 Dataset Exploration

### View First 5 Rows

```python
print(df.head())
```

### Dataset Shape

```python
print(df.shape)
```

### Dataset Information

```python
print(df.info())
```

### Statistical Summary

```python
print(df.describe())
```

---

## 📊 Data Visualization

### Scatter Plot

```python
plt.scatter(df['SGPA'], df['CGPA'])

plt.xlabel("SGPA")
plt.ylabel("CGPA")

plt.title("SGPA vs CGPA")

plt.show()
```

---

## 🤖 Machine Learning Model

### Define Input and Output

```python
X = df[['SGPA']]
y = df['CGPA']
```

### Train-Test Split

```python
X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
```

### Create Linear Regression Model

```python
model = LinearRegression()
```

### Train Model

```python
model.fit(X_train, y_train)
```

### Predict Values

```python
y_pred = model.predict(X_test)
```

---

## 📈 Model Evaluation

### Mean Absolute Error (MAE)

```python
mae = mean_absolute_error(y_test, y_pred)

print("MAE:", mae)
```

### Mean Squared Error (MSE)

```python
mse = mean_squared_error(y_test, y_pred)

print("MSE:", mse)
```

### Root Mean Squared Error (RMSE)

```python
rmse = np.sqrt(mse)

print("RMSE:", rmse)
```

### R² Score

```python
r2 = r2_score(y_test, y_pred)

print("R² Score:", r2)
```

---

## 🎯 Predict New CGPA

```python
new_sgpa = [[8.5]]

prediction = model.predict(new_sgpa)

print("Predicted CGPA:", prediction[0])
```

---

## 📊 Sample Output

```text
MAE: 0.01

MSE: 0.0002

RMSE: 0.014

R² Score: 0.99

Predicted CGPA: 7.90
```

---

## ✨ Features

🌟 Beginner-Friendly Project

📊 Data Visualization

🤖 Linear Regression Model

📈 CGPA Prediction

📋 Model Evaluation

🎓 Academic Dataset

🚀 Google Colab Ready

💡 Easy to Understand

---

## 📚 Evaluation Metrics Used

✅ Mean Absolute Error (MAE)

✅ Mean Squared Error (MSE)

✅ Root Mean Squared Error (RMSE)

✅ R² Score

---

## 🎓 Learning Outcomes

Through this project, I learned:

📌 Data Loading using Pandas

📌 Data Visualization using Matplotlib

📌 Train-Test Split

📌 Linear Regression

📌 Prediction Techniques

📌 Model Evaluation

📌 Basic Machine Learning Workflow

---

## 🔮 Future Improvements

🚀 Multiple Linear Regression

🚀 More Student Features

🚀 Streamlit Web Application

🚀 Student Performance Dashboard

🚀 CGPA Prediction System

---

## 📁 Project Structure

```text
SGPA-CGPA-Prediction/
│
├── sgpa_cgpa.csv
├── SGPA_CGPA_PredICTION.ipynb
├── README.md
│
└── screenshots/
```

---

## 👨‍💻 Author

### Chatakondu Venkata Yaswanth

🎓 B.Tech Computer Science and Engineering

🏫 IIIT Kottayam

🔗 LinkedIn:
https://www.linkedin.com/in/chatakondu-venkata-yaswanth-8bab82321

💻 GitHub:
https://github.com/YOUR_USERNAME

---

## ⭐ Support

If you found this project useful, please give it a ⭐ on GitHub.

---

## 📜 License

📚 This project is created for educational, learning, and internship purposes.
