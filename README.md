# Customer Churn Prediction

## 📌 Overview

This project aims to predict whether a customer will leave (churn) from a telecom company using historical customer data. A logistic regression model is trained on structured features and deployed as a Streamlit web application for live predictions.

---

## 🧠 Problem Statement

"Build a prediction model that can help us identify which customers are likely to leave our services."

Customer churn prediction helps the business proactively retain customers by understanding risk factors and acting early.

---

## 🔢 Dataset Features

| Feature Name       | Description                   |
| ------------------ | ----------------------------- |
| `gender`           | Customer gender (Male/Female) |
| `SeniorCitizen`    | 1 if senior, else 0           |
| `Partner`          | Has a partner (Yes/No)        |
| `Dependents`       | Has dependents (Yes/No)       |
| `tenure`           | Months with the company       |
| `PhoneService`     | Has phone service (Yes/No)    |
| `MultipleLines`    | Multiple phone lines          |
| `InternetService`  | DSL/Fiber optic/No            |
| `OnlineSecurity`   | Online security service       |
| `OnlineBackup`     | Online backup service         |
| `DeviceProtection` | Device protection             |
| `TechSupport`      | Tech support service          |
| `StreamingTV`      | Streams TV                    |
| `StreamingMovies`  | Streams movies                |
| `Contract`         | Contract type                 |
| `PaperlessBilling` | Uses paperless billing        |
| `PaymentMethod`    | Mode of payment               |
| `MonthlyCharges`   | Monthly billing amount        |
| `TotalCharges`     | Total billing amount          |
| `Churn`            | Target variable (Yes/No)      |

---

## 🧪 Steps Followed

### 1. Data Loading & Exploration

* Loaded CSV using `pandas`
* Explored dataset shape, types, missing values
* Visualized class balance in `Churn`

### 2. Data Preprocessing

* Converted `Churn` to binary (Yes = 1, No = 0)
* Filled missing values in `TotalCharges`
* Label encoded binary columns
* One-hot encoded categorical columns
* Scaled numeric values (`MonthlyCharges`, `TotalCharges`)
* Split dataset (70% train, 30% test)

### 3. Model Training

* Used `LogisticRegression` from `sklearn`
* Evaluated using Accuracy, F1-score, Precision, Recall, Confusion Matrix
* Saved model using `pickle` as `logistic_model.pkl`

### 4. Streamlit App

* Built `app.py` with input widgets for all features
* Encoded inputs same as training pipeline
* Used trained model to predict and display results with messages

### 5. Deployment

* Created `requirements.txt` with all dependencies
* Deployed on [Streamlit Cloud](https://share.streamlit.io)

---

## 📂 Project Structure

```
customer-churn-prediction/
├── app.py
├── logistic_model.pkl
├── churn_analysis.ipynb
├── requirements.txt
├── README.md
```

---

## 📊 Sample Prediction Output

**Input:**

* Gender: Female
* Contract: Month-to-month
* Tenure: 2
* MonthlyCharges: 70.5

**Output:**
🟡 This customer is likely to churn.

---

## ✅ Requirements

```
pandas
numpy
scikit-learn
streamlit
pickle-mixin
```

---

## 📎 GitHub + Live App

* GitHub Repo: *(Your repo link here)*
* Live App: *(Your Streamlit link here)*
