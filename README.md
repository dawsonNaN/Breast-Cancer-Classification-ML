# Breast Cancer Classification Using Machine Learning
## Project Overview

This project investigates whether a small set of cell-nucleus measurements can distinguish benign from malignant breast tumour observations. Using the Wisconsin Diagnostic Breast Cancer data provided for the course, we compare two supervised classification methods—Logistic Regression and Random Forest—with K-Means clustering as an unsupervised benchmark.

The project focuses on both predictive performance and model interpretability, aiming to identify the most informative measurements for distinguishing tumour diagnoses.

## Research Questions

How accurately can selected tumour measurements distinguish benign from malignant cases?

Which modelling approach performs best on a held-out test set?

Which measurements contribute most to the predictions?

## Dataset

The course-provided dataset contains 569 observations, including 357 benign and 212 malignant cases. It includes 30 numerical cell-nucleus measurements, a binary diagnosis variable, and a course-specific technician column excluded from modelling.

No missing values or duplicate rows were found in the dataset.


## Methodology

1. Exploratory Data Analysis (EDA)

Explored feature distributions, correlations, and differences between benign and malignant cases to understand the dataset and identify potentially informative measurements.

2. Data Preprocessing and Feature Selection

Applied a stratified 80/20 train-test split.

Standardized numerical measurements using training data.

Used PCA to inform feature selection.

Selected four predictors: mean concave points, mean fractal dimension, mean texture, and mean symmetry.

The final models used the four original standardized measurements rather than PCA scores.

3. Model Development

Three approaches were evaluated:

Logistic Regression: To estimate diagnosis probabilities and interpret predictor relationships.

Random Forest: To capture nonlinear patterns and evaluate feature importance.

K-Means Clustering: To explore whether natural groupings in the measurements align with diagnosis categories.

4. Model Evaluation

Compared the models using accuracy, benign precision, malignant recall, confusion matrices, and feature importance.



## Key Findings

Random Forest achieved the highest observed test accuracy, correctly classifying 105 of 114 observations.

The model correctly identified 39 of 42 malignant cases.

Mean concave points and mean texture were particularly informative predictors.

Logistic Regression provided interpretable relationships between measurements and diagnosis.

K-Means demonstrated that natural measurement groupings partially corresponded to diagnosis categories.



