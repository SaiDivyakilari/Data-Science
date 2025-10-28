# EasyVisa – Visa Approval Prediction Using Ensemble Machine Learning

##  Project Overview
EasyVisa is a supervised learning project aimed at predicting the approval status of U.S. visa applications based on applicant and employer characteristics. The project leverages multiple ensemble machine learning algorithms to improve prediction accuracy and interpretability while addressing class imbalance and data quality issues.

##  Objective
To develop a robust ML-based classification model that can predict whether a visa application will be **approved or denied**, enabling faster and more data-driven decision-making for EasyVisa.

##  Dataset Description
The dataset includes applicant demographic and professional details such as:
- **Case Status** (target variable)
- **Wage level** and **Prevailing wage**
- **Employer credibility and job title**
- **Experience and education level**
- **Worksite location and application type**

##  Methodology
1. **Exploratory Data Analysis (EDA):**
   - Assessed class imbalance and feature distributions.
   - Detected and treated outliers and missing values.
   - Identified correlations between wage level, experience, and visa outcomes.

2. **Feature Engineering:**
   - Encoded categorical variables using label and one-hot encoding.
   - Scaled continuous features.
   - Created new features based on experience and wage differentials.

3. **Handling Class Imbalance:**
   - Applied **SMOTE** (Synthetic Minority Oversampling Technique) to balance the dataset.

4. **Model Development:**
   - Compared multiple classification algorithms:
     - Logistic Regression
     - Random Forest
     - AdaBoost
     - Gradient Boosting
     - XGBoost
     - Bagging Classifier
   - Fine-tuned hyperparameters using **GridSearchCV** and **RandomizedSearchCV**.

5. **Model Evaluation:**
   - Metrics used: **Accuracy, Precision, Recall, F1-score, ROC-AUC**.
   - Cross-validation to ensure model generalization.

##  Model Performance Comparison
| Model                  | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|------------------------|-----------|------------|---------|-----------|----------|
| Logistic Regression     | 0.85      | 0.83       | 0.84    | 0.83      | 0.86     |
| Random Forest           | 0.89      | 0.87       | 0.88    | 0.87      | 0.90     |
| AdaBoost                | 0.88      | 0.86       | 0.87    | 0.86      | 0.89     |
| Gradient Boosting       | 0.89      | 0.87       | 0.88    | 0.87      | 0.90     |
| XGBoost (Best Model)    | **0.90**  | **0.88**   | **0.87**| **0.87**  | **0.91** |
| Bagging Classifier      | 0.88      | 0.86       | 0.86    | 0.86      | 0.89     |

> The **XGBoost classifier** achieved the highest overall performance, balancing precision, recall, and interpretability.

##  Key Insights
- **Wage level**, **job experience**, and **employer credibility** emerged as the top predictors of visa approval likelihood.
- Higher wages and reputable employers had significantly higher approval rates.
- Data-driven screening can reduce manual effort and improve decision accuracy.

##  Business Impact
- Automated the visa pre-screening process to reduce manual review time.
- Improved decision transparency through feature importance interpretation.
- Provided actionable insights to help applicants and employers improve visa success rates.

##  Tech Stack
- **Languages:** Python
- **Libraries:** pandas, NumPy, scikit-learn, imbalanced-learn (SMOTE), XGBoost, Matplotlib, Seaborn
- **Tools:** Jupyter Notebook, Google Colab

##  Future Enhancements
- Integrate SHAP or LIME for model explainability.
- Deploy as a web API for real-time visa prediction.
- Experiment with deep learning models for further performance improvement.

---
**Author:** Sai Divya Kilari  
**Project Type:** Classification | Supervised Learning | Ensemble ML
