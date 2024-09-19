# **ChurnPredictor: Predicting Customer Churn in a Telecom Dataset**

## Project Overview
This project focuses on predicting customer churn using a telecom dataset. We explore various machine learning models such as **Linear Regression**, **Logistic Regression**, and **Generalized Additive Models (GAMs)** to understand both linear and non-linear relationships between customer features and churn. The goal is to build interpretable models and compare their performance to provide insights into customer churn behavior.

---

## Table of Contents
1. [Project Objective](#project-objective)
2. [Dataset Overview](#dataset-overview)
3. [Tasks Overview](#tasks-overview)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
5. [Modeling Approaches](#modeling-approaches)
   - [Linear Regression](#linear-regression)
   - [Logistic Regression](#logistic-regression)
   - [Generalized Additive Models (GAMs)](#generalized-additive-models-gam)
6. [Model Comparison](#model-comparison)
7. [Conclusion](#conclusion)
8. [Installation and Setup](#installation-and-setup)
9. [Contributing](#contributing)
10. [License](#license)

---

## Project Objective

The aim of this project is to predict customer churn and provide interpretable insights that help a telecommunications company understand why customers are leaving. The project involves:
- **Exploratory Data Analysis (EDA)** to investigate the relationships between customer features and churn.
- **Building predictive models** including Linear Regression, Logistic Regression, and GAM.
- **Comparing models** to determine the best approach for churn prediction.

---

## Dataset Overview

The dataset used in this project contains customer data from a telecommunications company. Each row represents a customer, and the features include demographics, services subscribed, account information, and whether the customer churned.

Key Features:
- **Demographics**: Gender, SeniorCitizen, Partner, Dependents.
- **Account Information**: Tenure, MonthlyCharges, TotalCharges.
- **Services**: InternetService, OnlineSecurity, StreamingTV, TechSupport.
- **Target Variable**: `Churn` (binary: 1 = churned, 0 = did not churn).

---

## Tasks Overview

1. **Exploratory Data Analysis (EDA)**:
   - Perform EDA to visualize relationships between features and churn.
   - Use statistical methods to check assumptions for linear, logistic, and GAM models.
   
2. **Linear Regression**:
   - Treat churn as a continuous variable (0 for staying, 1 for churning).
   - Build a linear regression model, interpret the coefficients, and assess performance.

3. **Logistic Regression**:
   - Treat churn as a binary variable and predict the probability of churn using logistic regression.
   - Interpret the coefficients to understand feature importance.

4. **Generalized Additive Model (GAM)**:
   - Build a GAM to capture non-linear relationships between customer features and churn.
   - Interpret the GAM model to explore non-linear effects.

5. **Model Comparison**:
   - Compare the performance and interpretability of Linear Regression, Logistic Regression, and GAM models.
   - Provide recommendations on the best model for the telecommunications company based on performance and interpretability.

---

## Exploratory Data Analysis (EDA)

- **Correlation Analysis**: A correlation matrix was used to check relationships between continuous variables such as `tenure`, `MonthlyCharges`, and `TotalCharges`.
- **Boxplots and Histograms**: Visualizations like boxplots and histograms were employed to check the distribution of features against churn.
- **Scatter Plots with Regression Lines**: Scatter plots were used to explore the linearity between continuous variables and churn.
- **Chi-Square Tests**: Conducted chi-square tests for categorical variables like `gender`, `Partner`, and `SeniorCitizen` to check their statistical significance in relation to churn.

---

## Modeling Approaches

### Linear Regression

- **Objective**: Treat churn as a continuous variable (0 = stay, 1 = churn) and predict churn using linear regression.
- **Key Insights**:
  - `tenure` showed a strong negative correlation with churn.
  - High `MonthlyCharges` was associated with a higher likelihood of churn.
- **Performance**: Linear regression was found to be limited due to the binary nature of the target variable, making it less effective for precise churn prediction.

### Logistic Regression

- **Objective**: Treat churn as a binary variable and predict the probability of churn.
- **Key Insights**:
  - Logistic regression provided interpretable coefficients, showing how each feature increases or decreases the likelihood of churn.
  - Features like `tenure`, `MonthlyCharges`, and `SeniorCitizen` had significant predictive power.
- **Performance**: Logistic regression performed well in predicting churn and provided interpretable coefficients for business insights.

### Generalized Additive Models (GAM)

- **Objective**: Capture non-linear relationships between customer features and churn.
- **Key Insights**:
  - GAMs revealed non-linear patterns in `tenure` and `MonthlyCharges` that were not captured by linear or logistic regression models.
  - This model offered greater flexibility in capturing complex relationships.
- **Performance**: GAMs outperformed linear models in terms of flexibility and interpretability for non-linear features.

---

## Model Comparison

| Model                  | Pros                                                           | Cons                                                             |
|------------------------|----------------------------------------------------------------|------------------------------------------------------------------|
| **Linear Regression**   | Simple and easy to interpret                                   | Doesn't handle binary targets well; limited performance           |
| **Logistic Regression** | Good for binary classification; interpretable coefficients     | Assumes linearity between features and log-odds of the outcome    |
| **GAM**                | Captures non-linear relationships; highly flexible             | More complex to implement and interpret than logistic regression  |

- **Best Performing Model**: **GAM** was the most flexible and captured non-linear relationships, while **Logistic Regression** offered the best interpretability for linear relationships.
- **Recommendation**: A combination of **GAM for complex features** and **Logistic Regression for linear features** may provide the best results for the telecommunications company.

---

## Conclusion

- **Key Findings**:
  - **tenure** and **MonthlyCharges** were significant predictors of churn.
  - **SeniorCitizen** and **Partner** were important categorical features.
  - **GAM** captured non-linear relationships that logistic regression missed, while logistic regression was better for interpreting linear effects.
  
- **Recommendation**: Use a hybrid approach where **GAM** is used for non-linear features and **Logistic Regression** for linear features, balancing model performance with interpretability.

---

## Installation and Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/AkhilByteWrangler/ChurnPredictor.git
   cd ChurnPredictor
   ```
2. Run the main.ipynb in Github Codespaces (All requirements are listed in the first cell)
