# 🩺 Breast Cancer Classification using Support Vector Machine (SVM)

## 📌 Project Overview

This project applies **Support Vector Machine (SVM)** to classify breast cancer tumors based on their diagnostic measurements. Multiple SVM kernels were evaluated, and the best-performing model was further optimized using **GridSearchCV**.

Since this is a **medical diagnosis** problem, the primary objective was not only to achieve high accuracy but also to minimize **False Negatives (Type II Errors)**, as failing to identify a cancer patient can have serious clinical consequences.

---

## 🎯 Business Problem

Early detection of breast cancer plays a crucial role in improving patient outcomes.

The goal of this project is to develop a machine learning model capable of accurately classifying tumors while minimizing false negatives, ensuring that cancer cases are not overlooked.

---

## 📂 Dataset

- **Dataset:** Breast Cancer Wisconsin Diagnostic Dataset
- **Target Variable:** `diagnosis`
- **Classes:**
  - **N** → Benign (Non-cancerous)
  - **R** → Malignant (Cancerous)

---

## 🛠️ Project Workflow

- Data Loading
- Data Cleaning
- Exploratory Data Analysis (EDA)
- Target Encoding
- Feature Selection
- Train-Test Split
- Feature Scaling using StandardScaler
- Model Building using:
  - Linear SVM
  - RBF SVM
  - Polynomial SVM
- Model Comparison
- Hyperparameter Tuning using GridSearchCV
- Model Evaluation
- ROC Curve Analysis
- Prediction on Unseen Data

---

## 📊 Exploratory Data Analysis

The following analyses were performed:

- Checked missing values and duplicate records
- Examined class distribution
- Statistical summary using `describe()`
- Distribution analysis using histograms
- Outlier detection using boxplots
- Correlation analysis using a heatmap

### Key Findings

- No missing values
- No duplicate records
- Most numerical features were right-skewed
- Features were on different scales, making feature scaling essential
- Several highly correlated features were observed, which is acceptable for SVM since it is not a coefficient-based model

---

## 🤖 Models Implemented

| Model | Accuracy |
|--------|---------:|
| Linear SVM | 96.49% |
| RBF SVM | 97.37% |
| Polynomial SVM | 88.60% |
| Tuned RBF SVM | **98.25%** |

---

## 🔧 Hyperparameter Tuning

The best-performing kernel (**RBF**) was optimized using **GridSearchCV**.

### Tuned Parameters

- C
- Gamma

Cross-validation was used to identify the best combination of hyperparameters.

---

## 📈 Model Performance

### Final Tuned RBF SVM

| Metric | Score |
|---------|------:|
| Accuracy | **98.25%** |
| Precision | **1.00** |
| Recall | **0.95** |
| F1-Score | **0.98** |
| ROC-AUC | **0.976** |

---

## 📌 Why RBF Kernel?

Although the Linear SVM achieved an impressive **96.49%** accuracy, the RBF kernel provided superior overall performance by:

- Increasing classification accuracy
- Improving Recall
- Reducing False Negatives
- Achieving the highest ROC-AUC score

For a medical diagnosis problem, minimizing **False Negatives** is particularly important because missing a cancer patient can delay treatment and negatively impact patient outcomes.

---

## 📉 ROC Curve

The tuned RBF SVM achieved an **ROC-AUC score of 0.976**, demonstrating excellent ability to distinguish between benign and malignant tumors across different decision thresholds.

---

## 🧰 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## 📚 Machine Learning Concepts Covered

- Support Vector Machine (SVM)
- Linear Kernel
- RBF Kernel
- Polynomial Kernel
- Hyperparameter Tuning
- GridSearchCV
- StandardScaler
- Confusion Matrix
- Precision
- Recall
- F1 Score
- ROC Curve
- ROC-AUC
- Model Evaluation

---

## 🚀 Future Improvements

- Perform dimensionality reduction using PCA for visualization.
- Experiment with additional machine learning algorithms such as Random Forest and XGBoost.
- Deploy the trained model as a web application using Streamlit or Flask.

---

## 👩‍💻 Author

**Dharani Kaligi**

If you found this project useful, feel free to ⭐ the repository.
