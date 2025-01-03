# Machine Learning Workflow Automation for Regression Tasks

## Introduction

This project implements a machine learning pipeline configured dynamically using a JSON file. While the task requirements were designed to support both regression and classification tasks, this implementation focuses exclusively on regression workflows. The solution automates data preprocessing, feature engineering, model selection, hyperparameter tuning, and evaluation for regression models.

## Problem Statement

The task involved automating a machine learning workflow for both regression and classification tasks using a JSON configuration file. The pipeline needed to:

1. **Target Identification:** Extract the target variable and prediction type (regression or classification) from the JSON file.
2. **Data Preprocessing:** Handle missing values and apply transformations as per JSON instructions.
3. **Feature Engineering:** Perform feature generation and reduction dynamically.
4. **Model Selection:** Dynamically configure models based on the task type and selected algorithms.
5. **Hyperparameter Tuning:** Optimize model performance using GridSearchCV.
6. **Evaluation:** Log relevant metrics (e.g., RMSE for regression, AUC for classification).
7. **Reusability:** Ensure the pipeline works for both regression and classification with minimal adjustments.

## My Implementation

This project focuses specifically on regression tasks. Key components of the implementation are:

### JSON Parsing
- Extract configuration details such as target variable, prediction type, features, and selected algorithms.
- Adapt the workflow based on the JSON file dynamically.

### Data Preprocessing
- Load the dataset and handle missing values as defined in the JSON (e.g., mean, median, or custom values).
- Apply scaling or normalization for numerical features.

### Feature Engineering
- Generate linear and polynomial interactions as specified.
- Perform dimensionality reduction using techniques like PCA or Tree-based methods.

### Model Pipeline
- Build regression models like Random Forest Regressor and Ridge Regression based on JSON configurations.
- Optimize model hyperparameters using GridSearchCV.
- Integrate preprocessing, feature engineering, and model training into a single scikit-learn pipeline.

### Evaluation
- Compute metrics such as RMSE, MAE, and R² for regression tasks.
- Log results for comparison and analysis.

## How to Use

1. **Setup the Project**
   - Clone the repository and install dependencies:
     ```bash
     git clone <repository_url>
     cd <repository_directory>
     pip install -r requirements.txt
     ```

2. **Run the Workflow**
   - Place the dataset (`iris.csv`) JSON file('algoparams_from_ui.json') in the project folder.
   - Execute the notebook (`FinalSolution.ipynb`) to run the pipeline.

3. **Modify the JSON**
   - Update `algoparams_from_ui.json` to test different configurations (e.g., enable/disable algorithms, change hyperparameters).

## Project Files

- **`algoparams_from_ui.json`**: Configuration file containing workflow parameters.
- **`FinalSolution.ipynb`**: Jupyter notebook implementing the regression pipeline.
- **`Screening Test - DS.docx`**: Document outlining the task requirements and problem statement.

## Tools and Libraries

- **Programming Language:** Python
- **Libraries:** pandas, numpy, scikit-learn
- **Notebook Environment:** VS Code

## Regression Models Used

- Random Forest Regressor
- Linear Regression
- Ridge Regression
- Decision Tree Regressor

## Learnings and Challenges

- Understood how to automate regression workflows using JSON configurations.
- Enhanced skills in building reusable and dynamic pipelines.
- Faced challenges in generalizing the pipeline for both regression and classification but focused on completing the regression task effectively.


