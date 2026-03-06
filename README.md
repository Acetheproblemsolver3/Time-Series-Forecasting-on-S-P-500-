# S&P 500 Time Series Forecasting using CNN-RNN Models

## Project Overview
This project explores deep learning approaches for financial time series forecasting using historical S&P 500 index data. The goal is to investigate whether hybrid neural network architectures combining Convolutional Neural Networks (CNN) with Recurrent Neural Networks (RNN) such as LSTM and GRU can capture temporal patterns in financial market data.

The project is primarily exploratory and focuses on understanding how deep learning models behave when applied to noisy financial time series.

---

## Dataset

The dataset used for this project is obtained from Kaggle:

https://www.kaggle.com/datasets/arashnic/time-series-forecasting-with-yahoo-stock-price

It contains historical stock price data sourced from Yahoo Finance.

Typical features include:

- Date
- Open
- High
- Low
- Close
- Volume

The S&P 500 index is used as the target time series for forecasting.

---

## Methodology

The project explores hybrid deep learning architectures combining convolutional and recurrent layers:

- **CNN layers** to extract short-term temporal features
- **LSTM layers** to capture long-term dependencies
- **GRU layers** as an alternative recurrent architecture

The models are implemented using **TensorFlow Keras**.

The workflow includes:

1. Data preprocessing and normalization
2. Train-test chronological split
3. Model training using CNN-RNN architectures
4. Forecast generation and visualization

---

## Technologies Used

- Python
- TensorFlow / Keras
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

---
## Results

The CNN-RNN hybrid model was able to capture short-term trends in the S&P 500 time series.

Evaluation metrics: 
34/34 ━━━━━━━━━━━━━━━━━━━━ 0s 8ms/step
12/12 ━━━━━━━━━━━━━━━━━━━━ 0s 4ms/step 
12/12 ━━━━━━━━━━━━━━━━━━━━ 0s 4ms/step 
0.9959789601187466
0.9749589863008734
0.9614490323959186
The model built with LSTM with Conv1D layers , gave us excellent results of r2_scores with 99% on the training set , 97% on the validation set and a whooping 96% on the test set .
The model performs reasonably well on trend prediction but struggles during periods of high market volatility.

---
## Project Purpose

This project is designed for **learning and experimentation with deep learning models for time series forecasting**. Financial markets are highly noisy and difficult to predict, so the focus here is on exploring modeling approaches rather than building a production trading system.

---

## Future Improvements

Possible future extensions include:

- Adding additional macroeconomic features
- Using transformer-based time series models
- Hyperparameter tuning
- Comparing deep learning models with classical models like ARIMA or Prophet
