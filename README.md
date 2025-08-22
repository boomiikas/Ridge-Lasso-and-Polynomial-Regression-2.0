# 🏡 Ridge Regression – Predicting House Prices

## 📌 Project Overview
This project applies **Ordinary Least Squares (OLS)** and **Ridge Regression** to predict house prices.  
The dataset contains information about house size, bedrooms, bathrooms, distance from the city center, and house age.  

The main goal is to show how **Ridge Regression handles multicollinearity** (highly correlated features) better than OLS.

---

## 📂 Dataset
**Source:** [Google Drive Link](https://drive.google.com/file/d/1FDbOghfF0PbG7F8T1TNjK2U9c0BzDZTJ/view?usp=sharing)  

**Features:**
- `size_m2` → Size of the house (in square meters)  
- `bedrooms` → Number of bedrooms  
- `bathrooms` → Number of bathrooms  
- `distance_city` → Distance to the city center (in km)  
- `age_years` → Age of the house (in years)  

**Target:**
- `price_k` → House price (in thousands)  

---

## ⚙️ Methods Used
1. **OLS (Ordinary Least Squares)**  
   - Minimizes squared errors between actual and predicted values.  
   - Struggles when features are highly correlated.  

2. **Ridge Regression**  
   - Adds a penalty term (\(\alpha \sum \beta^2\)) to shrink coefficients.  
   - Handles **multicollinearity** and prevents unstable coefficients.  

---

## 📊 Results & Comparison
- **OLS:** Coefficients unstable due to high correlation between `size_m2` and `bedrooms`.  
- **Ridge:** Coefficients are smaller, more balanced, and predictions generalize better.  

| Feature        | OLS Coefficient | Ridge Coefficient |
|----------------|-----------------|-------------------|
| size_m2        | High / Unstable | Moderate, stable  |
| bedrooms       | Sometimes negative | Positive & balanced |
| bathrooms      | Reasonable      | Slightly smaller  |
| distance_city  | Negative (expected) | Negative (stable) |
| age_years      | Negative        | Negative (stable) |

- **R² (Goodness of Fit):**  
  - OLS: Good fit on training, may drop on test set (overfitting).  
  - Ridge: More stable across training and test data.  

---

## ✅ Why Ridge is Better Here
- **Handles multicollinearity** between `size_m2` and `bedrooms`.  
- **Improves stability** of coefficients.  
- **Better generalization** on unseen house price data.  

---
