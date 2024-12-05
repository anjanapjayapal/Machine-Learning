Here is the **README** file for the project:

---

# Predicting Delivery Time for DoorDash Orders

## Overview

This project aims to predict the total delivery time (in seconds) for DoorDash orders based on historical data. The objective is to build a predictive model that can accurately estimate the time taken for a delivery, starting from the moment an order is created (`created_at`) to when it is delivered (`actual_delivery_time`). 

## Dataset Description

The dataset `historical_data.csv` includes a subset of DoorDash deliveries from early 2015. Each row represents a unique delivery with features covering time, store details, order details, market conditions, and model predictions. 

### Features:
1. **Time Features**:
   - `market_id`: ID representing a specific city or region.
   - `created_at`: Timestamp when the order was placed (UTC).
   - `actual_delivery_time`: Timestamp when the order was delivered (UTC).

2. **Store Features**:
   - `store_id`: Unique identifier for the restaurant.
   - `store_primary_category`: Cuisine category (e.g., Italian, Asian).
   - `order_protocol`: Protocol ID for how the store receives orders.

3. **Order Features**:
   - `total_items`: Total items in the order.
   - `subtotal`: Total order value (in cents).
   - `num_distinct_items`: Count of unique items in the order.
   - `min_item_price`: Price of the least expensive item (in cents).
   - `max_item_price`: Price of the most expensive item (in cents).

4. **Market Features**:
   - `total_onshift_dashers`: Dashers available within 10 miles of the store.
   - `total_busy_dashers`: Busy dashers currently delivering orders.
   - `total_outstanding_orders`: Outstanding orders being processed within 10 miles.

5. **Model Predictions**:
   - `estimated_order_place_duration`: Predicted time for the restaurant to receive the order (seconds).
   - `estimated_store_to_consumer_driving_duration`: Predicted driving time from the store to the consumer (seconds).

### Target Variable:
- **`delivery_duration`:** Total time (seconds) from `created_at` to `actual_delivery_time`.

## Project Workflow

1. **Data Preprocessing**:
   - Handled missing values, cleaned data, and converted timestamps.
   - Generated additional features such as time-based indicators (e.g., day of the week, hour of the day).

2. **Exploratory Data Analysis (EDA)**:
   - Visualized distributions of delivery times and other features.
   - Analyzed correlations and relationships between predictors and the target variable.

3. **Feature Engineering**:
   - Created new features to enhance model performance (e.g., order-to-delivery ratios, dasher availability rates).
   - Normalized and scaled numerical data.

4. **Model Training**:
   - Experimented with regression models such as Linear Regression, Random Forest, and Gradient Boosting.
   - Used cross-validation to tune hyperparameters and avoid overfitting.

5. **Evaluation**:
   - Evaluated models using metrics such as Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).
   - Visualized predictions vs actual delivery times for performance insights.

6. **Results**:
   - Achieved an optimal model that balances accuracy and interpretability.
   - Identified key predictors of delivery time, including dasher availability and order size.

## Key Insights

- The number of dashers available and outstanding orders significantly impacts delivery times.
- Larger orders and orders from busy regions tend to have longer delivery durations.
- Predictive features like `estimated_order_place_duration` and `estimated_store_to_consumer_driving_duration` improve model accuracy.

## Technology Stack

- **Programming Language**: Python
- **Libraries**: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, XGBoost

## Files Included

1. `historical_data.csv`: Dataset for the analysis and modeling.
2. `ANJANA_P.ipynb`: Jupyter Notebook containing data preprocessing, EDA, modeling, and evaluation.
3. `README.md`: Project documentation.

## How to Run the Notebook

1. Install the required Python packages:  
   ```bash
   pip install -r requirements.txt
   ```
2. Open the notebook using Jupyter:  
   ```bash
   jupyter notebook ANJANA_P.ipynb
   ```
3. Run all cells sequentially to reproduce the results.

## Future Work

- Incorporate real-time data streams for continuous model training.
- Explore deep learning approaches for more complex patterns.
- Test the model in production to assess performance in real-world scenarios.

## Contact

For queries or collaboration, please reach out:  
**Name**: Anjana P.  
**Email**: anjanapjayapal@gmail.com  
**LinkedIn**: [Anjana P.](https://linkedin.com/in/anjanapjayapal)  
**GitHub**: [github.com/anjanapjayapal](https://github.com/anjanapjayapal)

--- 
