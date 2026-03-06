# ARTI308 Lab 5 – Feature Engineering (Classification)

## Overview
This lab demonstrates a complete machine learning workflow for predicting vehicle price categories using a dataset of car attributes. The goal is to classify vehicles into price groups represented by the target variable `Price_Category`.

The notebook covers the full pipeline from data exploration and preprocessing to model training, evaluation, and interpretation.

---

## Dataset Description
The dataset contains information about vehicles and their specifications.

Main features include:

- `Car ID` – Unique identifier for each vehicle
- `Brand` – Manufacturer of the vehicle
- `Model` – Vehicle model name
- `Year` – Manufacturing year
- `Engine Size` – Engine capacity
- `Fuel Type` – Type of fuel used
- `Transmission` – Transmission type
- `Mileage` – Total distance driven
- `Condition` – Vehicle condition
- `Price` – Vehicle market price
- `Price_Category` – Target variable derived from price

---

## Machine Learning Workflow

The lab follows a structured machine learning pipeline:

1. Dataset inspection and validation  
2. Target variable analysis  
3. Feature type identification  
4. Data leakage prevention  
5. Feature engineering  
6. Reducing high-cardinality categories  
7. Preparing features for modeling  
8. Train/Test split  
9. Encoding categorical variables  
10. Training a Random Forest classifier  
11. Model evaluation  
12. Feature importance analysis  
13. Optional feature selection  

---

## Feature Engineering

Several new features were created to improve model performance:

- `Car_Age` – Age of the vehicle calculated from `Year`
- `Mileage_per_Year` – Average mileage driven per year
- `Engine_per_Age` – Engine size relative to vehicle age
- `Mileage_per_Engine` – Mileage relative to engine capacity
- `Model_reduced` – Reduced version of `Model` to control high-cardinality categories

These features help the model capture patterns related to vehicle usage and depreciation.

---

## Model Selection

A **Random Forest classifier** was used as the baseline model because it:

- Handles both numerical and categorical variables
- Captures non-linear relationships
- Is robust to noise
- Provides feature importance for interpretation

Categorical variables were encoded using **One-Hot Encoding** before training the model.

---

## Model Evaluation

Model performance was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

These metrics help assess how well the model predicts each price category.

---

## Feature Importance

Random Forest provides feature importance scores that indicate which attributes most influence predictions. Important features typically include:

- Mileage
- Car_Age
- Engine Size
- Mileage_per_Year
- Brand
- Model_reduced

This helps interpret the model and understand the factors affecting vehicle price classification.

---

## Feature Selection (Optional)

Feature selection was performed using `SelectFromModel`, which keeps only the most important features based on Random Forest importance scores. This can reduce model complexity while maintaining similar performance.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Conclusion


This lab demonstrates how machine learning can be applied to structured datasets using feature engineering, categorical encoding, and ensemble models. The Random Forest model successfully learns patterns in vehicle attributes to classify cars into different price categories.
