# Loan Default Prediction-GhanaLoanConnect

## Overview

This project addresses the problem of **Non-Performing Loans (NPLs)** at GhanaLoanConnect, a peer-to-peer lending platform. Our team developed a machine learning solution to predict whether a borrower is likely to default on a loan, enabling the company to make more informed lending decisions.



##  Objectives

- Predict borrowers likely to **default**
- Identify and analyse top risk indicators
- Select the best-performing model through evaluation and tuning



##  Dataset

- **Source**: Internal dataset from GhanaLoanConnect
- **Records**: 9,578 borrowers
- **Target Variable**: `not.fully.paid`
- **Notable Features**:
  - `int.rate` (interest rate)
  - `instalment` (monthly payment)
  - `log.annual.inc` (log of income)
  - `fico` (FICO credit score)
  - `purpose` (loan purpose)



##  Techniques Used

###  Data Cleaning & Preprocessing
- Handled missing values
- One-hot encoded `purpose`
- Created `long_credit_history` as a derived feature

###  Feature Engineering
- Added indicators like:
  - Long vs. short credit history
  - High debt-to-income ratio
  - Low FICO score

### Modeling
- **Logistic Regression**
- **Random Forest**
- **Gradient Boosting**
- Used **SMOTE** for balancing imbalanced target classes
- Applied **GridSearchCV** for hyperparameter optimization

###  Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1 Score
- ROC AUC
- Confusion Matrix



##  Key Results

| Model               | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|--------------------|----------|-----------|--------|----------|---------|
| Logistic Regression| 0.90    | 0.91     | 0.97  | 0.94    | 0.95   |
| Gradient Boosting  | **0.99** | **0.99**  | **0.997** | **0.99** | **0.995** |
| Random Forest (Tuned)| TBD   | TBD       | TBD    | TBD      | TBD     |



## Insights

- **Higher interest rates**, **low FICO scores**, and **short credit history** are strong predictors of default.
- Tree-based models significantly outperformed logistic regression.
- Oversampling with SMOTE reduced false negatives and improved model fairness.



##  Project Structure


─ loan_borrower_data.csv            # The main dataset used for training and evaluation
─ Bank loan default.ipynb           # Jupyter notebook containing all preprocessing, modelling, and evaluation steps
─ Report_Project_Approach.docx      # Report on project workflow and team contributions
─ Report_Findings_Recommendations.docx  # Report on insights, results, and recommendations
─ README.md                         # Overview of the project, team, and outcomes



## Team

**Project Manager**  
- Patrick Ayeh Ayisi  

**Collaborators**  
- Umar Zaidu Yakubu
- David Wilson
- Owiredu-Amoh Baffuor Etto Jr.
- Marvin Dawson
- Jemima Ama Fiapemetsi
- Iwikotan Oreofe Gloria
- Maya Leotina Agebedekpui




##  Future Work

- Add more real-world features (e.g., employment status, location)
- Explore model explainability (SHAP, LIME)
- Deploy using Streamlit or Flask




