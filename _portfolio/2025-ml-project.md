---
title: "Predicting Flight Arrival Delays: Machine Learning Approaches"
excerpt: "Team project applying multiple ML models to predict flight delays using BTS data<br/><img src='/images/portfolio/ml-project.png'>"
collection: portfolio
date: 2025-12-01
---

## Project Overview
Team project for CS4641: Machine Learning at Georgia Institute of Technology (Fall 2025), focusing on predicting flight arrival delays at Hartsfield–Jackson Atlanta International Airport using U.S. Bureau of Transportation Statistics data.

**Team Members:** Antonio Arias Alonso, Luoyi Zhang, Magnus H. Voss, Richie Jonathan, Sara El Khattabi Vilchez

**Project Website:** [https://rjrichie.github.io/ml-flight-arrival-delay/](https://rjrichie.github.io/ml-flight-arrival-delay/)

## Objectives
- Develop binary classification models to predict whether flights will be delayed (>15 minutes)
- Build regression models to estimate arrival delay magnitude in minutes
- Compare performance across multiple ML algorithms on imbalanced dataset

## Dataset
- **Source:** U.S. Bureau of Transportation Statistics (BTS)
- **Scope:** Domestic arrivals at ATL from 11 airlines (2019-2025, excluding COVID years)
- **Features:** Scheduled/actual times, carrier information, origin airport, temporal factors
- **Challenge:** Highly imbalanced (84.8% on-time, 15.2% delayed)

## Methods & Models

### Classification Models
- **Logistic Regression** - Baseline linear model with class balancing
- **Random Forest Classifier** - Ensemble method with hyperparameter tuning
- **Multi-Layer Perceptron** - Neural network with early stopping
- **XGBoost** - Gradient boosting with randomized search optimization

### Regression Models
- **Random Forest Regressor** - Predicting delay magnitude
- **MLP Regressor** - Neural network for continuous delay estimation
- **XGBoost Regressor** - Optimized gradient boosting

## Key Results

### Classification Performance (Best: XGBoost)
- **Accuracy:** 61.4%
- **F1-Score:** 0.316
- **ROC-AUC:** 0.643
- Successfully balanced precision/recall for minority class detection

### Regression Performance (Best: XGBoost)
- **MAE:** 19.48 minutes
- **RMSE:** 34.11 minutes
- **R²:** 0.039
- 57.1% of predictions within 15 minutes of actual delay

## Technical Contributions
- Extensive feature engineering (temporal, operational, carrier-specific features)
- Addressed class imbalance using balanced weights and SMOTE techniques
- Comprehensive hyperparameter tuning with cross-validation
- Feature importance analysis revealing scheduled elapsed time, origin airport, and seasonality as top predictors

## Technologies Used
- **Machine Learning:** scikit-learn, XGBoost, PyTorch/TensorFlow
- **Data Processing:** pandas, NumPy
- **Visualization:** matplotlib, seaborn
- **Development:** Python, Jupyter Notebook

## Conclusions
Tree-based ensemble methods (Random Forest, XGBoost) consistently outperformed linear and neural models, demonstrating the importance of capturing nonlinear interactions in flight delay prediction. The relatively low R² in regression tasks highlighted the need for external features (weather, air traffic, upstream delays) for improved delay magnitude estimation.

## Course
**CS4641: Machine Learning**  
Georgia Institute of Technology, Fall 2025
