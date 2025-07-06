# 💳 Credit-Carn-Customer-Churn-Prediction

This repository contains code and analysis for predicting Credit Card Customer Churn. The project uses EDA, feature engineering, and multiple machine learning models to identify customers likely to leave the credit card service, helping banks retain valuable customers.

# 📂 Dataset

- Source: Kaggle Dataset

- Size: ~10,000 customer records

- Features: Demographic, transaction, and credit-related attributes

- Target: Attrition_Flag (Existing or Attrited Customer)

# 📝 Problem Statement

Churn prediction helps banks and financial institutions identify customers likely to stop using their services. Early detection enables proactive retention strategies, saving costs and improving customer satisfaction.

# 🧪 Project Workflow

# 1. Data Preprocessing

- Checked for:

  - Null values → none found

  - Duplicate entries → none found

- Dropped unnecessary columns (e.g. Naive Bayes classifier outputs)

- Encoded categorical variables via one-hot encoding

- Scaled numeric features using Min-Max Scaler

# 2. Exploratory Data Analysis (EDA)

- Pie charts of churned vs. existing customers

- Gender distribution among churned and non-churned customers

- Histograms for:

  - Credit Limit

  - Revolving Balance

  - Average Open to Buy

  - Transaction Amounts

  - Utilization Ratio

- Box plots of numerical features vs. churn status

- Correlation heatmap to detect multicollinearity

- Scatterplots of correlated features

# Key EDA Insights:

- Churn rate in the dataset is ~16%

- Female customers show slightly higher churn rates

- Several financial attributes differ significantly between churned and non-churned groups

- Many numeric features are skewed or multi-modal

# 3. Feature Engineering

- One-hot encoding for:

  - Gender

  - Education Level

  - Marital Status

  - Income Category

  - Card Category

- Scaled all numeric features to [0, 1] range

# 4. Modeling

- Models Trained:
  
  - AdaBoost Classifier

  - Gradient Boosting Classifier

  - Random Forest Classifier

  - Extra Trees Classifier

  - Decision Tree Classifier

  - Support Vector Machine

  - Bagging Classifier

- Cross-validation:

  - Stratified 8-fold CV

  - Metrics recorded:

    - Accuracy

    - F1-score

    - Confusion Matrix

# 5. Ensemble Model

Built a Voting Classifier to combine predictions from all models for improved robustness and accuracy.

# 📊 Results

- From the ensemble of models:

- Gradient Boosting achieved the highest single-model accuracy ~96.69%

- SVM was the least accurate but still above 90%

- Ensemble Voting Classifier offered robust overall performance

# 💡 Key Findings

- Customers with higher transaction activity are less likely to churn.

- Lower credit limits and higher revolving balances correlate with churn.

- Demographic factors (like marital status and education) show noticeable differences in churn probability.

# Libraries

- scikit-learn

- seaborn

- matplotlib

- pandas

- numpy

- xgboost
