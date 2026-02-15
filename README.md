# Loan-Approval-Risk
Machine learning project predicting loan approval risk (classification) and maximum loan amount (regression) using Python and scikit-learn.

# Runtime note (important)

- The first run will train/tune the Random Forest model (can take ~10 minutes).
- After the first run, the tuned model is saved to `models/rf_best.joblib`.
- With `FAST_MODE = True`, future runs will load the saved model instantly.
