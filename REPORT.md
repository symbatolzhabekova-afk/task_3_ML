
# Machine Learning Task 3 Report

## 1. Project Overview

The objective of this project is to predict whether a bank client will subscribe to a term deposit using classification algorithms.

## 2. Dataset Description

- Training dataset: 32,940 rows and 22 columns.
- Test dataset: 8,236 rows and 20 columns.
- Target variable: `y`.
- Target classes: `yes` and `no`.
- Positive class proportion: approximately 11.27%.
- Negative class proportion: approximately 88.73%.

## 3. Data Preprocessing

- Removed the `id` column because it is an identifier.
- Excluded `duration` from model features.
- Used median imputation for numerical features.
- Used most-frequent imputation for categorical features.
- Scaled numerical features using StandardScaler.
- Encoded categorical features using OneHotEncoder.
- Split the training data into training and validation sets using stratified sampling.

## 4. Models

Three classification models were evaluated:

- Logistic Regression
- Decision Tree
- Random Forest

## 5. Model Evaluation

The models were evaluated using Accuracy, Precision, Recall, F1-score, and ROC-AUC.

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 0.8365 | 0.3701 | 0.6429 | 0.4697 | 0.8028 |
| Random Forest | 0.8978 | 0.5873 | 0.3127 | 0.4081 | 0.7899 |
| Decision Tree | 0.8555 | 0.4004 | 0.5687 | 0.4699 | 0.7447 |

## 6. Model Selection

Logistic Regression was selected based on its highest validation ROC-AUC score of 0.8028.

## 7. Test Predictions

The selected model generated predictions for all 8,236 test records.

- Total predictions: 8,236.
- Missing predictions: 0.
- Output labels: `yes` and `no`.

## 8. Output Files

- `outputs/model.joblib`
- `outputs/predictions.csv`
- `outputs/model_comparison.csv`

## 9. Conclusion

Logistic Regression achieved the highest ROC-AUC score among the three evaluated models. The project completed the main classification workflow, including preprocessing, model training, evaluation, model selection, and test prediction generation.
