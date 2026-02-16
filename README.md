# Loan Approval Risk & Loan Limit Prediction

Machine learning project predicting:

1. **Loan approval risk** (classification)  
2. **Maximum approved loan amount** (regression)

Built using **Python** and **scikit-learn**.

---

## Business Problem

Financial institutions must evaluate loan applications while minimising default risk.

This project builds predictive models to:

- Identify high-risk applicants likely to be declined  
- Estimate the maximum loan amount that can be safely approved  
- Support risk-adjusted lending decisions  
- Enable personalised loan offers  

---

## Dataset

The dataset contains approximately **58,600 loan applications** with financial and demographic features such as:

- Income  
- Employment length  
- Loan amount  
- Interest rate  
- Credit history  
- Loan intent  
- Home ownership  

### Target Variables

| Task | Target |
|---|---|
| Classification | `loan_approval_status` |
| Regression | maximum loan amount approved |

---

## Machine Learning Approach

### Data Preparation

- Feature scaling  
- One-hot encoding of categorical variables  
- Class imbalance inspection  
- Train/test split (80/20, stratified)

### Models Evaluated

- Logistic Regression  
- Naive Bayes  
- Decision Tree  
- Random Forest (final model)

### Hyperparameter Tuning

Random Forest hyperparameters optimised using:

- GridSearchCV  
- 5-fold cross-validation  

Optimisation focused on improving recall for **high-risk (declined) loan applications**.

---

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
```

---

## Key Results

### Classification Performance (Test Set)

| Model | ROC AUC |
|---|---|
| Naive Bayes | 0.87 |
| Logistic Regression | 0.89 |
| Random Forest | **0.94** |

Final tuned Random Forest achieved:

- Accuracy ≈ **0.95**
- Strong recall for declined loans
- Balanced precision–recall performance
- Good generalisation with minimal overfitting

---

### Regression Performance (Maximum Loan Prediction)

Two regression feature sets were evaluated.

| Model | R² | Mean Absolute Error |
|---|---|---|
| Numerical features only | 0.969 | ≈ £1,210 |
| Full feature set | **0.971** | ≈ £1,257 |

Both models demonstrate strong predictive performance.  
Most predictive signal comes from core financial indicators.

---

## Key Findings

- Random Forest significantly outperformed simpler classifiers  
- Ensemble learning captured complex borrower risk patterns  
- Financial variables (income, loan size, credit history) drive prediction accuracy  
- Additional encoded features provide marginal regression improvement  
- Model provides a reliable framework for risk-based lending decisions  

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

### Option 1 — Google Colab (recommended)

Open the notebook and run all cells:

```
notebooks/Loan Approval Risk and Loan Limit Prediction.ipynb
```

The notebook handles setup automatically.

---

### Option 2 — Local Machine

1. Clone repository

```
git clone https://github.com/KieranRossetti/Loan-Approval-Risk.git
cd Loan-Approval-Risk
```

2. Install dependencies

```
pip install -r requirements.txt
```

3. Run notebook

Open:

```
notebooks/Loan Approval Risk and Loan Limit Prediction.ipynb
```

Run all cells.

---

## Technologies Used

- Python  
- pandas  
- NumPy  
- scikit-learn  
- matplotlib  
- seaborn  
- joblib  

---

## Portfolio Context

This project demonstrates applied machine learning for financial risk modelling, including:

- End-to-end predictive modelling pipeline  
- Classification and regression modelling  
- Hyperparameter optimisation  
- Model evaluation and comparison  
- Real-world business decision support  

---

## Author

**Kieran Rossetti**  
Machine Learning & Data Analytics Portfolio Project
