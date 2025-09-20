# Yield Curve Prediction for Fixed Income Markets

## Overview
This project provides a comprehensive machine learning approach to modeling and predicting the yield curve for fixed income markets. The yield curve, which plots yields (interest rates) of bonds with equal credit quality but different maturities, is a key indicator in the bond market and a strong predictor of future economic activity and inflation.

## Problem Statement
The goal is to forecast three tenors (1M, 5Y, and 30Y) of the yield curve, representing short-term, medium-term, and long-term maturities. The model incorporates:
- Historical values of the yield curve for various tenors
- Percentage of federal debt held by the public, foreign governments, and the Federal Reserve
- Corporate spread on Baa-rated debt relative to the 10-year treasury rate

## Data Sources
- **Yahoo Finance**
- **FRED (Federal Reserve Economic Data)**

The dataset consists of daily data from 2010 onward.

## Approach
1. **Data Collection & Cleaning**: Data is gathered using `pandas_datareader` and preprocessed to fill missing values and engineer relevant features.
2. **Exploratory Data Analysis (EDA)**: Includes descriptive statistics, correlation analysis, and visualization of the data distribution and relationships.
3. **Feature Selection**: Univariate feature selection is performed to identify the most relevant predictors for each target tenor.
4. **Modeling**: Multiple regression and machine learning models are evaluated, including:
   - Linear Regression
   - Lasso, ElasticNet
   - Decision Trees, KNN
   - Neural Networks (MLPRegressor)
5. **Model Evaluation**: Models are compared using cross-validation and validation set performance (MSE, R2).
6. **Hyperparameter Tuning**: Grid search is used to optimize neural network architectures.
7. **Results**: Both regression and neural network models are compared, with results visualized for each tenor.

## Key Libraries Used
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- keras
- statsmodels

## How to Run
1. Install required Python packages (see below).
2. Open the notebook `Dossier 4 - Yield Curve Prediction .ipynb` in Jupyter or VS Code.
3. Run the cells sequentially to reproduce the analysis and results.

## Installation
Install the required packages using pip:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn keras statsmodels pandas_datareader
```

## Results Summary
- The linear regression model is a strong baseline for one-step-ahead forecasting.
- Neural networks (MLP) provide comparable results and offer flexibility for modeling multiple time series.
- Feature selection confirms that previous values of the yield curve are the most important predictors.

## Author
Vidit Goyal

## License
This project is for educational and research purposes.
