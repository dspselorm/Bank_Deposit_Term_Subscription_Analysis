# Bank_Deposit_Term_Subscription_Analysis


# Term Deposit Subscription Prediction

This project aims to predict whether a bank client will subscribe to a term deposit based on various features such as demographic data, contact duration, and previous campaign history. It leverages data analysis, feature engineering, and logistic regression to build a predictive model.

---

## Project Overview

- **Goal**: Help marketing teams identify which clients are likely to subscribe to term deposits.
- **Data**: CSV dataset from a bank's direct marketing campaigns.
- **Target Variable**: `y` (yes/no — whether the client subscribed)

---

## Steps Performed

### 1. Exploratory Data Analysis (EDA)
- Checked class balance, feature distributions, and patterns.
- Found key insights: longer calls and certain job types (e.g., retired, students) correlate with higher subscription rates.

### 2. Feature Engineering
- Created new features:
  - `contacted_before` from `pdays`
  - `duration_contacted` = duration × contacted_before
  - Grouped `age` and `duration` into bins
- Encoded categorical variables using OneHotEncoder

### 3. Model Building
- Used **Logistic Regression** with:
  - `class_weight='balanced'` to handle class imbalance
  - Train/test split: 70/30
  - Evaluation metrics: accuracy, precision, recall, F1 score

### 4. Performance
- **Accuracy**: 83%
- **Recall (Subscribed)**: 78% (↑ from 23%)
- **Precision (Subscribed)**: 30%
- **F1 Score (Subscribed)**: 0.44

---

## Deliverables

- `final_project_report.txt`: Full summary of analysis and results
- `bank.csv`: Original dataset (semicolon-delimited)
- Python code for:
  - Data cleaning and preprocessing
  - Feature engineering
  - Model training and evaluation
- Visualizations (optional)

---

## Key Takeaways

- Target clients with job types like **retired**, **students**, and **admin staff**
- Focus on calls lasting longer than 200 seconds
- Schedule campaigns in **March, June, or December**
- Use balanced models to improve recall on minority class

---

## Tech Stack

- Python 3
- pandas, scikit-learn, seaborn, matplotlib
- imbalanced-learn (SMOTE)
