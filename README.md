# 🛒 Walmart Sales Forecasting with Machine Learning

## 📌 Description
Predicts Walmart’s weekly sales using historical data, store info, and external factors, using Linear Regression as a baseline and XGBoost as an advanced model for more accurate demand forecasting.

---

## 📂 Dataset
This project uses the [Walmart Sales Forecast dataset by Aslan Ahmedov on Kaggle](https://www.kaggle.com/datasets/aslanahmedov/walmart-sales-forecast).  

It includes:
- Train data: Weekly sales data by store and department from February 2010 to November 2012.
- Test data: Same format without Weekly_Sales values for prediction.
- stores.csv: Metadata for ~45 Walmart stores (type and size).
- features.csv: Contains external variables like Temperature, Fuel_Price, CPI, Unemployment, and Holiday_Flag.

This rich feature set enables modeling the effects of economic conditions and holidays on sales trends.

---

Preprocessing Steps:
1. Merge all datasets into one.
2. Handle missing values and duplicates.
3. Encode categorical features (`Type`, `IsHoliday`) into numeric format.
4. Create time-based features (Year, Month, Week, Day, Season, etc.).
5. Generate lag and rolling mean features for capturing trends.
6. Perform seasonal decomposition to understand patterns.
7. Remove outliers and apply scaling.

---

## 🛠️ Tools & Libraries
- Python
- Pandas, NumPy → Data manipulation
- Matplotlib, Seaborn → Visualization
- scikit-learn → ML algorithms & metrics (Linear Regression)
- XGBoost → Gradient boosting regression
- Statsmodels → Time series decomposition

---

## 📊 Methodology
1. Data Loading & Merging → Combine Walmart sales, features, and store info.
2. Cleaning → Handle nulls, duplicates, and remove anomalies.
3. Feature Engineering → Create temporal, lag, and statistical features.
4. Model Training:
   - Linear Regression (baseline model)
   - XGBoost with hyperparameter tuning using GridSearchCV
5. Evaluation:
   - SMAPE, RMSE, R²
6. Visualization → Compare actual vs predicted weekly sales.

---

## 📈 Results (%)
| Model              | SMAPE | RMSE   | R²    |
|--------------------|-----------|--------|-------|
| Linear Regression  | 35.43     | 18.33  | 0.98  |
| XGBoost            | 28.31     | 13.16  | 0.99  |

- XGBoost significantly outperformed Linear Regression in terms of accuracy and error reduction.
- Seasonal trends and holiday effects were successfully captured.
