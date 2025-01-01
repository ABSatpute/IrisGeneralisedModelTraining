Features
Dynamic JSON Parsing

Reads configuration parameters for target variable, prediction type, feature handling, and hyperparameter tuning.
Adapts to any valid JSON input format.
Preprocessing

Handles missing data with imputation strategies (e.g., mean, median, mode).
Standardizes or scales feature data.
Feature Reduction

Supports multiple methods:
No Reduction
Correlation with Target
Tree-based Selection
Principal Component Analysis (PCA)
Model Selection

Automatically chooses appropriate models for regression or classification based on JSON configuration.
Current models supported for regression:
Random Forest Regressor
Decision Tree Regressor
Linear Regression
Hyperparameter Tuning

Performs grid search using GridSearchCV to find optimal parameters.
Pipeline Implementation

Uses Pipeline from scikit-learn for modular execution of preprocessing, feature reduction, and model training.
Metrics Logging

Logs standard evaluation metrics:
Regression: MAE, MSE, R²
Requirements
Install the required Python packages using:

bash
Copy code
pip install -r requirements.txt  
Requirements File
numpy==1.24.3
pandas==1.5.3
scikit-learn==1.2.2
matplotlib
joblib
scipy
