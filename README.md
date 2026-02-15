# Loan Approval Risk & Loan Limit Prediction

Machine learning project predicting:

1. Loan approval risk (classification)
2. Maximum approved loan amount (regression)

Built using Python and scikit-learn.

---

## Business Problem

Financial institutions must evaluate loan applications while minimising default risk.

This project builds predictive models to:

- Identify high-risk applicants likely to be declined
- Estimate the maximum loan amount that can be safely approved
- Support risk-adjusted lending decisions
- Enable personalised loan offers


## Dataset

The dataset contains approximately **58,600 loan applications** with financial and demographic features such as:

- Income  
- Employment length  
- Loan amount  
- Interest rate  
- Credit history  
- Loan intent  
- Home ownership  

Target variables:

| Task | Target |
|---|---|
| Classification | `loan_approval_status` |
| Regression | Maximum loan amount approved |


## Machine Learning Approach

### Data Preparation
- Feature scaling
- One-hot encoding of categorical variables
- Class imbalance inspection
- Train/test split (80/20, stratified)

### Models Trained
- Logistic Regression
- Decision Tree
- Random Forest (final model)

### Hyperparameter Tuning
Random Forest hyperparameters were optimised using:

- GridSearchCV
- 5-fold cross-validation

Parameters evaluated:

- `n_estimators`
- `max_depth`
- `min_samples_split`
- `max_features`

Optimisation focused on improving recall for high-risk (declined) loan applications.


## Model Training Strategy

Hyperparameter tuning is computationally expensive, so the project supports two execution modes.

### TRAIN MODE
- Runs full hyperparameter tuning
- Saves best model to `models/rf_best.joblib`

### FAST MODE
- Loads previously tuned model
- Skips training for fast execution

Switch mode using:

```python
FAST_MODE = True   # fast execution
FAST_MODE = False  # retrain model
