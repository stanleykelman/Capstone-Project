# Capstone-Project
UC BERKELEY ML/AI Class Capstone Project 2024
# Predicting Employee Termination Using Survival Analysis

## Project Overview
This project applies survival analysis techniques to predict employee termination, focusing on identifying key drivers of early exits. The analysis uses data from employee performance and demographics, and implements three survival models:
- Kaplan-Meier Estimator
- Cox Proportional Hazards Model
- Random Survival Forest (RSF)

The project aims to compare the effectiveness of these models in predicting employee tenure and identifying actionable insights for improving retention strategies.

---

## Objective
The primary objective is to assess the performance of different survival models in predicting employee termination and to identify significant predictors of termination. These insights can help organizations develop targeted strategies to improve retention and reduce turnover.

---

## Key Business Objective
- **Goal**: Use survival analysis models to identify high-risk employees and understand the factors influencing termination.
- **Impact**: Improve workforce planning, reduce costs associated with turnover, and enhance retention strategies.

---

## Dataset
The dataset contains performance and demographic data on employees, with features such as:
- **Tenure**: Duration of employment.
- **Event**: Whether the employee was terminated (1 for terminated, 0 otherwise).
- **Performance Metrics**: Delivered packages, shipments per hour.
- **Demographics**: Gender.

The dataset includes:
- 4,738 records and 6 features after cleaning and preprocessing.
- Source: Internal company performance data.

---

## Models Implemented
Three survival models were implemented and evaluated:
1. **Kaplan-Meier**:
   - Visualizes survival probabilities over time.
   - Provides high-level survival trends.
2. **Cox Proportional Hazards**:
   - Evaluates the impact of covariates on termination risk.
   - Achieved the best performance (C-index: 0.72).
3. **Random Survival Forest (RSF)**:
   - Ensemble learning method for survival predictions.
   - Identified feature importance but underperformed in predictive ability (C-index: 0.50).

---

## Project Structure
### 1. Exploratory Data Analysis (EDA)
- Examined data distribution and key features.
- Visualized survival probabilities and termination trends.

### 2. Data Preprocessing
- Handled missing values.
- Encoded categorical features and scaled numerical data.
- Split data into training and testing sets.

### 3. Model Implementation
- Kaplan-Meier for overall survival trends.
- Cox Proportional Hazards for covariate analysis and risk prediction.
- RSF for non-parametric survival modeling and feature importance analysis.

### 4. Model Evaluation
- Compared models using the Concordance Index (C-index).
- Generated survival curves and feature importance visualizations.

---

## Results
- **Kaplan-Meier**: Provided useful visualizations of survival probabilities but lacked covariate inclusion.
- **Cox Proportional Hazards**: Best-performing model with a C-index of 0.72, offering interpretable results.
- **RSF**: Limited predictive ability (C-index: 0.50), suggesting the need for further tuning or feature engineering.

---

## Key Findings
1. **Tenure** and **delivered packages** are significant predictors of termination.
2. Kaplan-Meier is valuable for visual exploration but lacks predictive functionality.
3. Cox Proportional Hazards is the most reliable model for understanding termination risks.
4. RSF requires further optimization to improve its predictive capabilities.

---

## Recommendations
1. **Focus on Tenure Management**:
   - Address early signs of risk based on tenure predictions.
2. **Refine Feature Engineering**:
   - Enhance performance data to improve model accuracy.
3. **Leverage Cox Proportional Hazards**:
   - Use this model for operational decision-making due to its robustness and interpretability.
4. **Explore Advanced Models**:
   - Consider integrating Deep Learning-based survival models like DeepSurv.

---

## How to Run the Project
### 1. Clone the Repository
```bash
git clone https://github.com/stanleykelman/Survival-Analysis.git
