# ☕ Café  Demand Forecasting

## Victor Leiva Espinoza

## 📌 Introduction
This project focuses on building a predictive model to estimate the daily demand for each product sold at a café that specializes in Indian snacks. By analyzing historical transaction data, we aim to forecast the quantity of each item expected to be sold on a given day. This can support inventory planning, staffing, and promotional strategies.

---

## 📊 Dataset Description
The dataset, sourced from Kaggle, contains transactional records from a café offering items like samosas, chai, lassi, and Mom’s Magic biscuits. It includes two main CSV files:

- **Order Details (`order_items.csv`)**
  - `id`: Unique identifier for each entry
  - `order_id`: Order number
  - `product_id`: Identifier for the purchased item
  - `quantity`: Number of units purchased
  - `total`: Total price (unit price × quantity)
  - `created_at`: Timestamp of the transaction

- **Product Pricing (`products.csv`)**
  - `Item`: Name of the product
  - `Price`: Fixed unit price

The data spans from **April 21, 2025 to June 19, 2025**, capturing over 9,000 transactions.

The Dataset can be found here: https://www.kaggle.com/datasets/ajayjaat/caf-order-transactions-dataset?select=order_2+%281%29.csv

---

## 🎯 Objective
The goal is to develop a machine learning model that predicts the number of units expected to be sold for each product on a future date.

- Aggregating historical sales data by day and product
- Engineering temporal and trend-based features
- Training regression models (e.g., XGBoost, LightGBM)
- Evaluating performance using time-aware validation techniques

The final output will be a daily forecast table listing each product and its expected sales volume.

## ✅ Conclusion

This project successfully developed a time-aware regression model to forecast daily product-level demand for a café specializing in Indian snacks. Using XGBoost and a series of engineered temporal and rolling features, we predicted quantities sold over the final 7-day period of the dataset.

Key evaluation metrics were:

- **RMSE**: 16.17  
- **MAE**: 6.30  
- **R²**: 0.837  

These figures indicate the model captures the majority of sales variation and performs reasonably well in aggregate. However, the scatter plot of actual vs. predicted quantities reveals that the model tends to underperform on extreme cases—particularly where sales volumes spike.

This limitation is critical in practice: underpredicting during peak days could lead to stockouts, while overpredicting inflates inventory costs. Thus, while the model is a strong baseline, future iterations should address:

- **Outlier robustness** through quantile regression or gradient boosting with asymmetric loss
- **Contextual feature inclusion** (e.g., holidays, weather, marketing events)
- **Per-product model tuning**, as product behaviors vary

Overall, this model serves as a valuable starting point for inventory planning and sales forecasting. With further refinement, it can evolve into a decision-support tool for operational efficiency in café management.
