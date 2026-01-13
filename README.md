# House Prices Prediction

## Overview
This project focuses on predicting house prices using the **Ames Housing dataset**. 
The goal is to build robust regression models that capture the relationship between house features and sale prices.

Key steps include:
- Data cleaning and preprocessing
- Handling skewness and outliers with log transformation
- Encoding categorical and ordinal features
- Model training with Linear, Ridge, Lasso, Random Forest, and Gradient Boosting
- Hyperparameter tuning and ensemble methods
- Generating predictions for submission

---

## **Data**
The dataset consists of various features describing houses in Ames, Iowa, including:
- Lot size, building type, year built, garage, basement, and more.
- `SalePrice` as the target variable.

---

## **Preprocessing**
- **Log transformation** applied to skewed numeric features (`SalePrice`, `LotFrontage`, `GrLivArea`, etc.)
- **Ordinal encoding** for quality/condition columns (`ExterQual`, `KitchenQual`, `BsmtQual`, etc.)
- **One-hot encoding** for other categorical columns
- Train/test alignment to avoid column mismatch

---

## **Models & Results**

| Model                 | RMSE       |
|----------------------|------------|
| Linear Regression     | 0.157      |
| Ridge Regression      | 0.132      |
| Lasso Regression      | 0.134      |
| Random Forest         | 0.147      |
| Gradient Boosting     | 0.135      |
| Ridge (Tuned)         | 0.134      |
| Gradient Boost (Tuned)| 0.152      |
| Ensemble (Ridge + GBR)| 0.132      |
| Voting Regressor CV   | 0.128      |

**Best Performance:** Ensemble + cross-validation (VotingRegressor) with RMSE ~0.128

---

## **Tech Stack**
- Python (pandas, numpy, matplotlib, seaborn)
- scikit-learn (Linear, Ridge, Lasso, Random Forest, Gradient Boosting, VotingRegressor)
- Hyperparameter tuning with `GridSearchCV`
- Data visualization with seaborn & matplotlib

---

