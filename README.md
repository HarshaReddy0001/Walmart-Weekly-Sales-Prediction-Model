# Weekly Sales Prediction Model - Forecasting Retail Performance

A machine learning project focused on predicting weekly retail sales to aid businesses in demand forecasting, inventory/staffing optimization, and data-driven decision-making for increased profitability.

## 1. Overview and Goal

The goal of this project is to build and evaluate various machine learning models to accurately predict weekly sales for different stores and departments within a retail setting. By leveraging historical sales data and relevant external factors, the project aims to provide valuable insights for business planning and operational efficiency. This predictive capability allows businesses to move from reactive to proactive strategies.

## 2. Technologies Used

*   **Python**
*   **Pandas**
*   **NumPy**
*   **Scikit-learn** (ExtraTreesRegressor, RandomForestRegressor, MLPRegressor, train_test_split, r2_score)
*   **Matplotlib**
*   **Seaborn**

## 3. Methodology

The project follows these key steps:

1.  **Data Loading and Merging:** Loading and combining sales, store, and feature data from CSV files.
2.  **Data Preprocessing:** Handling missing values (specifically for MarkDown features), converting categorical variables (Store, Dept, Type, Month) into a suitable format for modeling using one-hot encoding, and extracting the month from the date.
3.  **Model Selection:** Exploring different regression models including Extra Trees Regressor, Random Forest Regressor, and Neural Network (MLPRegressor).
4.  **Model Training and Evaluation:** Splitting the data into training and testing sets, training the selected models, and evaluating their performance using metrics such as Mean Squared Error (MSE), Root Mean Squared Error (RMSE), RMSE normalized by standard deviation, and R-squared.

## 4. Results / Conclusion

Based on the evaluation metrics on the test set, the Extra Trees Regressor model demonstrated the best performance among the models tested.

*   **Root Mean Squared Error (RMSE):** Measures the average magnitude of the errors. A lower RMSE indicates a better fit to the data.
    *   Extra Trees Regressor: 4059
    *   Random Forest Regressor: 5398
    *   Neural Network: 11808
*   **RMSE / Standard Deviation:** Normalizing RMSE by the standard deviation of the target variable provides a relative measure of the model's performance compared to a simple baseline model. A lower value indicates better performance.
    *   Extra Trees Regressor: 0.179
    *   Random Forest Regressor: 0.238
    *   Neural Network: 0.521
*   **R-squared (R²):** Represents the proportion of the variance in the dependent variable that is predictable from the independent variables. A higher R-squared value (closer to 1) indicates that the model explains a larger proportion of the variance in weekly sales.
    *   Extra Trees Regressor: 0.968
    *   Random Forest Regressor: 0.943
    *   Neural Network: 0.729

The Extra Trees Regressor's significantly lower RMSE and higher R-squared value indicate that it is the most effective model among those tested for predicting weekly sales in this project.

## 5. Feature Importance

Analysis of feature importance revealed that `Dept`, `Store`, and `Size` are among the most significant factors influencing weekly sales. Economic indicators like `Fuel_Price`, `CPI`, and `Unemployment` were found to be less significant in this model. Understanding these key drivers allows businesses to focus their efforts on areas with the highest impact on sales.

## 6. Business Value

This project offers significant value to retail businesses by providing a data-driven approach to sales forecasting and operational management. By accurately predicting weekly sales, businesses can:

*   **Optimize Inventory Management:** Reduce instances of overstocking (minimizing holding costs and waste) and understocking (preventing lost sales opportunities) by aligning inventory levels with predicted demand.
*   **Improve Staffing Efficiency:** Schedule staff more effectively based on anticipated customer traffic and sales volume, leading to reduced labor costs during slow periods and improved customer service during peak times.
*   **Enhance Marketing and Promotional Strategies:** Plan targeted marketing campaigns and promotions based on predicted sales patterns and the impact of markdowns, maximizing their effectiveness.
*   **Facilitate Better Financial Planning:** Generate more accurate revenue forecasts, aiding in budgeting and financial planning.
*   **Enable Strategic Decision-Making:** Provide insights into the factors driving sales performance, allowing businesses to make informed decisions regarding store operations, product assortment, and expansion strategies.
*   **Gain a Competitive Advantage:** Utilize predictive analytics to stay ahead of market trends and competitor activities.

## 7. Next Steps & Contact

*   **Future Features:**
    *   Explore other advanced regression models and techniques.
    *   Incorporate external events or local factors that might influence sales.
    *   Develop a user interface for easier interaction and prediction generation.
    *   Implement A/B testing capabilities for evaluating the impact of different strategies.
