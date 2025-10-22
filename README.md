# House Prices - Advanced Regression Techniques Challenge

This repository contains a solution to the ["House Prices - Advanced Regression Techniques"](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview) challenge on Kaggle. The goal of this challenge is to predict the final price of each home based on various features.

It is part of the Project Work for the University Of Bologna's Master's Course ["Machine Learning and Data Mining"](https://www.unibo.it/en/study/course-units-transferable-skills-moocs/course-unit-catalogue/course-unit/2024/446627)

## Solution Summary

The solution follows a classic machine learning workflow, from data exploration to advanced ensembling, to predict house prices. The full implementation and detailed analysis can be found in the `challenge/main.pdf` file.

### Methodology

1. **Data Exploration and Cleaning:**
    * Performed an in-depth Exploratory Data Analysis (EDA) to understand feature correlations, distributions, and outliers.
    * Handled missing data using various imputation strategies (e.g., filling with "None", 0, or the median value).
    * Identified and corrected the right-skewness of the `SalePrice` target variable by applying a log transformation.
    * Removed a few significant outliers to improve model robustness.

2. **Feature Engineering:**
    * Created new features to capture more complex relationships, such as `TotalSF` (total square footage), `TotalBath` (total bathrooms), and `HouseAge`.
    * Encoded categorical features using **Ordinal Encoding** for features with an intrinsic order (e.g., quality ratings) and **One-Hot Encoding** for nominal features.

3. **Modeling and Evaluation:**
    * Trained and evaluated a range of regression models, including **Ridge Regression** as a baseline, **Random Forest**, and **XGBoost**.
    * Tuned hyperparameters for each model using `GridSearchCV` and `RandomizedSearchCV` to optimize performance.
    * The performance metric used was the Root Mean Squared Error (RMSE) between the logarithm of the predicted and actual sale prices.

4. **Ensembling (Stacking):**
    * To maximize predictive accuracy, a **stacking ensemble** was implemented.
    * The best-performing models (tuned Ridge, XGBoost, and Random Forest) were used as base-level learners.
    * A `RidgeCV` model was trained as a meta-regressor on the out-of-fold predictions from the base models to produce the final price prediction.

### Results

The final stacked model achieved a score of **0.12624** on the Kaggle leaderboard, demonstrating the effectiveness of the feature engineering and ensembling strategy.

### References

- **Assignment:** [University of Bologna - Machine Learning and Data Mining](https://www.unibo.it/en/study/course-units-transferable-skills-moocs/course-unit-catalogue/course-unit/2024/446627)  
* **Competition:** [House Prices - Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques?search=ilcors)
