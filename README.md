Customer Churn Prediction
-->Project Overview

This project focuses on predicting customer churn using machine learning techniques. Customer churn prediction helps businesses identify customers who are likely to discontinue services, enabling proactive retention strategies and improved customer relationship management.

The project follows a complete end-to-end Data Science workflow including:

Data Understanding & EDA
Data Preprocessing
Feature Engineering
Model Building
Model Evaluation
Hyperparameter Tuning
Business Insights
-->Business Problem

Customer retention is critical for subscription-based businesses. Acquiring new customers is often more expensive than retaining existing ones. The objective of this project is to build a predictive model that identifies customers who are likely to churn based on customer demographics, account information, service usage, and billing patterns.

-->Project Structure
customer-churn-prediction/
│
├── data/
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_modeling.ipynb
│
├── README.md
--> Dataset

Dataset Used:

IBM Telco Customer Churn Dataset

The dataset contains customer-level information such as:

Demographics
Subscription details
Service usage
Billing information
Contract information
Churn status
-->Exploratory Data Analysis (EDA)

Performed detailed exploratory data analysis to understand:

Data types
Missing values
Numerical and categorical feature distributions
Customer churn patterns
Feature relationships
Outliers and skewness
Key EDA Insights
Customers with shorter tenure showed higher churn probability.
Month-to-month contract customers had higher churn rates.
Higher monthly charges were associated with increased churn.
Dataset showed moderate class imbalance.
Visualizations Used
Histograms
Boxplots
Countplots
Correlation Heatmaps
-->Data Preprocessing

The following preprocessing steps were performed:

✔ Data Cleaning
Identified datatype inconsistencies in TotalCharges
Converted TotalCharges from string to numeric datatype
Removed rows with missing values
✔ Encoding
Label Encoding for binary categorical variables
One-Hot Encoding for multi-category variables
✔ Feature Scaling
StandardScaler applied for Logistic Regression model
✔ Train-Test Split
Dataset split into training and testing sets using train_test_split
-->Models Implemented

The following machine learning models were built and evaluated:

1. Logistic Regression
Baseline classification model
Performed well with stable generalization
2. Decision Tree Classifier
Captured nonlinear relationships
Observed overfitting and weaker generalization
3. Random Forest Classifier
Improved stability over Decision Tree
Better generalization performance
4. Tuned Random Forest Classifier
Hyperparameter tuning performed using GridSearchCV
Achieved best overall balanced performance
--> Model Evaluation

Evaluation metrics used:

Accuracy
Precision
Recall
F1-Score
Confusion Matrix
Cross Validation
-->Cross Validation

Used:

Stratified K-Fold Cross Validation

Purpose:

Validate model stability
Improve generalization assessment
Handle class imbalance more effectively
-->Hyperparameter Tuning

Performed hyperparameter tuning on Random Forest using:

GridSearchCV

Parameters tuned:

n_estimators
max_depth
min_samples_split
min_samples_leaf
-->Final Model Selection
Selected Model:
Tuned Random Forest Classifier
Reason for Selection
Best overall balance between:
Accuracy
Precision
Recall
F1-score
Improved generalization performance after tuning
Reduced overfitting compared to standalone Decision Tree
-->Key Business Insights
Customers with shorter tenure are more likely to churn.
Month-to-month contract customers show significantly higher churn rates.
Higher monthly charges correlate with increased churn probability.
Long-term customers tend to remain more stable and loyal.
--> Technologies & Libraries Used
Programming Language
Python
Libraries
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Machine Learning Techniques
Classification
Feature Engineering
Hyperparameter Tuning
Cross Validation
-->Future Improvements

Potential enhancements:

SMOTE / imbalance handling
XGBoost implementation
ROC-AUC optimization
Threshold tuning
Model deployment using Flask/FastAPI
ML pipeline automation
-->Conclusion

This project demonstrates a complete machine learning workflow for customer churn prediction. Multiple machine learning models were explored, evaluated, and compared using business-oriented metrics. Hyperparameter tuning and cross-validation were applied to improve model performance and generalization capability.

The final tuned Random Forest model provided the best overall performance and can help businesses proactively identify high-risk customers and improve retention strategies.