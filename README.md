# 📉 Customer Churn Prediction

Predicting whether a customer will churn (leave a service) is crucial for customer retention strategies. In this project, we analyze customer data from a telecom company and build multiple classification models to predict churn based on demographic and service usage features.

## 📁 Dataset Overview

- **Source**: Synthetic telecom customer dataset
- **Target Variable**: `Churn` (Yes/No)
- **Features**:
  - Demographics: `gender`, `SeniorCitizen`, `Partner`, `Dependents`
  - Services: `PhoneService`, `InternetService`, `StreamingTV`, etc.
  - Charges: `MonthlyCharges`, `TotalCharges`, `tenure`

## 🔍 Exploratory Data Analysis (EDA)

Performed detailed EDA to:
- Understand feature distributions (`tenure`, `MonthlyCharges`, `TotalCharges`)
- Visualize Churn vs. numerical features using boxplots
- Check for class imbalance in target variable
- Summarize data types and missing values

## 🧹 Preprocessing

- Converted categorical variables using `LabelEncoder` and `get_dummies`
- Handled missing or non-numeric values in `TotalCharges`
- Scaled numerical features using `StandardScaler`
- Split data into training and testing sets (80:20)

## 🤖 Models Used

### 1️⃣ Logistic Regression
- Simple, interpretable baseline model
- Performance:
  - **Accuracy**: 0.80
  - **F1 Score**: 0.61
  - **AUC**: 0.84

### 2️⃣ Random Forest Classifier
- Ensemble tree-based model
- Used feature importance to identify key variables
- Performance:
  - **Accuracy**: 0.79
  - **F1 Score**: 0.61
  - **AUC**: 0.82

### 3️⃣ XGBoost Classifier
- Gradient boosting model
- Tuned with early stopping and evaluation metrics
- Performance:
  - **Accuracy**: 0.77
  - **F1 Score**: 0.60
  - **AUC**: 0.82

## 📊 Model Comparison

| Model              | Accuracy | F1 Score | AUC  |
|--------------------|----------|----------|------|
| Logistic Regression| 0.80     | 0.61     | 0.84 |
| Random Forest      | 0.79     | 0.61     | 0.82 |
| XGBoost            | 0.77     | 0.60     | 0.82 |

- **Best Performing Model**: Logistic Regression

## 🧠 Business Insight

> Logistic Regression provides the most balanced and interpretable performance. It is suitable for deployment in real-world systems where explainability is crucial for early churn detection.

## 📌 Key Visualizations

- Distribution plots for tenure, charges
- Churn vs. features boxplots
- Confusion matrices for all models
- ROC curves and Precision/Recall comparisons
- Feature importance for Random Forest

## 🛠️ Tech Stack

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Scikit-learn
- XGBoost
- Jupyter Notebook

## ✅ Results Summary

- Logistic Regression outperformed others in terms of AUC and simplicity.
- Ensemble models like Random Forest and XGBoost showed potential but slightly overfitted.
- EDA and feature engineering played a critical role in boosting model performance.

---

> Feel free to fork, star ⭐, or contribute to the project!

