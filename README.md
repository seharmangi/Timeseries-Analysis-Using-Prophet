# Timeseries Analysis Using Prophet

A multi-product multi-store sales forecasting using prophet — automates time series forecasting for each product-store combination, saving forecasts and plots neatly organized by a folder

# Multi-Product Multi-Store Sales Forecasting with Prophet

This project performs time series sales forecasting using Facebook's Prophet model for multiple product-store combinations. It automates the process of training separate models, generating forecasts, and saving the results and plots in an organized folder structure.

## Features

- Handles multiple time series based on product and store.
- Automatically creates forecasts for each combination.
- Saves forecast data and visualization plots (forecast & components) in dedicated folders.
- Easy to extend for new datasets with similar structure.

## Dataset Format

The dataset should be a CSV with the following columns:

- `Time Date`: Date of sales observation (YYYY-MM-DD or similar format).
- `Product`: Product identifier.
- `Store`: Store identifier.
- `Sales`: Sales values to forecast.

Example:

| Time Date | Product | Store | Sales |
|-----------|---------|-------|-------|
| 2023-01-01| A       | X     | 50    |
| 2023-01-01| A       | Y     | 30    |
| ...       | ...     | ...   | ...   |

## How to Use

1. Load your dataset (with columns as above).
2. Run the forecasting script.
3. Find the results in the `prophet_forecasting_results` folder, organized by `Product_Store` subfolders.

Each subfolder contains:

- `forecast.csv`: Forecasted sales including predicted values and confidence intervals.
- `forecast_plot.png`: Time series plot with forecasts.
- `components_plot.png`: Seasonal and trend components plots.

## Dependencies

- pandas
- matplotlib
- fbprophet (or prophet)

Install dependencies with:

```bash
pip install pandas matplotlib prophet

