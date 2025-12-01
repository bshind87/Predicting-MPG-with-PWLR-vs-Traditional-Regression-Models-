README.md — Auto MPG Fuel Efficiency Prediction Project
Fuel Efficiency Prediction Using Piecewise Linear Regression (PWLR) and Multivariate Regression Models

This project explores multiple regression techniques to predict vehicle fuel efficiency (Miles per Gallon, MPG) using the Auto MPG dataset. The analysis compares Piecewise Linear Regression (PWLR)—our core modeling approach—with traditional and modern regression models including linear regression, polynomial regression, and Random Forest regression. Extensive data cleaning, feature engineering, and multivariate modeling form the foundation of this work.

Project Objectives
  Build predictive models for MPG using a combination of raw and engineered features
  Evaluate PWLR against multiple baseline and advanced regression techniques
  Understand nonlinear relationships between vehicle attributes and fuel efficiency
  Perform multivariate modeling with scalable and interpretable methods
  Provide clear visualizations and performance comparisons using R², RMSE, and MAE

Models Implemented
  Univariate Models (horsepower → mpg)
  Linear Regression
  Polynomial Regression (Degree 2)
  Piecewise Linear Regression (PWLF)
  Multivariate Models (all predictors + engineered features)
  Multiple Linear Regression
  Polynomial Regression (Degree 2)
  Random Forest Regression
  Custom Multivariate Piecewise Linear Regression (PWLR)

Uses decision tree segmentation + linear models in each leaf
Captures nonlinear structure while remaining interpretable

Data Cleaning & Preprocessing
  Replaced missing values (horsepower = '?') with median
  Converted categorical variables (cylinders, origin, model_year)
  One-hot encoded origin categories

Engineered additional predictive features:
  hp_to_weight
  car_age
  Removed outliers where needed
  Scaled numeric features for sensitive models

Technologies Used
  Category	Tools
  Language	Python 3
  Modeling	scikit-learn, RandomForestRegressor, PolynomialFeatures
  PWLR	Custom SegmentedLinearRegressor, pwlf
  Data Processing	pandas, numpy
  Visualization	seaborn, matplotlib
  Notebook	JupyterLab

Performance Metrics
Models were evaluated using:
  R² – variance explained
  RMSE – root mean squared error
  MAE – mean absolute error

Random Forest achieved the highest predictive accuracy, while PWLR provided strong interpretability with competitive performance.

Repository Structure
project/
│
│── reports/
│   ├── PWLR vs Traditional and Ensemble Regression Models​.pptx
│   └── PWLR vs Traditional and Ensemble Regression Models​.pdf
│
│── notebooks/
│   ├── 01_auto_mpg_cleaned.pynb
│   └── 02_auto_mpg_modeling_and_dashboard.ipynb
│
│── plots/
│   ├── Feature_Importance_chart.png 
│   ├── heatmap.png
│   ├── linear_veg_multi_prev_vs_act.png 
│   ├── mae_comparison.png 
│   ├── Partial_Dependence_plots.png 
│   ├── poly2_prev_vs_act.png 
│   ├── r_square_comparison.png 
│   ├── Random_Forest_Feature_imp.png 
│   ├── random_forest_red_vs_actual.png 
│   ├── Random_Forest_residual_distribution.png 
│   ├── Ranodom_Forest_pred_vs_act.png 
│   ├── residual_linear_reg_multi.png 
│   ├── residual_poly2_multi.png 
│   ├── residual_random_forest.png
│   ├── Results_comparison.png
│   ├── rmse_comparison.png 
│   └── univariate_mpg_vs_hp_fitted_curves.png
│
├── Requirements.txt
│
└── README.md

Visualizations Included
  Scatter plots with fitted curves
  PWLR breakpoint plots
  Feature importance (Random Forest)
  Partial dependence plots
  R², RMSE, MAE bar charts
  Performance heatmap (sorted by best model)
  Model comparison dashboard

How to Run the Project
1. Clone the Repository
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

2. Install Dependencies
pip install -r requirements.txt

3. Open the Notebooks
jupyter notebook


Run notebooks in the order

Key Findings
Fuel efficiency is highly nonlinear; linear models capture only broad trends
  Polynomial regression improves curvature modeling
  PWLR captures segmented behavior and is interpretable
  Random Forest achieved the best predictive performance (R² ≈ 0.92)
  Feature engineering significantly improved model performance

Authors
Bhalchandra Shinde, MS in AI, Northeastern University
Shantanu Wankhare, MS in AI, Northeastern University
Bartazari Dominick, MS in AI, Northeastern University

References
Auto MPG Dataset – UCI Machine Learning Repository
PWLF Documentation
scikit-learn User Guide

Relevant regression benchmarking papers (2024)
