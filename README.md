# Loan Approval Risk & Loan Limit Prediction

Machine learning project predicting:

1. Loan approval risk (classification)
2. Maximum approved loan amount (regression)

Built using Python and scikit-learn.

---

## Business Problem

Financial institutions must evaluate loan applications while minimising default risk.

This project builds predictive models to:

* Identify high-risk applicants likely to be declined
* Estimate the maximum loan amount that can be safely approved
* Support risk-adjusted lending decisions
* Enable personalised loan offers

---

## Dataset

The dataset contains approximately **58,600 loan applications** with financial and demographic features such as:

* Income
* Employment length
* Loan amount
* Interest rate
* Credit history
* Loan intent
* Home ownership

Target variables:

| Task           | Target                       |
| -------------- | ---------------------------- |
| Classification | `loan_approval_status`       |
| Regression     | maximum loan amount approved |

---

## Machine Learning Approach

### Data Preparation

* Feature scaling
* One-hot encoding of categorical variables
* Class imbalance inspection
* Train/test split (80/20, stratified)

### Models Trained

* Logistic Regression
* Decision Tree
* Random Forest (final model)

### Hyperparameter Tuning

Random Forest hyperparameters were optimised using:

* GridSearchCV
* 5-fold cross-validation

Parameters evaluated:

* `n_estimators`
* `max_depth`
* `min_samples_split`
* `max_features`

Optimisation focused on improving recall for high-risk (declined) loan applications.

---

## Model Training Strategy

Hyperparameter tuning is computationally expensive, so the project supports two execution modes.

### TRAIN MODE

* Runs full hyperparameter tuning
* Saves best model to `models/rf_best.joblib`

### FAST MODE

* Loads previously tuned model
* Skips training for fast execution

Switch mode using:

```
FAST_MODE = True   # fast execution
FAST_MODE = False  # retrain model
```

---

## Project Structure

```
Loan-Approval-Risk/
│
├── data/
│   ├── raw/              # original dataset
│   └── processed/        # cleaned and transformed data
│
├── notebooks/
│   └── Loan Approval Risk and Loan Limit Prediction.ipynb
│
├── models/               # saved trained models (ignored by git)
│
├── requirements.txt
└── README.md
```

---

## How to Run the Project

### 1. Clone repository

```
git clone https://github.com/KieranRossetti/Loan-Approval-Risk.git
cd Loan-Approval-Risk
```

### 2. Install dependencies

```
pip install -r requirements.txt
```

### 3. Run notebook

Open:

```
notebooks/Loan Approval Risk and Loan Limit Prediction.ipynb
```

Run all cells.

---

## First Run vs Future Runs

First run:

* trains model
* performs hyperparameter tuning
* saves model

Later runs:

* loads saved model instantly

---

## Technologies Used

* Python
* pandas
* NumPy
* scikit-learn
* matplotlib
* seaborn
* joblib
