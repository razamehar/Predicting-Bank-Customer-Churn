# Predicting-Bank-Customer-Churn
This project aims to predict bank customer churn using a dataset derived from the Bank Customer Churn Prediction dataset available on Kaggle. The dataset used in this project has been generated from a deep learning model trained on the original dataset, resulting in feature distributions that are similar but not identical to the original data. Additionally, synthetic data has been generated separately from the Kaggle data to address class imbalance using an oversampling technique called SMOTE.

# Analysis Steps:
## Univariate Analysis:
1. Visualizing Categorical Features such as geography and gender
2. Visualizing Numerical Features such as Credit Score, Age, Tenure, Balance, Number of Products, Estimated Salary

## Bivariate Analysis:
1. Exploring Relationships Between Numerical Predictors and Target Variable:
2. Churn and Credit Score, Age, Tenure, Balance, Number of Products, Estimated Salary, Has Credit Card, Is Active member
3. Exploring Relationships Between Categorical Predictors and Target Variable:
4. Churn count with Gender and Geography

## Correlation Analysis:
Examining Relationships Between Numerical Predictors and Target Variable using Point-Biserial Correlation as the target variable is binary.

# Feature Engineering and Oversampling:
To enhance the model's performance, a new feature was introduced that calculates the ratio between the Balance and EstimatedSalary variables. Additionally, to address the class imbalance issue within the dataset (Class 1 comprises only 21% of the total data), an oversampling technique like SMOTE was employed to generate synthetic data.

# Predictive Modeling:
## Model Selection and Hyperparameter Tuning with Cross Validation:
1. Explored various configurations for the K-Neighbors, Decision Tree, Random Forest, AdaBoost models, and XGBoost classifiers using 80% of the data for training while reserving 20% as a hold-out set.
2. Subjected model parameters to k-fold cross-validation (k = 10) to identify the best-performing configurations.
3. Selected Random Forest, Extra Tree, and XGBoosting classifiers for hyperparameter tuning based on their higher ROC AUC scores (more than 95%).
4. fter exhaustive grid search, identified the best hyperparameters for each model.
5. Evaluated models using a 10-fold cross-validation approach, employing ROC AUC score as a key metric.

## Model Evaluation:
1. The optimal model (XGB Classifier) was trained on 100% of the training data and evaluated on the reserved holdout set.
2. Model stacking and blending were employed but reduced the performance significantly, hence were not utilized.
3. The optimal model performs well on both the training and the hold-out datasets.

## Feature Importance: Model interpretability using SHAP (Shapley Additive Explanations) Summary Plot.
Achieved model interpretability through visualization of SHAP (Shapley Additive Explanations) summary plot.

# Findings & Observations:
Findings and observations are based on univariate, multivariate analysis, and correlation analysis.

# Recommendations:
The strategies will contribute not only to the retention of existing customers but also to the acquisition of new customers.

## Usage
### Prerequisites
- Python 3.10.12

# License
This project is licensed under the Raza Mehar License. See the [LICENSE.md](LICENSE.md) file for details.

# Contact
For any questions or clarifications, please contact Raza Mehar at [raza.mehar@gmail.com].
