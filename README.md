# Sales Forecasting Models: Comparative Analysis

This repository contains the implementation and analysis of four popular forecasting models for retail sales: **LSTM**, **SARIMA**, **XGBoost**, and **Random Forest**. The goal of this project is to identify models offering the best balance of accuracy, scalability, and computational efficiency using real-world retail data.

## Dataset

We used the [Store Sales - Time Series Forecasting](https://www.kaggle.com/competitions/store-sales-time-series-forecasting) dataset from Kaggle. The dataset includes:
- Time-series sales data
- Store metadata
- Economic indicators
- Holiday and event information

## Models Implemented

1. **LSTM (Long Short-Term Memory):**
   - Captures long-term dependencies in time-series data.
   - Suitable for data with sequential and temporal patterns.

2. **SARIMA (Seasonal ARIMA):**
   - Extends ARIMA by incorporating seasonal components.
   - Useful for capturing periodic trends but struggles with non-linear relationships.

3. **XGBoost:**
   - Gradient boosting framework optimized for structured data.
   - Demonstrates high accuracy and computational efficiency.

4. **Random Forest:**
   - Ensemble-based method.
   - Robust to non-linear data patterns and computationally efficient.

## Evaluation Metrics

The models were evaluated using the following metrics:
- **Mean Squared Error (MSE):** Measures average squared difference between actual and predicted values.
- **Root Mean Squared Error (RMSE):** Square root of MSE, providing error in the same unit as the target.
- **Mean Absolute Error (MAE):** Measures average absolute difference between actual and predicted values.
- **R-squared (R²):** Proportion of variance explained by the model.

## Results Highlights

| Model          | MSE       | RMSE     | MAE     | R²      |
|----------------|-----------|----------|---------|---------|
| **XGBoost**    | 13,393.00 | 115.73   | 41.56   | 0.9711  |
| **Random Forest** | 41,302.63 | 203.23   | 82.36   | 0.9108  |
| **LSTM**       | 155,879.24| 394.82   | 108.12  | 0.663   |
| **SARIMA**     | 462,911.54| 680.38   | 305.67  | 0.00007 |

- **XGBoost** emerged as the best performer with the lowest error metrics and the highest R² value.
- **Random Forest** balanced accuracy and computational efficiency well.
- **LSTM** captured intricate patterns but was computationally intensive.
- **SARIMA** struggled with non-linear and high-dimensional data.

## Repository Structure

```
.
├── data/                   # Dataset files (not included due to size; see Kaggle link)
├── notebook/              # Jupyter notebooks for model implementation
├── README.md               # Project overview (this file)
```

## Getting Started

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-repo-name/sales-forecasting.git
   cd sales-forecasting
   ```

2. **Prepare Dataset:**
   - Download the dataset from [Kaggle](https://www.kaggle.com/competitions/store-sales-time-series-forecasting) and place it in the `data/` directory.

3. **Run the Notebooks:**
   - Explore the `notebook/` folder for model implementation and analysis.

## Key Insights

- Simpler models like **XGBoost** and **Random Forest** often outperformed more complex approaches like **LSTM**, particularly in terms of computational efficiency and accuracy.
- Traditional time-series methods such as **SARIMA** struggled with the high dimensionality and non-linearity of real-world retail data.

## Future Work

- Investigate hybrid models combining the strengths of different approaches.
- Apply advanced feature engineering techniques to enhance forecasting accuracy.

## References

Refer to the `References` section in the project report for a detailed bibliography.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

For any questions or suggestions, feel free to open an issue or contact the authors.
