# Lines to Curvers: Linear vs Non-Linear Models

This project compares **linear** and **non-linear** models for predicting housing sale prices using the Kaggle dataset: [House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques).

It integrates **theory of predictive modeling** with practical machine learning methods to explore how different model families perform, interpret, and generalize.

---

## Problem Statement

> **Objective:** Predict housing sale prices and compare the performance and theoretical implications of **linear** versus **non-linear** modeling techniques.

The project serves as a case study for:
- Bias-variance tradeoff
- Statistical inference
- Data → parameter space transformations
- Regularization and uncertainty quantification

---

## Dataset

- Source: Kaggle competition dataset
- Size: ~1,460 training rows × 80+ features (numerical + categorical)
- Target: `SalePrice` (continuous)
- Key Observations: Right-skewed distribution, missing values, mixed feature types

---

## Methodology

### 🔹 Preprocessing
- Missing value imputation
- One-hot encoding of categorical features
- Feature scaling (standardization)
- Separate workflows for original vs engineered features

### Linear Models
- **Linear Regression**
- **Ridge Regression**
- **Lasso Regression**
- **Elastic Net**

> Evaluated using R², RMSE, MAE, CV-RMSE  
> Regularization used to control overfitting and multicollinearity

### Non-Linear Models
- **Random Forest**
- **Gradient Boosting**
- **XGBoost**
- **LightGBM**
- **Neural Network**

> Applied tree-based models and neural networks with hyperparameter tuning, early stopping, dropout, and batch normalization

---

## 📈 Results Summary

| Model Type     | Best Test R² | Best RMSE ($) | Notes |
|----------------|--------------|---------------|-------|
| Ridge (Linear) | 0.868        | 31,819        | Best among linear models |
| XGBoost        | 0.915        | 25,514        | Best overall model |
| Gradient Boost | 0.908        | ~26,600       | Stable high performance |
| Neural Net     | ~0.89–0.90   | Varies        | Sensitive to tuning |

- **Linear models** benefited from regularization and feature engineering
- **Non-linear models** captured complex feature interactions and curvature
- XGBoost achieved the **highest predictive accuracy**

---

## Theory Connections

| Concept                    | Application                                                 |
|----------------------------|-------------------------------------------------------------|
| Bias-Variance Tradeoff     | Boosting ↓bias, bagging ↓variance, regularization stabilizes |
| Statistical Inference      | Coefficient analysis in linear models                        |
| Uncertainty Quantification | Cross-validation + ensemble variance                         |
| Transformations            | Feature → Parameter space (Linear: direct, NN: deep mappings) |
| Generalized Aliasing       | Lasso and Ridge reduce collinearity issues                  |

---

