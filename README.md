# 🏦 Bank Customer Churn Prediction

## 📌 Project Overview

Customer churn is a critical challenge in the banking industry, as retaining existing customers is often more cost-effective than acquiring new ones. This project leverages Machine Learning to identify customers who are likely to leave the bank, enabling proactive retention strategies.

The solution includes data exploration, feature engineering, model training, evaluation, and deployment through an interactive Streamlit application.

---

## 🎯 Objectives

- Predict whether a customer will churn or remain with the bank.
- Identify key factors influencing customer retention.
- Build a highly accurate and interpretable machine learning model.
- Deploy the model for real-time predictions.

---

## 📊 Dataset Information

The dataset contains customer information such as:

- Credit Score
- Geography
- Gender
- Age
- Tenure
- Balance
- Number of Products
- Has Credit Card
- Is Active Member
- Estimated Salary

### Target Variable

| Value | Meaning |
|---------|---------|
| 0 | Customer Stays |
| 1 | Customer Churns |

---

## 🔍 Exploratory Data Analysis (EDA)

Performed comprehensive EDA to understand customer behavior and data patterns:

- Distribution analysis of numerical and categorical features
- Correlation analysis
- Churn distribution analysis
- Missing value inspection
- Outlier detection and treatment

### Outlier Handling

Applied the **Interquartile Range (IQR)** method to detect and cap outliers in:

- Age
- CreditScore
- NumOfProducts

---

## ⚙️ Feature Engineering

Created new features to improve model performance:

### Engineered Features

- `balance_per_num_prod`
- `credit_score_per_age`
- `age_group`
- `Tenure_bucket`

These features helped capture customer behavior and financial patterns more effectively.

---

## 🛠 Data Preprocessing

Implemented an automated preprocessing pipeline using:

### Numerical Features

- SimpleImputer
- StandardScaler

### Categorical Features

- SimpleImputer
- OneHotEncoder

### Pipeline Components

```python
ColumnTransformer
Pipeline
StandardScaler
OneHotEncoder
SimpleImputer
```

This ensures consistency between training and deployment.

---

## 🤖 Machine Learning Models Evaluated

The following algorithms were compared:

- Logistic Regression
- Random Forest Classifier
- Gradient Boosting Classifier
- AdaBoost Classifier
- Support Vector Machine (SVM)

### Evaluation Method

- Stratified K-Fold Cross Validation
- ROC-AUC Score

---

## 🏆 Best Model

### Random Forest Classifier

Performance:

| Metric | Score |
|----------|---------|
| ROC-AUC | 0.9996 |
| Model Type | Random Forest |
| Validation Method | Stratified K-Fold CV |

The Random Forest model achieved the highest predictive performance and was selected as the final model.

---

## 📈 Results

- ROC-AUC Score: **0.9996**
- Strong predictive performance on unseen data
- Robust handling of class imbalance
- Highly interpretable customer churn predictions

---

## 🚀 Deployment

The trained model was deployed using **Streamlit**.

### Features

- User-friendly interface
- Real-time churn prediction
- Instant probability estimation
- Easy customer retention analysis

### User Input

Users can enter:

- Age
- Credit Score
- Balance
- Tenure
- Geography
- Gender
- Number of Products
- Active Membership Status

and receive an instant churn prediction.

---

## 🧰 Technologies Used

### Programming Language

- Python

### Data Analysis

- Pandas
- NumPy

### Visualization

- Matplotlib
- Seaborn

### Machine Learning

- Scikit-learn

### Deployment

- Streamlit

### Model Persistence

- Joblib

---

## 📁 Project Structure

```text
Bank-Customer-Churn-Prediction/
│
├── data/
│   └── churn.csv
│
├── notebooks/
│   └── churn_prediction.ipynb
│
├── models/
│   ├── churn_model.pkl
│   └── preprocessor.pkl
│
├── app.py
├── requirements.txt
├── README.md
│
└── assets/
```

---

## 🔮 Future Improvements

- XGBoost and LightGBM implementation
- Hyperparameter optimization
- Explainable AI using SHAP
- Cloud deployment (AWS/GCP/Azure)
- Customer retention recommendation engine

---

## 📌 Business Impact

This solution helps banks:

- Identify high-risk customers
- Reduce customer attrition
- Improve retention campaigns
- Increase customer lifetime value
- Support data-driven decision-making

---

## 👨‍💻 Author

**Dev Sah**

Aspiring Data Scientist | Machine Learning Enthusiast

### Skills

- Python
- Machine Learning
- Data Science
- SQL
- Deep Learning
- Data Visualization

---

⭐ If you found this project useful, consider giving it a star on GitHub.
