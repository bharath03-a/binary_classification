# Vehicle Insurance Prediction

This repository focuses on predicting vehicle insurance response using machine learning techniques. The project involves data preprocessing, exploratory data analysis, feature engineering, model training, and evaluation with multiple classifiers.

## Table of Contents

1. [Introduction](#introduction)
2. [Data Overview](#data-overview)
3. [Exploratory Data Analysis](#exploratory-data-analysis)
4. [Feature Engineering](#feature-engineering)
5. [Modeling](#modeling)
6. [Evaluation](#evaluation)
7. [How to Use](#how-to-use)
8. [Dependencies](#dependencies)
9. [Contributing](#contributing)
10. [License](#license)

## Introduction

The project aims to predict whether a customer will respond positively to a vehicle insurance offer. Techniques such as data balancing (using SMOTE), scaling, and log transformations are applied to enhance model performance.

## Data Overview

The data comes from a vehicle insurance dataset, containing features such as:
- `Gender`
- `Age`
- `Driving_License`
- `Region_Code`
- `Previously_Insured`
- `Vehicle_Age`
- `Vehicle_Damage`
- `Annual_Premium`
- `Policy_Sales_Channel`
- `Vintage`
- `Response` (target variable)

The dataset consists of training (`train.csv`) and testing (`test.csv`) files.

## Exploratory Data Analysis

EDA revealed insights such as:
- Imbalanced target variable.
- Skewed distributions in certain features like `Age` and `Annual_Premium`.
- Identification of outliers in features like `Annual_Premium`.

Visualizations include bar plots, pie charts, histograms, and box plots for feature understanding.

## Feature Engineering

### Techniques applied:
- One-Hot Encoding for categorical variables (`Gender`, `Vehicle_Age`, etc.).
- Log Transformation for skewed features (`Age`).
- Standard Scaling to normalize numerical features.
- Balancing the dataset using SMOTE to address class imbalance.

## Modeling

The following models were implemented and evaluated:
1. **Logistic Regression**:
   - Achieved high recall but moderate overall accuracy.
2. **XGBoost**:
   - Provided the best performance with high accuracy and F1 score.
3. **Decision Tree**:
   - Overfit on the training data but gave decent testing accuracy.

### Evaluation Metrics:
- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score

### Hyperparameter Tuning:
Hyperparameter tuning was performed using `GridSearchCV` for Logistic Regression, but it was computationally intensive and interrupted.

## Predictions

Predictions for the test set were generated using the Logistic Regression model due to its superior recall for this use case. Results were saved in `submission.csv`.

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/bharath03-a/binary_classification
