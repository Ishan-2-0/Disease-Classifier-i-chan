Disease Classifier
Overview

This project implements a disease classifier using logistic regression, both from scratch and with sklearn. The goal is to predict whether a patient has diabetes based on health measurements.

Dataset

Source: Pima Diabetes dataset (UCI Machine Learning Repository)

Features:

Pregnancies

Glucose

BloodPressure

SkinThickness

Insulin

BMI

DiabetesPedigreeFunction

Age

Target: Outcome (1 = diabetes, 0 = no diabetes)

Approach
1. Manual Implementation

Logistic regression implemented from scratch using NumPy

Gradient descent to minimize binary cross-entropy (BCE) loss

Probabilities computed using sigmoid function

Thresholding for classification (default = 0.5, also tested 0.3)

Metrics computed: Confusion Matrix, Accuracy, Precision, Recall, ROC Curve

2. Sklearn Implementation

Logistic regression using sklearn.linear_model.LogisticRegression

Predictions and metrics calculated for comparison

ROC curve used to visualize model performance

Key Insights

Lowering the threshold increases recall but may reduce precision

Manual implementation matches sklearn results closely, validating the model

ROC curve demonstrates the tradeoff between true positive rate (TPR) and false positive rate (FPR)

Results

All result plots are stored in the results/ folder:

manual_roc.png — ROC curve for manual logistic regression

sklearn_roc.png — ROC curve for sklearn logistic regression

roc_comparison.png — Comparison of manual vs sklearn ROC curves

loss_curve.png — Binary cross-entropy loss curve for manual model

Folder Structure
Disease-Classifier/
├── Data/
│   └── diabetes.csv
├── results/
│   ├── manual_roc.png
│   ├── sklearn_roc.png
│   ├── roc_comparison.png
│ 
├── notebook.ipynb
└── README.md