
# Dengue Prediction Using Machine Learning

This project aims to develop a machine learning-based system to predict the likelihood of dengue outbreaks based on climatic and seasonal data. The goal is to enhance early warning capabilities, allowing healthcare providers and governments to act promptly to mitigate the effects of dengue fever.

## Table of Contents

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Dataset Description](#dataset-description)
- [Methodology](#methodology)
- [Technologies Used](#technologies-used)
- [Results and Findings](#results-and-findings)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [Contributors](#contributors)

---

## Project Overview

Dengue is a mosquito-borne viral infection prevalent in tropical and subtropical regions. Predicting outbreaks is essential for timely preventive measures. This project uses machine learning models to analyse environmental features and indicate the number of dengue cases with high accuracy.

## Problem Statement

Traditional methods for forecasting dengue outbreaks are often delayed or inaccurate. There is a need for a reliable predictive model that uses environmental and climate data to anticipate dengue trends and help public health authorities prepare effectively.

## Objectives

- Analyze dengue trends and climatic influences.
- Apply machine learning algorithms to build predictive models.
- Evaluate and compare model performance.
- Provide insights to aid in dengue outbreak prevention.

## Dataset Description

Total Samples: 1523

Total Features: 18 input features + 1 output label

Type of Data: Structured, tabular medical diagnostic data

Label Column: Result (Categorical: positive, negative)


## Methodology

The following steps were followed:

1. **Data Preprocessing**: Handling missing values, feature engineering, and normalization.
2. **Exploratory Data Analysis (EDA)**: Understanding data distributions and correlations.
3. **Model Building**:
   - Linear Regression
   - Random Forest Regressor
   - XGBoost
   - Gradient Boosting
4. **Evaluation Metrics**:
   | Metric                   | Description                                                                                                                                                   |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Accuracy**             | Measures the proportion of correctly predicted instances (both positives and negatives). <br> **Formula:** `(TP + TN) / (TP + TN + FP + FN)`                  |
| **Precision**            | Measures how many of the predicted positive cases were actually positive. <br> **Formula:** `TP / (TP + FP)`                                                  |
| **Recall (Sensitivity)** | Measures how many actual positive cases were correctly identified. <br> **Formula:** `TP / (TP + FN)`                                                         |
| **F1 Score**             | Harmonic mean of Precision and Recall; balances false positives and false negatives. <br> **Formula:** `2 * (Precision * Recall) / (Precision + Recall)`      |
| **ROC-AUC Score**        | Area under the Receiver Operating Characteristic curve; evaluates the classifier’s ability to distinguish between classes.                                    |
| **Confusion Matrix**     | Displays the counts of true positives (TP), true negatives (TN), false positives (FP), and false negatives (FN) to give a full overview of model performance. |


## Technologies Used

- Python (Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn)
- Jupyter Notebook
- Google Colab
- Microsoft Word (for documentation)

## Results and Findings

- Among the models, the Random Forest and Gradient Boosting Regressors showed the best performance.
- Feature importance analysis indicated temperature and humidity as critical predictors of dengue outbreaks.

## Conclusion

Machine learning models, particularly ensemble methods like Random Forest and Gradient Boosting, offer a powerful tool for predicting dengue outbreaks using climatic data. These models can significantly aid public health planning and resource allocation.

## Future Work

- Incorporate real-time data from health departments.
- Deploy the model as a web or mobile application.
- Integrate additional environmental factors such as urbanization or population density.

## Contributors

- Minhazur Rahman
"""
