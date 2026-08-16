The project focuses on feature engineering and data preprocessing for the Heart Disease Prediction Dataset. The objective is to prepare patient clinical data for machine-learning models that predict whether heart disease is present.

The final output is a cleaned and machine-learning-ready dataset suitable for binary classification modelling.

Business Problem
Heart disease is a major healthcare concern. Healthcare professionals use patient demographic, clinical, and exercise-related information to assess possible cardiovascular risk.

This project prepares a dataset that can support a machine-learning model for predicting the presence of heart disease. The result should be considered a decision-support tool for preliminary screening and not a replacement for clinical diagnosis.

Dataset
Dataset: Heart Failure Prediction Dataset
Source: https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction

The dataset contains 918 patient records, 11 predictor variables, and one target variable. It includes clinical features such as age, sex, chest pain type, resting blood pressure, cholesterol, fasting blood sugar, ECG results, maximum heart rate, exercise-induced angina, ST depression, and ST-slope. The dataset supports the prediction of heart disease presence.

Target Variable
The target variable is HeartDisease.

0 = No heart disease

1 = Heart disease present

This makes the project a binary classification problem.

Project Tasks
The project includes the following tasks:

Business understanding

Dataset inspection

Missing-value assessment

Duplicate-record detection

Data-type validation

Categorical feature encoding

Numerical feature scaling

Outlier detection using boxplots and the IQR method

Correlation analysis

Feature importance analysis using Random Forest

Creation of cleaned and machine-learning-ready datasets

Data visualisation

Preprocessing Steps
Data Cleaning
Checked for missing values.

Checked for duplicate records.

Validated data types.

Preserved the original cleaned dataset separately.

Feature Engineering
No additional derived clinical features were created. The original variables were retained to preserve detailed clinical information and avoid unnecessary complexity.

Encoding
Binary categorical variables (Sex and ExerciseAngina) were encoded as 0 and 1.

Multi-category variables (ChestPainType, RestingECG, and ST_Slope) were transformed using one-hot encoding.

drop_first=True was used to reduce redundant dummy variables.

Feature Scaling
StandardScaler was applied to the following continuous numerical variables:

Age

RestingBP

Cholesterol

MaxHR

Oldpeak

Binary variables and the target variable were not scaled.

Outlier Detection
Outliers were assessed using boxplots and the Interquartile Range method.

Potential outliers were identified in RestingBP, Cholesterol, MaxHR, and Oldpeak. The observations were retained because extreme clinical measurements may contain useful information for identifying high-risk patients.

Feature Selection
Feature selection was supported by:

Correlation heatmap

Correlation analysis

Random Forest feature importance

Important features identified included ST-slope categories, Oldpeak, Cholesterol, MaxHR, Age, ExerciseAngina, and RestingBP.

Visualisations
The project includes the following visualisations:

Heart disease target distribution count plot

Age histogram by heart disease status

Cholesterol histogram by heart disease status

Resting blood pressure box plot

Chest pain type count plot

Age versus maximum heart rate scatter plot

Correlation heatmap

Random Forest feature-importance chart

Tools and Libraries
Python

Jupyter Notebook

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn
