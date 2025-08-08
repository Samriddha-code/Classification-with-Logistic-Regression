# Breast Cancer Classification using Logistic Regression

## Overview  
This project uses logistic regression to classify breast tumors as malignant or benign based on the Wisconsin Breast Cancer Dataset.

## Data Preparation  
- Dropped irrelevant columns (`id`, `Unnamed: 32`).  
- Converted the diagnosis column to binary: malignant = 1, benign = 0.  
- Split data into 80% training and 20% testing sets with stratification to maintain class balance.  
- Standardized features using `StandardScaler`.

## Model Training & Evaluation  
- Trained logistic regression on scaled data.  
- Evaluated using confusion matrix, precision, recall, accuracy, F1-score, and ROC-AUC.  
- Default threshold (0.5) gave precision ~97.5% and recall ~92.9%.

## Threshold Tuning  
- Explored thresholds from 0 to 1.  
- Selected threshold 0.4 improved recall to ~95.2% while keeping precision ~97.6%.  
- This reduces missed malignant cases, important for medical diagnosis.

## Sigmoid Function  
- Logistic regression outputs probabilities using the sigmoid function:  
  $$
  \sigma(z) = \frac{1}{1 + e^{-z}}
  $$  
- The sigmoid converts linear outputs to probabilities between 0 and 1.  
- Thresholding these probabilities yields final class predictions, allowing tuning based on the problem’s needs.

## How to Use  
1. Load and preprocess data.  
2. Split and scale features.  
3. Train model.  
4. Perform threshold tuning and evaluate metrics.  
5. Visualize results with precision-recall curves and ROC curve.

## Tools  
Python, Pandas, NumPy, Scikit-learn, Matplotlib

---
