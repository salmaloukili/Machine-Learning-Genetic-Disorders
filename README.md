# Predicting Genetic Disorders: A Machine Learning Approach

This project explores machine learning techniques to predict genetic disorders using a dataset of genetic features. It evaluates the performance of two models: **Random Forest** and **Neural Networks**, with a focus on addressing data imbalances and missing values, aiming to support early diagnosis and precision medicine.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Models and Methods](#models-and-methods)
- [Results](#results)
- [Future Work](#future-work)
- [Contributors](#contributors)

---

## Overview
Genetic disorders are complex, often caused by DNA mutations leading to significant health issues. This project aims to predict such disorders and their subclasses using machine learning techniques, ultimately assisting in early diagnosis and treatment strategies.

## Dataset
The dataset, sourced from a HackEarth challenge, contains 22,083 entries with features like blood tests, genetic history, and other indicators of genetic disorders. Notably, it includes:
- **Primary Disorders**: Single-gene, Mitochondrial, and Multifactorial.
- **Subclasses**: Examples include Tay-Sachs, Diabetes, and Alzheimer’s.

## Data Preprocessing
Given the dataset’s high level of missing data and imbalanced classes, we employed several preprocessing steps:
- **Feature Selection**: Selected features with higher relevance, removing redundant attributes.
- **Handling Missing Values**: Missing values were either dropped or imputed as appropriate.
- **Encoding & Normalization**: Categorical features were label-encoded, while numerical data was scaled with a Robust Scaler for stability.

## Models and Methods

### 1. Random Forest
An ensemble learning method that combines multiple decision trees to improve prediction accuracy. Key approaches:
- **Hyperparameter Tuning**: Used `RandomizedSearchCV` with a 5-fold cross-validation strategy to fine-tune model parameters.
- **Class Imbalance Handling**: Tested various sampling techniques, but they did not enhance performance significantly.

### 2. Neural Network
A deep learning approach using Keras and TensorFlow’s Sequential API with multiple dense layers:
- **Architecture**: Utilized a model with four hidden layers and a softmax output layer.
- **Regularization**: L1 and L2 regularization was applied to reduce overfitting.
- **Optimization**: Used Adam optimizer with learning rate adjustments to improve convergence.

## Results
- **Random Forest**: Achieved 58% average F1 score, with stronger performance in detecting Mitochondrial disorders.
- **Neural Network**: Slightly outperformed Random Forest, with a 60% macro F1 score. However, both models struggled with the Multifactorial disorder class, highlighting the need for better class distinction.

## Future Work
Improvements include applying advanced feature engineering techniques, exploring dimensionality reduction (e.g., PCA), and implementing more sophisticated approaches for handling class imbalances, such as classifier chaining.

## Contributors
- **Salma Loukili**: Neural Network model development, feature engineering, and visualization.
- **Nicolas Gutierrez**: Random Forest model optimization, feature selection, and dataset analysis.

---

This project demonstrates the potential of machine learning in predicting genetic disorders and serves as a foundation for future advancements in computational genetics.
