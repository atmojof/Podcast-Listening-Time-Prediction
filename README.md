# Podcast Listening Time Prediction (Playground Series S5E4 - Kaggle)

This repository contains a solution for the Kaggle competition: **Playground Series S5E4**, where the goal is to predict podcast listening time based on episode features.

## Task

Predict the number of minutes each podcast episode is listened to (`Listening_Time_minutes`) using structured metadata such as genre, guest popularity, and time of publication.

## Approach

We use a **Random Forest Regressor** with **K-Fold Cross-Validation** (5 folds) to estimate performance. The solution includes robust feature engineering and handles missing values and categorical data appropriately.

## Feature Engineering

- **Ordinal Encoding** for `Publication_Time` (e.g., Morning < Afternoon < Night).
- **One-hot Encoding** for categorical variables like `Podcast_Name`, `Genre`, etc.
- Median imputation for missing values in numeric features.
- Ensuring aligned features between train and test sets.

## Evaluation Metrics

- **Root Mean Squared Error (RMSE)** – for accuracy.
- **Mean Absolute Error (MAE)** – for robustness.
- **Standard Deviation of Absolute Error (SDA)** – to assess prediction consistency.

## Final Model

The final predictions are generated using the full training set with a basic Random Forest Regressor.

## Files

- `train.csv`, `test.csv`, `sample_submission.csv`: Original data from Kaggle
- `submission_rf_cv.csv`: Submission file generated from cross-validated model
- `notebook.py`: Full model training and prediction code (this script)

## Requirements

- Python 3.x
- pandas, numpy, scikit-learn

## Author

Firmansyah Tri Atmojo – Senior Data Scientist



---
