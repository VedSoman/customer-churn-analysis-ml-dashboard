# Customer Churn Analysis & Prediction

## Project Overview

This project focuses on analyzing customer churn behavior and building machine learning models to predict whether a customer will leave (churn) or stay.

The goal is to identify key factors influencing churn and provide actionable insights that can help businesses improve customer retention.

---

## Objectives

* Perform data cleaning and preprocessing
* Conduct exploratory data analysis (EDA)
* Build and evaluate machine learning models
* Identify key factors affecting churn
* Create an interactive Power BI dashboard for business insights

---

## Dataset Information

The dataset contains customer information such as:

* Demographics (gender, partner, dependents)
* Account details (tenure, contract type)
* Services (internet, streaming, security)
* Billing (monthly charges, total charges)
* Target variable: **Churn (Yes/No)**

---

## Data Preprocessing

* Handled missing values in `TotalCharges`
* Converted data types from object → numeric
* Removed irrelevant column (`customerID`)
* Performed One-Hot Encoding for categorical features
* Converted boolean values to numeric (0/1)

---

## Exploratory Data Analysis (EDA)

### Key Insights:

* Customers with **month-to-month contracts** have the highest churn
* Customers with **low tenure (new customers)** are more likely to churn
* **Higher monthly charges** increase churn probability
* Customers with **long-term contracts** are more stable

---

## Machine Learning Models

### 1. Logistic Regression

* Initial model showed good accuracy (~79%)
* Struggled with identifying churn customers (low recall)

### 2. Improved Logistic Regression

* Applied `class_weight='balanced'`
* Improved churn detection significantly
* Recall increased from **52% → 79%**

### 3. Support Vector Machine (SVM)

* Achieved highest recall (~83%)
* Best model for detecting churn customers

---

## Model Evaluation Metrics

* Accuracy
* Confusion Matrix
* Precision, Recall, F1-score

### Important Finding:

> Recall is more important than accuracy in churn prediction because missing a churn customer leads to business loss.

---

## Feature Importance

Top factors influencing churn:

* **Tenure** (most important)
* **Contract Type**
* **Monthly Charges**
* **Internet Service (Fiber Optic)**

---

## Power BI Dashboard

An interactive dashboard was created to visualize churn insights:

### Dashboard Features:

* KPI Cards (Total Customers, Churn Count, Churn Rate)
* Churn Distribution (Pie Chart)
* Churn by Contract Type
* Churn by Tenure Group
* Churn by Charges Group
* Internet Service Impact
* Interactive Filters (Gender, Contract, Service)

---

## Business Insights

* Focus on improving **early customer experience**
* Encourage **long-term contracts**
* Review pricing for **high-paying customers**
* Target high-risk customers using predictive models

---

## Tools & Technologies Used

* **Python** (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)
* **Machine Learning** (Logistic Regression, SVM)
* **Power BI** (Dashboard & Visualization)
* **Statistics & Data Analysis**

---

## Project Structure

```bash
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_model_building.ipynb
│   ├── cleaned_churn.csv
│   ├── churn_cleaned_readable.csv
├── output images/
│   ├── Data cleaning images/
│       ├── Churn VS 1 year Contract
│       ├── Churn VS 2 year Contract
│       ├── Customer churn Distribution chart
│       ├── Monthly charges VS Churn
│       ├── Tenure VS Churn
│   ├── Model building images/
│       ├── Confusion matrix Heatmap
│       ├── Top 10 Important features
├── PowerBI file/
│   ├── churn_dashboard.pbix
│
└── README.md
```

---

## Conclusion

This project demonstrates an end-to-end data analytics workflow:

* Data Cleaning
* Data Analysis
* Machine Learning
* Business Insights
* Dashboard Visualization

It highlights how data-driven approaches can help businesses reduce customer churn and improve decision-making.

---

## If you found this project useful, consider giving it a star!
