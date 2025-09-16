# PCOS Detection using Machine Learning
### 📌 Overview

This project focuses on building predictive machine learning models to detect Polycystic Ovary Syndrome (PCOS) using patient health data. The goal is to leverage statistical analysis, data preprocessing, and classification models to identify PCOS cases with high sensitivity, ensuring minimal false negatives in a healthcare context.

### 📂 Dataset

Two datasets were provided:

PCOS with infertility features

PCOS without infertility features

Both were merged on Patient File No. to create a unified dataset.

Final dataset contained 44 features including demographic, lifestyle, and biological parameters.

### 🔍 Exploratory Data Analysis (EDA)

Univariate Analysis: Studied categorical (Target, Pregnant, Weight Gain, Skin Darkening, etc.) and numerical features (Age, BMI, Cycle Length, etc.).

Outlier Detection: Used boxplots & IQR to check for biological outliers.

Correlation Heatmap: Identified features with correlation > 0.25 with the Target variable.

Insights:

Higher BMI and irregular cycles were strongly linked with PCOS.

Lifestyle factors like fast food consumption and lack of regular exercise showed association.

SHAP values highlighted hormonal markers and cycle length as influential features.

### 🤖 Machine Learning Models

Implemented and compared three classification algorithms:

Logistic Regression

Decision Tree Classifier

Random Forest Classifier

### 📊 Model Evaluation

Models were evaluated using:

Confusion Matrix

Accuracy = (TP + TN) / (TP + TN + FP + FN)

Precision = TP / (TP + FP)

Recall (Sensitivity) = TP / (TP + FN) → prioritized for healthcare

ROC Curve & AUC

Key Result:

Random Forest delivered the best balance of metrics with Recall ≈ 81%, ensuring most PCOS cases were correctly identified.

### 🌟 Explainability

Used SHAP (SHapley Additive exPlanations) to interpret model predictions.

Top influential features included:

BMI

Cycle length

Hormone levels (FSH/LH ratio, AMH, PRL)

Lifestyle indicators

### 🧪 Prediction for New Patients

Built a pipeline to take new patient data as input and predict PCOS status.

Outputs both:

Prediction (PCOS / No PCOS)

Probability of PCOS

### ✅ Key Takeaways

Highlighted the importance of recall in medical diagnosis.

Demonstrated ability to handle real-world messy data (merging, encoding, scaling, outlier analysis).

Applied model comparison, evaluation, and interpretability techniques.

Showcased end-to-end ML workflow: data preprocessing → EDA → model training → evaluation → explainability → prediction.

### 📌 Tools & Libraries

Python (pandas, numpy, matplotlib, seaborn)

scikit-learn (Logistic Regression, Decision Tree, Random Forest, metrics)

SHAP (model interpretability)

### 🚀 Future Scope

Deploy the model as a web application for real-time predictions.

Experiment with advanced models (XGBoost, LightGBM).

Collect larger and more diverse datasets for generalization.
