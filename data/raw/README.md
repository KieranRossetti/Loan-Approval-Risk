# Raw Data

This folder contains the **original dataset** used in the project.

The raw data is not modified and serves as the starting point for all preprocessing and modelling steps.

---

## Expected File

Place the following dataset in this folder:

```
loan_approval_data.csv
```

The notebook reads this file directly when running the analysis.

---

## Why the Dataset Is Not Included

The dataset is not stored in this repository due to size and distribution restrictions.

To run the project locally, you must provide the dataset yourself.

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

## Folder Purpose

This folder should only contain:

- Original unmodified data files

Processed or cleaned data should **not** be stored here.
