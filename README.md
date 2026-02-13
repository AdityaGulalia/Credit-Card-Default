# Credit Card Default Prediction — Decision Tree

## Project Overview

This project builds a **binary classification model** to predict whether a credit card customer will **default on their payment next month**.
The model used is a **Decision Tree Classifier**, which learns decision rules from customer financial and payment history.

The main goal of this project is to understand:

* How decision trees work
* Model complexity
* Overfitting vs underfitting
* Feature importance

---

## Problem Statement

Credit card companies want to identify customers who are likely to **default on their payments**.
By predicting this in advance, they can:

* Reduce financial risk
* Adjust credit limits
* Take preventive measures

The objective of this project is:

> Predict whether a customer will default next month based on their financial and payment history.

---

## Dataset

**Dataset:** Credit Card Default Dataset
**Rows:** ~30,000 customers
**Features:** 23 financial and demographic attributes
**Target column:** `default.payment.next.month`

Target values:

* `0` → No default
* `1` → Default

---

## Feature Categories

### Demographic Information

* `SEX`
* `EDUCATION`
* `MARRIAGE`
* `AGE`

### Credit Information

* `LIMIT_BAL` (credit limit)

### Payment History (Last 6 Months)

* `PAY_0` to `PAY_6`
  Represents repayment status for each month.

### Bill Amounts (Last 6 Months)

* `BILL_AMT1` to `BILL_AMT6`
  Monthly credit card bills.

### Payment Amounts (Last 6 Months)

* `PAY_AMT1` to `PAY_AMT6`
  Actual payments made.

---

## Project Workflow

### 1. Data Loading and Inspection

* Loaded dataset using pandas
* Checked data types and missing values
* Verified dataset structure

### 2. Data Preprocessing

* Removed the `ID` column (non-informative identifier)
* Split features and target

### 3. Train-Test Split

* Training data: 80%
* Testing data: 20%

### 4. Model Training

* Model used: **Decision Tree Classifier**
* Trained using the training dataset

### 5. Model Evaluation

Evaluated the model using:

* Classification report
* Confusion matrix
* Accuracy score

---

## Model Tuning: Tree Depth

The `max_depth` parameter was varied to study:

* Underfitting (very shallow trees)
* Overfitting (very deep trees)

Example depths tested:

```
[2, 4, 6, 8, 10, 15]
```

This helped identify the depth with the best generalization performance.

---

## Feature Importance Analysis

The decision tree provides **feature importance scores**, showing which features most influenced predictions.

A bar chart was used to visualize the **top 10 most important features**.

This helps understand:

* Key factors affecting default
* Customer behavior patterns

---

## Key Concepts Learned

This project demonstrates:

* Decision tree classification
* Non-linear models
* Overfitting vs underfitting
* Tree depth tuning
* Feature importance analysis
* Confusion matrix interpretation

---

## Tools and Libraries

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

## Project Structure

```
credit-card-default/
│
├── data/
│   └── credit_default.csv
│
├── notebook/
│   └── decision_tree.ipynb
│
└── README.md
```

---

## Results (Example)

Typical performance for a decision tree on this dataset:

* Accuracy: ~75–82%
* Balanced performance between default and non-default classes

(Exact results may vary depending on tree depth and data split.)

---

## Future Improvements

Possible next steps:

* Random Forest classifier
* Gradient Boosting models
* Hyperparameter tuning
* Feature selection
* Handling class imbalance

---

## Conclusion

This project demonstrates how a **decision tree** can be used to predict credit card default risk.
It highlights the importance of **model complexity control** and shows how **feature importance** can provide insights into customer financial behavior.
