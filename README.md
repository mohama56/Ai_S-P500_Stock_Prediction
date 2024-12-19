# SPY S&P 500 Stock Prediction

This project applies machine learning techniques to predict the stock prices of the SPY S&P 500 ETF, which tracks the performance of the S&P 500 index. By leveraging historical stock data, the project builds a regression model to forecast future closing prices and uncover potential market trends.

## Overview

This project uses the **XGBoost Regressor**, a gradient boosting algorithm, to model and predict the closing prices of SPY. The process involves:

- **Data Preprocessing**: Cleaning and preparing the dataset, handling missing values, and removing outliers.
- **Feature Engineering**: Creating additional indicators, such as moving averages and price change metrics.
- **Model Training**: Training the XGBoost Regressor on historical data to predict closing prices.
- **Prediction**: Evaluating the model’s accuracy on unseen test data.

## Key Features

- **Comprehensive Data Cleaning**: Handling missing or invalid values (`NaN`, `inf`) and outliers.
- **Feature Engineering**: Adding moving averages (e.g., `SMA_5`, `SMA_20`) and other technical indicators for improved predictions.
- **Prediction Accuracy**: Comparing predicted closing prices with actual values.
- **Reproducibility**: Ensures scalability for other financial datasets.

## Technologies Used

- **Programming Language**: Python
- **Libraries**:
  - `pandas` for data manipulation.
  - `numpy` for numerical computations.
  - `matplotlib` for visualization.
  - `xgboost` for regression modeling.
  - `scikit-learn` for preprocessing and evaluation.

## Dataset

The dataset consists of historical SPY stock data, with columns such as:
- `Open`: Opening price
- `High`: Daily high price
- `Low`: Daily low price
- `Close`: Closing price (target variable)
- `Volume`: Daily traded volume
- Derived indicators, including simple moving averages (`SMA_5`, `SMA_20`).

## How It Works

### Step 1: Data Preprocessing
- Handle missing or invalid values (`NaN`, `inf`) in the dataset.
- Scale and normalize numerical columns.
- Remove extreme outliers.

### Step 2: Feature Engineering
- Create new features such as moving averages and price differences.
- Use these engineered features as inputs for the regression model.

### Step 3: Model Training
- Split the data into training and testing sets (80% train, 20% test).
- Train an XGBoost Regressor using features like `Open`, `Volume`, and technical indicators.

### Step 4: Prediction and Evaluation
- Use the trained model to predict the `Close` price for test data.
- Compare predicted prices with actual closing prices to assess accuracy.
