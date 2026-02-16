# Raw Data

This folder contains the **original dataset** used in the project.

The raw data is not modified and serves as the starting point for all preprocessing and modelling steps.

---

## Dataset Availability

The dataset is included in this repository for reproducibility and ease of use.

Location:
data/raw/loan_approval_data.csv

The notebook reads this file directly when running the analysis.

---

## How It Is Used

The raw dataset is used to:

- Clean and preprocess data
- Generate processed datasets
- Train classification and regression models

All transformed outputs are saved in:

```
data/processed/
```

---

## Data Integrity Policy

Files in this folder must remain **unchanged**.

All cleaning, transformation, and feature engineering must be performed in the analysis pipeline and saved to the processed data folder.

This ensures reproducibility and preserves the original source data.

---

## Folder Purpose

This folder should only contain:

- Original unmodified data files

Processed or cleaned data should **not** be stored here.
