
# 🦟 Dengue Prediction Using Machine Learning

### A Machine Learning Approach to Dengue Classification Using Hematological Data

Dengue is one of the major public health concerns in Bangladesh. Early identification of dengue cases can help support timely medical assessment and patient management.

This project explores the application of Machine Learning techniques to classify dengue-positive and dengue-negative cases using patients' hematological data. It involves Exploratory Data Analysis (EDA), data preprocessing, model development, hyperparameter tuning, performance evaluation, and Explainable AI.

The primary objective was to compare different machine learning algorithms and identify a model that performs effectively on the available dataset.

---

## 📌 Project Overview

The project uses clinical hematological features to develop a binary classification system for dengue prediction.

Rather than relying on a single algorithm, multiple machine learning models were implemented and evaluated to compare their predictive performance.

**Key objectives:**
- Explore and understand the dataset through EDA.
- Identify data distributions, patterns, and potential outliers.
- Perform data cleaning and preprocessing.
- Train and compare different machine learning classifiers.
- Optimize model performance through hyperparameter tuning.
- Evaluate models using multiple performance metrics.
- Interpret model predictions using LIME (Explainable AI).

---

## 📂 Dataset Information

**Dataset:** Dengue Fever Hematological Dataset: Clinical Insights for Improved Diagnosis and Patient Management

**Source:** [Mendeley Data](https://data.mendeley.com/)

The dataset contains 1,523 patient records and 18 features, including demographic and hematological information.

### Features

| Category | Features |
|---|---|
| Demographic | Gender, Age |
| Blood Parameters | Hemoglobin, RBC, HCT |
| White Blood Cell Parameters | Neutrophils, Lymphocytes, Monocytes, Eosinophils, Total WBC |
| Red Blood Cell Indices | MCV, MCH, MCHC, RDW-CV |
| Platelet Parameters | Total Platelet Count, MPV, PDW, PCT |

**Target variable:** Dengue classification (Positive / Negative).

The original dataset contained:
- 1,042 dengue-positive cases.
- 482 dengue-negative cases.

After removing duplicate records, 1,511 samples remained.

---

## 🔍 Exploratory Data Analysis (EDA)

EDA was performed to understand the underlying structure and characteristics of the dataset before applying machine learning algorithms.

The following visualisation techniques were used:

- **Histograms:** To understand the distribution of numerical features.
- **Violin Plots:** To compare feature distributions between dengue-positive and dengue-negative cases.
- **Boxplots:** To identify potential outliers.
- **KDE Plots:** To examine the density and distribution patterns of selected features.
- **Correlation Heatmap:** To explore relationships between numerical variables.

These visualisations helped identify patterns in the data, particularly differences in hematological parameters between the two classes.

---

## ⚙️ Data Preprocessing

The following preprocessing steps were performed:

1. Checked for missing values.
2. Removed duplicate records.
3. Examined potential outliers using boxplots.
4. Applied Label Encoding to the categorical gender feature.
5. Used Min-Max Scaling for numerical feature scaling.
6. Applied SMOTE to address class imbalance.
7. Split the dataset into training and testing sets using an 80:20 ratio with stratification.

---

## 🤖 Machine Learning Models

Several classification algorithms were implemented and compared.

### Individual Classifiers

- Logistic Regression
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Naive Bayes
- Decision Tree
- Random Forest

### Boosting Algorithms

- AdaBoost
- XGBoost
- Gradient Boosting

### Ensemble Learning

- Stacking
- Blending

Different combinations of models were also explored to investigate whether ensemble learning could improve predictive performance.

---

## 🎯 Hyperparameter Optimization

To improve model performance, hyperparameter tuning was performed using:

- GridSearchCV
- RandomizedSearchCV

The optimization process focused on finding suitable parameter combinations for the different machine learning algorithms.

---

## 📊 Model Evaluation

Models were evaluated using multiple performance metrics:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC Curve and AUC

### Model Performance After Hyperparameter Tuning

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Random Forest | **82.30%** | 0.82 | 0.82 | **0.80** |
| Decision Tree | 77.38% | 0.75 | 0.77 | 0.75 |
| AdaBoost | 72.79% | 0.72 | 0.73 | 0.72 |
| XGBoost | 79.02% | 0.80 | 0.79 | 0.76 |
| Stacking | 80.98% | 0.80 | 0.81 | 0.78 |
| Blending | 78.03% | 0.79 | 0.78 | 0.75 |
| SVM | 74.75% | 0.74 | 0.75 | 0.71 |
| Logistic Regression | 74.75% | 0.75 | 0.75 | 0.71 |
| Naive Bayes | 72.13% | 0.72 | 0.72 | 0.66 |
| KNN | 74.42% | 0.73 | 0.74 | 0.71 |

### Best Performing Model

The **Random Forest classifier** achieved the highest accuracy of 82.30%, with an F1-score of 0.80 after hyperparameter optimization using GridSearchCV.

Its optimized hyperparameters included:

- Number of estimators: 100
- Maximum depth: 5

The ROC-AUC score of the optimized Random Forest model was 0.73.

---

## 🧠 Explainable AI (XAI) – LIME

Beyond evaluating predictive performance, the project also explored model interpretability using **LIME (Local Interpretable Model-Agnostic Explanations)**.

LIME was applied to the best-performing Random Forest model to understand how individual hematological features influenced its predictions.

For an example positive prediction, the model assigned a 69% confidence score to the positive class.

Features such as:
- Neutrophils
- PCT
- Monocytes
- RDW-CV
- MCV
- RBC

were identified as influential in that particular prediction.

This provided a better understanding of how the model arrived at its classification decisions.

---

## 🛠️ Technologies & Tools

- **Programming Language:** Python
- **Data Analysis:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Boosting:** XGBoost
- **Imbalanced Data Handling:** Imbalanced-learn (SMOTE)
- **Explainable AI:** LIME
- **Model Optimization:** GridSearchCV, RandomizedSearchCV

---

## 📁 Project Workflow

1. Dataset Collection
2. Exploratory Data Analysis
3. Data Cleaning and Preprocessing
4. Feature Scaling and Encoding
5. Train-Test Split
6. SMOTE Sampling
7. Machine Learning Model Development
8. Hyperparameter Optimization
9. Model Evaluation and Comparison
10. Explainable AI Using LIME

---

## 💡 Key Learnings

Working on this project helped me develop a better understanding of the complete machine learning workflow.

Some of the key things I learned:

- How to explore and interpret real-world clinical datasets.
- Why EDA is important before building predictive models.
- How different machine learning algorithms behave on the same dataset.
- The importance of hyperparameter tuning and model evaluation.
- Why accuracy alone is not enough to judge a classification model.
- How Explainable AI can help interpret individual model predictions.

Most importantly, I learned that developing a machine learning model is not just about achieving a high accuracy score. Understanding the data, evaluating the results, and interpreting model behaviour are equally important.

---

## ⚠️ Limitations

This project was developed for academic and educational purposes.

The model was trained and evaluated on a limited public dataset. Its performance does not establish clinical reliability or suitability for real-world medical diagnosis.

Further validation using larger, diverse, and independently collected clinical datasets would be necessary before considering any practical healthcare application.

---

## 👨‍💻 Author

**Minhazur Rahman**

BSc in Computer Science & Engineering  
North South University, Dhaka, Bangladesh

Currently pursuing MSc in Data Science at Kingston University, London, UK.

**GitHub:** [Minhazflop](https://github.com/Minhazflop)

---

*An academic project exploring the application of Machine Learning and Explainable AI to dengue classification.*
