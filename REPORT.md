# Machine Learning Project Report

## 1. Project Overview

The goal of this project is to predict whether a bank client will subscribe to a term deposit using machine learning classification models.

## 2. Dataset

The dataset contains customer demographic information, financial indicators, and details about previous marketing campaigns.

- Training samples: 32,940
- Test samples: 8,236
- Target variable: `y`
- Positive class: `yes`
- Negative class: `no`

The target classes are imbalanced, with approximately 11.27% positive examples and 88.73% negative examples.

## 3. Data Preprocessing

- Removed the `id` column because it is an identifier.
- Excluded `duration` to avoid using call duration as a predictor.
- Imputed missing values using median imputation for numerical features and most-frequent imputation for categorical features.
- Scaled numerical features.
- Applied one-hot encoding to categorical features.
- Used a stratified train-validation split.

## 4. Models

The following models were evaluated:

- Logistic Regression
- Decision Tree
- Random Forest

## 5. Evaluation

Models were compared using Accuracy, Precision, Recall, F1-score, and ROC-AUC.

The best model was selected based on validation ROC-AUC.

## 6. Output Files

- `outputs/model.joblib`: saved trained model
- `outputs/predictions.csv`: test predictions
- `outputs/model_comparison.csv`: validation metrics for all models

## 7. Conclusion

The project demonstrates a complete classification workflow, including preprocessing, model training, evaluation, model selection, and prediction generation.

