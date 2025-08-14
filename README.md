# 🛒 Walmart Sales Forecasting with Machine Learning

## 📌 Project Overview
This project predicts weekly sales for Walmart stores using historical sales data, store details, and external factors such as holidays and economic indicators.  
By applying advanced machine learning models like Linear Regression and XGBoost, the aim is to help Walmart optimize inventory, plan promotions, and forecast demand accurately.

---

## 📂 Dataset
The dataset is the [Walmart Store Sales Forecasting](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting) dataset, publicly available on Kaggle.  
It consists of four main CSV files:

- features.csv → Contains additional variables such as temperature, fuel price, CPI, unemployment, and holiday indicators.
- stores.csv → Store metadata including store type and size.
- train.csv → Historical weekly sales for each store and department.
- test.csv → Data for which predictions are required (sales values not provided).

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
- scikit-learn → ML algorithms & metrics
- XGBoost → Gradient boosting regression
- LightGBM → Alternative boosting approach
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
   - SMAPE, MAPE, MAE, MSE, RMSE, R², Adjusted R²
6. Visualization → Compare actual vs predicted weekly sales.

---

## 📈 Results
| Model              | SMAPE (%) | RMSE   | R²    |
|--------------------|-----------|--------|-------|
| Linear Regression  | 35.43     | 18.33  | 0.98  |
| XGBoost            | 28.31     | 13.16  | 0.99  |

- XGBoost significantly outperformed Linear Regression in terms of accuracy and error reduction.
- Seasonal trends and holiday effects were successfully captured.

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/walmart-sales-forecasting.git
