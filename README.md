#  IBM HR Analytics – Employee Attrition Prediction

This project uses machine learning to predict whether an employee is likely to leave the company, based on historical HR data provided by IBM.

---

##  Objective

To build a classification model that can predict employee attrition using real-world HR attributes. The goal is to help HR departments identify at-risk employees and take proactive retention measures.

---

##  Dataset

- Source: [IBM HR Analytics Dataset on Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
- File Used: WA_Fn-UseC_-HR-Employee-Attrition.csv
- Contains 35 features for 1,470 employees, including demographics, job role, satisfaction, performance, and attrition status.

---

##  Tools & Libraries

- *Language*: Python  
- *Libraries*: pandas, numpy, matplotlib, seaborn, scikit-learn, imbalanced-learn, xgboost
- *Environment*: Jupyter Notebook / Google Colab

---

##  Workflow Overview

### 1. Data Loading
- Read the CSV file using pandas.

### 2. Data Exploration
- Used .info(), .describe(), .value_counts() to understand variable types and distributions.
- Identified key categorical variables such as JobRole, Department, and OverTime.

### 3. Data Preprocessing
- Applied LabelEncoder to encode categorical variables.
- Used StandardScaler to scale numerical features.
- Balanced class distribution using *SMOTE* (Synthetic Minority Over-sampling Technique).

### 4. Exploratory Data Analysis (EDA)
- Visualized attrition distribution by department and job role using seaborn plots.
- Generated correlation heatmaps and countplots to uncover relationships.

### 5. Model Training
Trained and evaluated the following classification models:
- *Logistic Regression*
- *Random Forest*
- *XGBoost Classifier*

Used 5-fold cross-validation with *Recall* as the main performance metric to minimize false negatives.

| Model              | Avg Recall |
|-------------------|------------|
| Logistic Regression | 0.8054     |
| Random Forest       | 0.9101     |
| XGBoost             | 0.8413     |

### 6. Evaluation
- Evaluated models using *confusion matrix, **precision, **recall, **F1-score, and **accuracy*.
- Prioritized recall to catch employees who are likely to leave.

### 7. Feature Importance
- Extracted top features influencing attrition using RandomForestClassifier.feature_importances_.

---

##  Key Insights

- Employees doing *OverTime, in **Sales* or *R&D* departments, or with low *job satisfaction*, were more likely to leave.
- Random Forest gave the highest recall, making it a strong candidate for HR prediction pipelines.

---

##  Files Included

- Employee_Attrition_Prediction.ipynb: The complete notebook.
- README.md: This file.

---

##  Demo Video



---

##  Conclusion

This machine learning project demonstrates how predictive analytics can assist HR teams in identifying attrition risks early, allowing them to take targeted employee engagement or retention actions.

---

##  Links

-  [Kaggle Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
-  [Project Inspiration](https://www.ibm.com/analytics/hr-employee-attrition)

---

##  Author

*[muhammad ali]*
Data Science Student – Week 4 Project
