# 🧠 Stroke Prediction – Data Mining Project

This project explores stroke risk prediction based on medical and demographic features using several machine learning techniques.

The project began as an academic exercise using [WEKA](https://www.cs.waikato.ac.nz/ml/weka/) and was later extended in Python using scikit-learn and Keras for improved control and flexibility.

---

## 📊 Dataset

- **Source**: [Kaggle – Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
- **Size**: 5,110 patient records
- **Target column**: `stroke` (0 = no stroke, 1 = stroke)
- **Features**: age, gender, hypertension, heart disease, glucose, BMI, smoking status, etc.

---

## 📚 Project Background

This project began in the WEKA environment as part of a university data mining course. The initial work included:

- ✅ **Decision Trees**: J48 (C4.5) and SimpleCart
- 📊 **Clustering**: KMeans
- 🔗 **Association Rules**: Apriori
- 🔍 Basic preprocessing: discretization, label encoding, and class balancing using SMOTE

Following the original submission, the project was expanded using Python for code-based experimentation and advanced modeling (e.g., Keras MLP).

📁 The WEKA-based summaries can be found here:  
[`weka/mman21_summary.md`](weka/mman21_summary.md)

---

## 🧪 Methods Used

| Technique              | Tool             | Purpose                           |
| ---------------------- | ---------------- | --------------------------------- |
| Decision Tree (J48)    | WEKA             | Interpretable supervised learning |
| SimpleCart             | WEKA             | Binary-split decision tree        |
| Decision Tree (Python) | scikit-learn     | Reimplementation in Python        |
| Clustering (KMeans)    | scikit-learn     | Discovering hidden groups         |
| Neural Network (MLP)   | Keras            | Deep learning for classification  |
| SMOTE                  | imbalanced-learn | Address class imbalance           |

---

## 📈 Model Results

| Model                  | Accuracy | Recall (Stroke) | Precision (Stroke) |
| ---------------------- | -------- | --------------- | ------------------ |
| SimpleCart (WEKA)      | 92.9%    | 92.9%           | 90.7%              |
| J48 (WEKA)             | 92.2%    | 92.8%           | 90.3%              |
| Decision Tree (Python) | 83%      | 92%             | ~77% (est.)        |
| Neural Network (Keras) | 81%      | 47%             | 14%                |
| KMeans Clustering      | —        | —               | —                  |

---

## 💡 Key Insights

- **Decision Trees** yielded the best results, offering strong recall and precision for stroke cases.
- **KMeans** successfully revealed a health-risk cluster, even without labels.
- **Neural Network** struggled with precision and recall due to class imbalance, but demonstrated stable training behavior.
- **SMOTE** improved recall in most models but often reduced precision.

---

## ▶️ How to Run the Notebook

1. Clone this repository:

   bash
   git clone https://github.com/HiliMor/stroke-prediction-project.git
   cd stroke-prediction-project

2. Download the dataset from Kaggle and place it inside the data/ folder.

3. Open the Jupyter notebook:
   notebooks/stroke_prediction_decision_tree.ipynb

---

## 🎓 Author Note

This project was originally submitted as part of a university course in Data Mining, and then extended into a full analytical project using modern Python tools for portfolio and learning purposes.
