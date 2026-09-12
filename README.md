# Global FinBank – Predictive Loan Modeling

## 📌 Project Overview

This project focuses on using Machine Learning to predict loan defaults for Global FinBank.

The objective is to identify potentially high-risk loans and support better credit-risk management and lending decisions using historical loan and customer data.

---

## 🎯 Objectives

- Predict whether a borrower is likely to default on a loan.
- Identify important factors influencing loan default.
- Compare multiple Machine Learning classification models.
- Select the best-performing model for loan default prediction.
- Provide business recommendations based on model results.

---

## 📊 Dataset

The project uses two datasets:

- Loan dataset
- Customer dataset

The datasets were merged using `customer_id`.

The combined dataset contains **270,299 loan records** and **29 features** after merging.

Key variables include:

- Annual Income
- Loan Amount
- Funded Amount
- Interest Rate
- Installment
- Loan Term
- Loan Grade
- Loan Purpose
- Home Ownership
- Employment Length
- Verification Status
- Issue Year
- Loan Status

---

## 🔄 Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the loan and customer datasets.
2. Checked data types and dataset structure.
3. Identified missing values.
4. Merged loan and customer datasets using `customer_id`.
5. Created a binary default target variable.
6. Encoded categorical variables using One-Hot Encoding.
7. Imputed missing values.
8. Scaled numerical features using StandardScaler.
9. Split the data into training and testing sets.

---

## 🎯 Target Variable

The `loan_status` variable was converted into a binary `default` variable.

- `Default` and `Charged Off` → **1 (Default)**
- Other loan statuses → **0 (Non-Default)**

The dataset contains:

- **252,436 non-default loans**
- **17,863 default loans**
- Default rate: **6.61%**

---

## 🤖 Machine Learning Models

Three classification models were developed and compared:

1. Logistic Regression
2. Decision Tree
3. Random Forest

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

---

## 🌲 Random Forest Model

Random Forest was selected as the preferred model because it achieved the highest F1-score among the three tested models.

### Model Performance

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 93.32% | 29.79% | 0.78% | 1.53% |
| Decision Tree | 93.21% | 25.00% | 1.40% | 2.65% |
| **Random Forest** | **93.15%** | **34.31%** | **3.92%** | **7.03%** |

Random Forest achieved:

- **Accuracy:** 93.15%
- **Precision:** 34.31%
- **Recall:** 3.92%
- **F1 Score:** 7.03%

The Random Forest model had the best F1-score and was therefore selected as the preferred model for loan default prediction.

---

## ⭐ Important Features

The Random Forest feature-importance analysis identified the following important predictors of loan default:

1. Annual Income – **16.5%**
2. Installment – **14.6%**
3. Interest Rate – **12.4%**
4. Loan Amount – **10.3%**

Other influential variables included funded amount and issue year.

---

## 💡 Key Business Insights

- Annual income is the most influential feature in predicting loan default.
- Installment obligations have a strong relationship with default risk.
- Higher interest rates should receive additional attention during risk assessment.
- Larger loan amounts can increase the potential financial exposure associated with default.
- The dataset shows a significant class imbalance, with default loans representing only 6.61% of observations.

---

## 🎯 Business Recommendations

- Use annual income and installment obligations as important inputs during credit-risk assessment.
- Pay closer attention to loans with higher interest rates and larger loan amounts.
- Use the Random Forest model as a supporting tool to identify potentially high-risk loans.
- Combine Machine Learning predictions with human credit-risk review rather than relying only on automated predictions.
- Improve future models using techniques designed to better handle the imbalance between default and non-default loans.

---

## ⚠️ Loan Approval Prediction Limitation

The original project objective also included predicting loan approval outcomes.

However, the available dataset does not contain rejected loan applications. Therefore, a true loan approval prediction model could not be developed using this dataset.

Additional historical loan application data containing both **approved and rejected applications** would be required to build and evaluate a reliable loan approval prediction model.

---

## 🛠️ Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## 📁 Project Structure

```text
global-finbank-ml-project/
│
├── Machine Learning – Predictive Loan Modeling.ipynb
├── README.md
├── requirements.txt
└── .gitignore
