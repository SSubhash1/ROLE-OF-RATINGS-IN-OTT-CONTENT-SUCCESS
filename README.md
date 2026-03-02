# 🎬 IMDb Top 1000 – Movie Rating Prediction

## 📌 Project Overview

This project predicts IMDb movie ratings using Machine Learning regression models.  
The dataset used is the **IMDb Top 1000 Movies Dataset**, and additional feature engineering was performed using sentiment analysis on movie descriptions.

The goal is to compare multiple regression models and evaluate their prediction performance.

---

## 📂 Dataset

- **File Name:** imdb_top_1000.csv  
- **Target Variable:** IMDb Rating  

### Features Used:
- Genre  
- Runtime  
- Votes  
- Gross  
- Director  
- Star Cast  
- Overview (used for sentiment analysis)

---

## ⚙️ Feature Engineering

- Extracted sentiment polarity from movie descriptions using **TextBlob**
- Converted categorical features into numerical format
- Handled missing values
- Applied feature scaling using **StandardScaler**

Example:

```python
from textblob import TextBlob

df["Sentiment"] = df["Overview"].apply(lambda x: TextBlob(str(x)).sentiment.polarity)
```

---

## 🤖 Machine Learning Models Used

### 1️⃣ Random Forest Regressor
- Ensemble learning technique
- Handles non-linearity effectively
- Strong overall performance

### 2️⃣ Decision Tree Regressor
- Tree-based regression model
- Easy to interpret
- Fast training

### 3️⃣ Support Vector Regressor (SVR)
- Effective in high-dimensional spaces
- Requires feature scaling
- Suitable for structured datasets

---

## 📊 Model Evaluation Metrics

The models were evaluated using:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- R² Score

Example:

```python
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score

mae = mean_absolute_error(y_test, y_pred)
mse = mean_squared_error(y_test, y_pred)
r2 = r2_score(y_test, y_pred)
```

---

## 🛠️ Technologies & Libraries Used

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- TextBlob  

---

## 🚀 Project Workflow

1. Data Collection  
2. Data Cleaning & Preprocessing  
3. Sentiment Feature Extraction  
4. Feature Scaling  
5. Train-Test Split  
6. Model Training  
7. Model Evaluation  
8. Performance Comparison  

---

## 📈 Objective

To analyze and compare regression models for predicting IMDb ratings and identify the most accurate model.

---

## 🔮 Future Improvements

- Hyperparameter tuning using GridSearchCV  
- Advanced feature selection techniques  
- Model deployment using Flask or Streamlit  
- Interactive dashboard visualization  

---
