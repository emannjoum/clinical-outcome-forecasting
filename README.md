# Stroke Prediction — ML Modeling Exploration
Archived project from early 2025 of machine learning and data engineering exploration 

This repository contains an exploratory machine learning workflow focused on predicting stroke occurrence using structured healthcare data.
The project walks through the full pipeline (from EDA and preprocessing to classical ML models and a neural network baseline), it reflects early experimentation with modeling decisions and evaluation.

The work emphasizes comparative modeling and data engineering rather than production deployment.

---

## Project Scope

* Perform exploratory data analysis on clinical tabular data
* Apply preprocessing, feature engineering, and imbalance handling
* Train and evaluate multiple model families
* Compare traditional ML approaches with a neural network baseline

This project has been preserved as part of development history and is not refactored beyond its original experimental state

---

## Dataset

This project uses the **Stroke Prediction Dataset** available on Kaggle.

You can download it here:

https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset

Place the CSV inside a local data directory and update the path if necessary

---

## Pipeline Overview

### Exploratory Data Analysis

* Distribution inspection
* Correlation visualization
* Class imbalance observation
* Categorical frequency analysis

### Preprocessing

* Column pruning
* BMI imputation based on age groups, instead of blindly imputing by mean/median.
* One-hot encoding
* Feature scaling
* Outlier inspection
* Yeo–Johnson transformation
* Multicollinearity check via VIF

### Feature Engineering

* Interaction term:

  * `bmi × avg_glucose_level`

### Imbalance Handling

* SMOTE resampling applied to training split

---

## Models Explored

### Support Vector Machine

* RBF kernel
* Hyperparameter tuning via GridSearch
* PCA visualization of decision boundaries

### Neural Network (Keras)

* Multi-layer dense architecture
* Batch normalization + dropout
* L2 regularization
* Binary cross-entropy optimization

### Random Forest

* Balanced class weighting
* Controlled depth and splits
* ROC-AUC evaluation

---

## Running

Install dependencies:

```
pip install numpy pandas matplotlib seaborn scikit-learn imbalanced-learn statsmodels tensorflow
```

Run the notebook after updating the dataset path.

---

## Important Notes

* This project reflects earlier experimentation and modeling exploration 
* Some preprocessing and evaluation choices were made pragmatically rather than systematically optimized
* Code structure prioritizes iteration over modular design

### Potential Improvements

* Consolidate preprocessing into reusable pipelines to avoid leakage risks
* Introduce systematic model comparison and experiment tracking
* Expand validation strategy beyond a single split

---


