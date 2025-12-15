# Healthcare Readmission Prediction

This project focuses on predicting hospital readmissions within 30 days using patient demographic and clinical data from the UCI Machine Learning Repository.

## Dataset
- Diabetes 130-US Hospitals for Years 1999–2008  
- Source: UCI Machine Learning Repository  

## Project Structure
- data/raw/ – Original dataset (unchanged)  
- data/processed/ – Cleaned dataset used for analysis and modeling  
- notebooks/  
  - 01_data_cleaning.ipynb – Data cleaning and feature preparation  
  - 02_eda.ipynb – Exploratory data analysis  
  - 03_modeling.ipynb – Model training and evaluation and comparison 
- models/
  -  logistic_regression.pkl - Saved trained model artifact


## Methods
- Performed data cleaning and feature selection
- Created a target variable (`readmitted_30`) indicating readmission within 30 days
- Conducted exploratory data analysis to understand distributions and class imbalance
- Split data into training and testing sets using stratification
- Applied preprocessing with one-hot encoding for categorical variables
- Examined distributions of key variables using histograms and bar charts
- Calculated summary statistics for numerical features
- Trained and evaluated Logistic Regression and Random Forest models
- Evaluated models using:
  - Precision, recall, and F1-score
  - ROC-AUC
- Saved the trained Logistic Regression model as a reusable artifact

## Results
- Logistic Regression gave more balanced recall for identifying readmitted patients
- Random Forest achieved higher overall accuracy but struggled with recall due to class imbalance
- ROC-AUC used to compare model performance

## Model Artifact

The trained Logistic Regression model is saved at:

models/logistic_regression.pkl


This file contains the full preprocessing and modeling pipeline and can be loaded using `joblib` for future predictions or evaluation.

Note: I could not save the Random Forest model due to GitHUb file size becoming too large to commit

## Data Access Notes

Due to GitHub file size limits, you are unable to see the raw and cleaned data directly.

To run this project locally:
1. Download the *Diabetes 130-US Hospitals (1999–2008)* dataset from the UCI Machine Learning Repository:
   https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008

2. Place the raw dataset file in:
   data/raw/

3. Run the data cleaning notebook (`01_data_cleaning.ipynb`) to generate the cleaned dataset in:
   data/processed/

4. Run the remaining notebooks in this order:
   - 02_eda.ipynb
   - 03_modeling.ipynb

The above workflow is how I generated all my work and results.

## Status
- **Sprint 2:** Completed (data cleaning and exploratory analysis)
- **Sprint 3:** Completed (model development, documentation and saved model artifact)
