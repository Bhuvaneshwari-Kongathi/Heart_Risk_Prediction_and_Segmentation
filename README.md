# Heart Risk Prediction and Lifestyle-Based Risk Segmentation

## Overview

This project analyzes demographic, lifestyle, behavioral, and health-related factors associated with a dataset-provided heart disease risk category.

The project combines two machine learning approaches:

1. **Supervised Machine Learning** to classify the existing heart disease risk category.
2. **Unsupervised Machine Learning** using K-Means to identify groups of individuals with similar characteristics.

The project demonstrates an end-to-end machine learning workflow including data profiling, preprocessing, exploratory data analysis, model comparison, model evaluation, feature importance, clustering, and interpretation.

> **Disclaimer:** This project is for educational and analytical purposes only. It is not intended for clinical diagnosis, medical advice, or healthcare decision-making.

## Business Problem

Heart-related health risks can be associated with demographic characteristics, lifestyle habits, behavioral factors, family history, and existing health conditions.

This project evaluates whether machine learning models can classify the heart disease risk category available in the dataset and explores whether individuals can be segmented into groups with similar health and lifestyle characteristics.

## Objectives

* Understand the dataset and assess data quality.
* Explore demographic and lifestyle patterns.
* Analyze the distribution of the heart disease risk category.
* Build reproducible preprocessing pipelines.
* Compare multiple classification algorithms.
* Evaluate the selected model on unseen data.
* Examine feature importance.
* Identify lifestyle and health-based groups using K-Means clustering.
* Compare clustering patterns with the existing risk category.

## Dataset

The dataset contains demographic, lifestyle, behavioral, and health-related information.

* **Records:** 216
* **Original Variables:** 20
* **Modeling Features:** 16
* **Target:** `risk_of_heart_disease`

Target distribution:

* **No:** 143
* **Yes:** 73

Example variables include:

* Age
* Gender
* Height and Weight
* Physical Exercise
* Exercise Type
* Fruit and Vegetable Servings
* Fast Food Consumption
* Screen Time
* Average Sleep
* Family History
* Medical Condition
* Smoking
* Stress
* Mental Health Condition
* Health Check-Ups

## Methodology

1. Data Loading
2. Data Profiling
3. Data Cleaning
4. Exploratory Data Analysis
5. Feature Selection
6. Train-Test Split
7. Data Preprocessing Pipeline
8. Classification Model Development
9. Cross-Validation
10. Final Model Evaluation
11. Feature Importance
12. K-Means Clustering
13. Silhouette Analysis
14. PCA Visualization
15. Cluster Interpretation

## Machine Learning Models

The following classification models were evaluated:

* Logistic Regression
* K-Nearest Neighbors
* Random Forest

Five-fold stratified cross-validation was performed using the training dataset.

Models were evaluated using:

* Accuracy
* Weighted Precision
* Weighted Recall
* Weighted F1-score

## Model Performance

Random Forest demonstrated the strongest overall cross-validation performance and was selected as the final model.

### Final Test Results

* **Selected Model:** Random Forest
* **Test Accuracy:** 66.15%
* **Test Records:** 65

Classification performance was stronger for the `No` category than the `Yes` category.

This indicates that the model has limited ability to identify positive-risk observations.

## Feature Importance

Random Forest feature importance identified several influential features, including:

* Weight
* Height
* Age
* Screen Time
* Average Sleep
* Physical Exercise
* Fruit and Vegetable Servings
* Family History

Feature importance represents relative contribution to the model and does not establish causal relationships.

## Risk Segmentation

K-Means clustering was used to identify groups of individuals with similar demographic, lifestyle, behavioral, and health characteristics.

* **Clustering Records:** 216
* **Optimal Clusters:** 2
* **Cluster Selection Method:** Silhouette Score

PCA was used to visualize the clusters in two dimensions.

The clusters showed similar distributions of the dataset-provided heart disease risk category, suggesting that the natural groups identified by K-Means did not strongly separate the existing risk labels.

## Key Findings

* The dataset contains 216 observations and 20 original variables.
* No missing values were identified during data profiling.
* The supervised learning dataset contains 16 predictive features.
* Random Forest demonstrated the strongest overall cross-validation performance.
* The final model achieved 66.15% accuracy on unseen test data.
* The model performed better for the negative-risk category than the positive-risk category.
* Weight, height, age, screen time, and sleep were among the leading model features.
* K-Means identified two lifestyle and health-based clusters.
* The clusters showed similar proportions of the existing risk category.

## Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Google Colab
* Git & GitHub

## Project Workflow

```text
Raw Dataset
     ↓
Data Profiling
     ↓
Data Cleaning
     ↓
Exploratory Data Analysis
     ↓
Feature Selection
     ↓
Train-Test Split
     ↓
Preprocessing Pipeline
     ↓
Model Comparison
     ↓
Cross-Validation
     ↓
Final Model Evaluation
     ↓
Feature Importance
     ↓
K-Means Clustering
     ↓
Silhouette Analysis
     ↓
PCA Visualization
     ↓
Cluster Interpretation
```

## Repository Structure

```text
heart-risk-prediction/
│
├── data/
│   └── Hearti.csv
│
├── notebooks/
│   └── Heart_Risk_Prediction_and_Segmentation.ipynb
│
├── outputs/
│   ├── model_comparison.csv
│   ├── silhouette_scores.csv
│   └── visuals/
│        ├── cluster_visualisation.png
│        ├── confusion_matrix.png
│        └── risk_distribution.png
│
├── docs/
│   └── Heart_Risk_Prediction_and_segmentation.docx
│
├── README.md
├── requirements.txt
└── .gitignore
```

## Limitations

* The dataset contains only 216 observations.
* The dataset may not represent the broader population.
* The target is a dataset-provided risk category and is not a clinical diagnosis.
* The positive class has fewer observations.
* The final model has limited performance for identifying positive-risk observations.
* Standard clinical cardiovascular measurements are not available.
* Feature importance does not establish causation.
* Clustering results depend on feature representation and algorithm selection.

## Future Improvements

* Use a larger and more representative dataset.
* Include clinically validated cardiovascular risk variables.
* Address class imbalance.
* Perform hyperparameter optimization.
* Evaluate additional machine learning models.
* Compare multiple clustering algorithms.
* Validate the model using external datasets.

## Author

**Bhuvaneshwari Kongathi**

Aspiring Data Analyst | Python | Machine Learning | Data Analytics

