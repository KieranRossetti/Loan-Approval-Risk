# Notebooks

This folder contains the main analysis notebook used for the project.

---

## Main Notebook

**Loan Approval Risk and Loan Limit Prediction.ipynb**

This notebook performs the complete machine learning workflow, including:

1. Data loading and inspection  
2. Data cleaning and preprocessing  
3. Feature encoding and scaling  
4. Exploratory data analysis (EDA)  
5. Model training and evaluation  
6. Hyperparameter tuning using GridSearchCV  
7. Model performance comparison  
8. Saving and loading the tuned model  

---

## Model Training Modes

The notebook supports two execution modes.

### TRAIN MODE
- Runs full hyperparameter tuning
- Takes several minutes
- Saves the tuned model locally

### FAST MODE
- Loads previously saved tuned model
- Skips training
- Runs quickly

Switch mode inside the notebook:

```python
FAST_MODE = True   # fast execution
FAST_MODE = False  # retrain model
```

---

## How to Run

Open the notebook and run all cells sequentially.

Recommended environment:
- Google Colab

Alternative:
- Local Python environment with required dependencies installed

---

## Runtime Notes

- First run may take several minutes due to hyperparameter tuning
- Later runs are fast when using FAST MODE
- The trained model is saved locally and not stored in the repository

---

## Purpose

The notebook demonstrates an end-to-end machine learning pipeline for:

- Loan approval classification
- Loan amount regression

It is designed for:
- reproducibility
- clear model evaluation
- realistic ML deployment workflow
