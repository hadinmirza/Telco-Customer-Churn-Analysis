# 📞 Telco Customer Churn Analysis using Machine Learning

## 📌 Project Overview

This project is an end-to-end Machine Learning classification project that predicts whether a telecommunications customer is likely to churn based on their demographic information, subscribed services, account details, and billing history.

The project follows a complete Machine Learning workflow, beginning with business understanding and data exploration, followed by data cleaning, feature engineering, feature selection, model building, and evaluation. It was developed as part of an AI/ML learning assignment to demonstrate practical implementation of the concepts covered during training.

---

# 🎯 Problem Statement

Customer churn is one of the biggest challenges faced by telecommunication companies. Losing existing customers increases acquisition costs and directly impacts revenue.

The objective of this project is to analyze customer behavior, identify the factors associated with churn, and build a Machine Learning model that predicts whether a customer is likely to leave the company.

---

# ❓Business Question

**Can we accurately predict whether a customer will churn using their demographic information, subscribed services, contract details, and billing history?**

---

# 📊 Problem Type

**Binary Classification**

The target variable (`Churn`) has two possible classes (**Yes** and **No**), making this a supervised binary classification problem.

---

# 📂 Dataset Information

* **Source:** Kaggle
* **Dataset:** Telco Customer Churn

**Original Dataset**

* 7,043 rows
* 21 columns

After Feature Engineering

* 7,043 rows
* 27 columns

Final Dataset Used for Modeling

* 7,043 rows
* 26 features (after removing `customerID`)

The dataset contains customer demographics, subscribed services, contract details, payment information, billing history, and customer churn status.

---

# 🎯 Target Variable

Churn

The goal of the model is to predict whether a customer will leave the company.

---

# 🛠 Project Workflow

### 1. Business Understanding

* Defined the business problem
* Identified the prediction objective
* Selected the target variable
* Determined the problem type

---

### 2. Data Understanding

Performed initial data exploration by examining:

* Dataset dimensions
* Column names
* Data types
* Summary statistics
* Missing values
* Unique values
* Target variable distribution

---

### 3. Data Quality Assessment

The dataset was inspected for common quality issues.

Findings:

* No duplicate records were found.
* No invalid categorical values were identified.
* `TotalCharges` was stored as an object instead of a numeric data type.
* Eleven hidden missing values (blank strings) were found in the `TotalCharges` column.

---

### 4. Data Cleaning

The following preprocessing steps were performed:

* Converted `TotalCharges` to numeric.
* Replaced hidden missing values with `0`.
* Verified duplicate records.
* Checked numerical outliers.
* Prepared a clean dataset for modeling.

---

### 5. Exploratory Data Analysis (EDA)

EDA was performed to understand customer behavior and identify important churn patterns.

Examples include:

* Churn distribution
* Customer tenure analysis
* Monthly charges distribution
* Correlation analysis
* Feature relationships
* Outlier inspection

---

### 6. Feature Engineering

Six new business-driven features were created:

* TotalServices
* IsNewCustomer
* AverageMonthlySpend
* HasAutoPayment
* IsLongTermCustomer
* HighMonthlyCharges

These features were created based on business understanding and insights obtained during exploratory data analysis.

---

### 7. Feature Selection

Feature selection was performed before model training.

The following feature was removed:

* customerID

It was removed because it is only a unique identifier and has no predictive value for customer churn.

---

### 8. Feature Encoding

Categorical variables were converted into numerical format using One-Hot Encoding to make them suitable for machine learning.

Numerical features were standardized using StandardScaler before model training.

---

### 9. Train-Test Split

The dataset was divided into:

* Training Set: 80%
* Testing Set: 20%

The testing dataset remained unseen during training to provide an unbiased evaluation of model performance.

---

### 10. Model Selection

The project uses:

## Logistic Regression

### Why Logistic Regression?

Logistic Regression was selected because:

* The task is a binary classification problem.
* It is simple, interpretable, and computationally efficient.
* It performs well on structured tabular datasets.
* The assignment prioritizes a well-prepared dataset over model complexity.
* It provides a strong baseline for customer churn prediction.

---

### Model Training

The model was trained using the cleaned and feature-engineered training dataset after preprocessing and feature encoding.

---

### Model Evaluation

The model was evaluated using unseen testing data.

Evaluation Metrics:

| Metric | Value |
|---------|-------|
| Accuracy | **80.41%** |
| Precision | **66.44%** |
| Recall | **52.94%** |
| F1-Score | **58.93%** |
| ROC-AUC | **84.16%** |

Confusion Matrix

```text
[[935 100]
 [176 198]]
```

---

# 📈 Results

The model achieved an accuracy of over **80%** with a strong **ROC-AUC score of 84.16%**, showing good overall ability to distinguish between customers who churn and those who remain.

The analysis also identified several important churn indicators, including:

* Month-to-month contracts
* Low customer tenure
* Higher monthly charges
* Fiber Optic internet service
* Electronic Check payment method

Customers with long-term contracts, automatic payment methods, and longer tenure were generally less likely to churn.

---

# 💡 Business Recommendations

* Improve onboarding and customer engagement during the first year of service to reduce early customer churn.
* Encourage customers to switch from month-to-month contracts to long-term plans through discounts and loyalty programs.
* Promote automatic payment methods and review Fiber Optic service quality or pricing to improve customer retention.

---

# ⚠ Limitations

* Logistic Regression assumes a linear relationship between features and the target variable.
* The dataset is moderately imbalanced, making churn prediction more challenging.
* Additional customer behavior and usage data could further improve model performance.
* More advanced models such as Random Forest or XGBoost may achieve higher predictive accuracy.

---

# 💻 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook
* Git
* GitHub

---

# 📚 What I Learned

During this project I gained practical experience with:

* Business understanding
* Data understanding
* Data quality assessment
* Data cleaning
* Exploratory Data Analysis (EDA)
* Feature engineering
* Feature selection
* Feature encoding
* Logistic Regression
* Model evaluation
* Git and GitHub workflow
* Building an end-to-end Machine Learning classification pipeline

---

# ⚠ Challenges Faced

Some challenges encountered during this project included:

* Detecting hidden missing values stored as blank strings instead of standard null values.
* Deciding the most appropriate way to handle missing values without losing data.
* Designing meaningful business-driven features instead of creating arbitrary features.
* Selecting a simple model that satisfied the assignment requirements while still achieving good predictive performance.
* Understanding how preprocessing, feature engineering, and model evaluation affect overall model performance.


# 👨‍💻 Author

**Muhammad Hadin Mirza**

Computer Engineering Student

Machine Learning Enthusiast

This project was developed for learning purposes and to demonstrate an end-to-end Machine Learning workflow suitable for an academic portfolio.