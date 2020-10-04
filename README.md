# Kaggle Problem Statement: [House Prices](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/overview)

## Background:
Ask a home buyer to describe their dream house, and they probably won't begin with the height of the basement ceiling or the proximity to an east-west railroad. But this playground competition's dataset proves that much more influences price negotiations than the number of bedrooms or a white-picket fence.

With 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa, this competition challenges you to predict the final price of each home.

## Description:
This project includes the following tasks performed in iPython:
* Exploratory data analysis
* Correlation analysis
* Data Visualization
* Scoring and Distance functions
* Clustering algorithms
* Regression Techniques

Python libraries used: Pandas, NumPy, SciPy, Scikit-learn, Matplotlib and Seaborn.

## Problem Statements:
1. Select Best Features based on best prediction for target = SalePrice. Used the following methods:
   * Univariate Selection - SelectKBest
   * Feature Importance
2. 5 Informative plots using different types of charts:
   * Scatter plot: Ground Living Area V/s Sale Price for Total rooms above ground
   * Line chart: Year built V/s Sale Price for each Building Type
   * Bar graph: Neighborhood V/s Count of Houses for each House Style
   * Histogram: Count of Houses for Year in which house was built or remodeled
   * Box Plot: Sale Price of Houses V/s Overall Quality and Air Conditioning
3. Handcrafted scoring function: The basis of the scoring function created is the correlation of the features w.r.t. the target feature i.e. SalePrice.
   * Each feature has been given a value based on the correlation. These values have been normalized in such a way that the sum of values of all features equals 1. These values are called weights.
   * The idea behind this function is that the more the correlation of the feature with the SalePrice, more weightage that feature has in its prediction. Also, the houses which are more desirable will have higher cost.
4. Pairwise distance functions:
   * Custom Distance Function: It is the square root of sum of cubes of differences between vectors.
   * SP Distance Function: It is absolute difference between the vectors.
5. Clustering using K-means Clustering algorithm where data is clustered based on the Euclidean Distance Metric.
6. Linear Regression:
   * Single Variable:
       - TotRMSAbvGrd
       - TotalBsmtSF
       - GarageArea
       - GrLivArea
   * Multiple Variables:
       - 15 best Features from SelectKBest method
       - 15 best Features from Feature Importance method
       - Features from entire dataset
7. Regression on External Dataset
8. Permutation test
9. Train models on training dataset and predict if a transaction is fraudulent for the test data set. Algorithms used:
   * Simple Linear Regression
   * Lasso Regression
   * ElasticNet Regression
   * SVR
   * XG Boost
   * Light GBM (Best Model)
