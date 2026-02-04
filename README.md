# Diabetes Risk Prediction Using Machine Learning

## Overview
This project applies machine learning techniques to estimate diabetes risk using health and lifestyle survey data.  
The goal is not medical diagnosis, but **early risk screening** — identifying individuals who may require further clinical testing.

The project demonstrates how predictive models can support healthcare decision-making while highlighting the importance of evaluation metrics in imbalanced medical datasets.

---

## Problem Statement
Diabetes is a widespread chronic condition where early detection is critical.  
However, comprehensive medical testing for all individuals is costly and impractical.

This project addresses the question:

> Can we use non-diagnostic health and lifestyle indicators to estimate diabetes risk for individuals whose diabetes status is unknown?

---

## Objective
- Build and evaluate machine learning models for binary diabetes risk prediction  
- Analyze model performance beyond accuracy, focusing on recall and ROC–AUC  
- Identify the most influential features contributing to diabetes risk  

---

## Dataset
- Source: Behavioral Risk Factor Surveillance System (BRFSS)
- Target variable:
  - `0` → No diabetes
  - `1` → Diabetes
- Features include:
  - BMI
  - Age
  - Blood pressure
  - General and physical health indicators
  - Lifestyle factors (diet, smoking, alcohol, activity)
  - Socioeconomic indicators

### Data Source
This dataset was obtained from Kaggle:
- Diabetes Health Indicators Dataset  
  https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset

The dataset is derived from the Behavioral Risk Factor Surveillance System (BRFSS) and contains anonymized, self-reported health and lifestyle information.


---

## Models Used
### 1. Logistic Regression
- Used as a baseline and interpretable model
- Feature scaling applied using `StandardScaler`
- Outputs probabilities that can be threshold-adjusted for screening sensitivity

### 2. Random Forest Classifier
- Captures non-linear relationships
- Used to analyze feature importance
- Requires no feature scaling

---

## Evaluation Metrics
Due to class imbalance, accuracy alone was insufficient.

The following metrics were used:
- Confusion Matrix
- Precision, Recall, F1-score
- ROC–AUC Score

---

## Key Results
- Logistic Regression achieved **ROC–AUC ≈ 0.82**, indicating strong class separability
- Default threshold resulted in low recall for diabetic cases, highlighting the risks of accuracy-based evaluation
- Random Forest feature importance identified **BMI, age, general health, and blood pressure** as the most influential predictors
- Results align with established medical understanding of diabetes risk factors

---

## Key Takeaways
- Machine learning models can effectively estimate diabetes risk when used as screening tools
- Threshold selection is critical in healthcare-related classification tasks
- Interpretability and evaluation metrics matter more than raw accuracy in imbalanced datasets

---

## Limitations
- This model is **not a diagnostic tool**
- Predictions depend on self-reported survey data
- False positives and false negatives carry different real-world consequences

---

## Tools & Technologies
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

---

## Conclusion
This project demonstrates how machine learning can be responsibly applied to healthcare screening problems by prioritizing interpretability, evaluation rigor, and real-world constraints.

---

## Author
**Prathamesh Lande**

