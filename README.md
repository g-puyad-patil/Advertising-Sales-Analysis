# Advertising Sales Analysis

A comprehensive data science project that analyzes the relationship between advertising expenditures (TV, Radio, and Newspaper) and product sales. This project implements Multiple Linear Regression to predict sales and evaluates model performance through various statistical techniques.

## Project Overview
The objective of this analysis is to answer key business questions regarding marketing ROI and to build a predictive model that can forecast sales based on advertising budgets.

### Key Questions Answered:
1. **Average TV Spend:** Calculating the mean expenditure for the TV medium.
2. **Correlation Analysis:** Determining the statistical relationship between Radio ads and Sales.
3. **Channel Impact:** Identifying which medium (TV, Radio, or Newspaper) drives the most sales.
4. **Predictive Modeling:** Visualizing a Multiple Linear Regression model's accuracy.
5. **Scenario Forecasting:** Predicting sales for a specific budget ($200 TV, $40 Radio, $50 Newspaper).
6. **Normalization:** Testing the effects of data scaling on model performance.
7. **Feature Ablation:** Measuring the drop in accuracy when excluding TV from the predictors.

---

## Dataset Description
The dataset contains four main columns:
- **TV:** Advertising dollars spent on TV.
- **Radio:** Advertising dollars spent on Radio.
- **Newspaper:** Advertising dollars spent on Newspaper.
- **Sales:** Number of units sold (Target Variable).

---

## Technical Approach

### 1. Exploratory Data Analysis (EDA)
We use correlation matrices and heatmaps to visualize how each medium relates to sales. 



### 2. Modeling
We utilize `Scikit-Learn` to implement a Linear Regression model.
- **Full Model:** `Sales ~ TV + Radio + Newspaper`
- **Reduced Model:** `Sales ~ Radio + Newspaper` (Used to answer Question 7)

### 3. Normalization
To answer Question 6, we apply `StandardScaler` to ensure all features are on the same scale, allowing for a fair comparison of coefficients.

---

## How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/Advertising-Sales-Analysis.git](https://github.com/g-puyad-patil/Advertising-Sales-Analysis.git)
2. Install dependencies:

pip install pandas seaborn scikit-learn matplotlib
3. Run the analysis:
python main.py

Results & Insights
Highest Impact: Based on the coefficients, TV advertising shows the strongest positive correlation with sales.

Model Visualization: The plot below compares the actual sales data against our model's predictions.

Prediction Result: For a budget of $200 TV, $40 Radio, and $50 Newspaper, the model forecasts a specific sales increase (see code output for exact value).
