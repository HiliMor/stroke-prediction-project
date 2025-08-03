# 📘 Stroke Prediction using WEKA

This project analyzes stroke risk prediction based on patient health and demographic features, using decision tree classifiers in WEKA.

## 🧠 Problem Definition

The goal was to predict the likelihood of a stroke based on features such as:

- Gender
- Age
- Hypertension
- Heart disease
- Glucose level
- BMI
- Smoking status
- Marital and work status

The dataset contained 5,110 records and was highly imbalanced (only ~5% stroke cases).

## 🧼 Preprocessing

- Removed irrelevant columns (e.g., ID)
- Removed rare gender entry ("Other")
- Imputed missing `bmi` values with the mean
- Discretized continuous features (age, glucose, BMI) based on medical thresholds
- Applied SMOTE to balance classes (note: SMOTE was mistakenly applied to the entire dataset, causing data leakage – discussed and acknowledged)

## 🌲 Models Used (via WEKA)

### 1. **J48 (C4.5)**

- Handles continuous features
- Uses Gain Ratio for split selection
- Includes pruning
- Accuracy: **92.2%**

### 2. **SimpleCart**

- Binary splits using Gini Index
- Post-pruning to reduce overfitting
- Accuracy: **92.9%**
- Better recall for stroke detection

## 📊 Performance Comparison

| Model      | Accuracy | Recall (stroke) | Precision (stroke) | F1 Score |
| ---------- | -------- | --------------- | ------------------ | -------- |
| J48        | 92.2%    | 92.8%           | 90.3%              | 91.5%    |
| SimpleCart | 92.9%    | 92.9%           | 90.7%              | 91.8%    |

## 🧠 Insights

- SimpleCart performed better in detecting stroke cases (important in medical context).
- Discretizing based on clinical thresholds helped model interpretability.
- Highlighted importance of feature selection and data balancing.
