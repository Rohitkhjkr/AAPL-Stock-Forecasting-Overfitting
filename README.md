# AAPL-Stock-Forecasting-Overfitting
Comparative study of Linear Regression and LSTM models for next-day AAPL return forecasting, with a focus on predictive validity and backtest overfitting.

# Description 
This project investigates whether machine-learning models can genuinely predict next-day Apple Inc. (AAPL) stock returns, or whether apparently good forecasting performance may arise from noise and overfitting. The study compares a simple statistical model, Linear Regression, with a more flexible Long Short-Term Memory (LSTM) neural network. Their performance is evaluated against a naive mean-return benchmark and a synthetic random-data benchmark. The main focus is therefore not simply to identify the model with the lowest forecasting error, but to examine whether the observed performance provides convincing evidence of genuine predictive information.

# Research Questions
1. To what extent can statistical and machine-learning models accurately predict stock returns using historical market information?
2. How does the difference between in-sample and out-of-sample performance inform the diagnosis of overfitting?
3. Can apparent predictive performance on real financial data be distinguished from patterns produced by simulated random data?

# Dataset 
**Apple Inc. (AAPL) from 2015 to 2024** and
A **synthetic random-return dataset** is also used as a no-signal benchmark in which no serial predictive mechanism is intentionally introduced.

# Methodology
The study uses a chronological 80/20 train-test split to preserve the temporal ordering of the forecasting problem.
Three forecasting approaches are considered:
1. Naive mean-return benchmark
2. Linear Regression
3. Long Short-Term Memory (LSTM)

The models are evaluated using:
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R²
- Directional Accuracy
- Residual diagnostics
- Paired statistical tests

# Overfitting and Predictive Validity
The study does not interpret a lower test error as sufficient evidence of genuine predictive ability. The evaluation therefore combines:
- Out-of-sample testing
- A simple benchmark
- Train-test performance comparison
- Residual diagnostics
- Statistical comparison of model errors
- A synthetic random-data benchmark
This framework is designed to examine whether apparent forecasting performance can be distinguished from patterns that may arise through noise, sampling variation or model complexity.

# Findings
- The LSTM achieved the lowest observed test MSE.
- The improvement over Linear Regression was small.
- The LR-LSTM difference was not statistically significant at the 5% level.
- The naive benchmark achieved higher directional accuracy than the LSTM.
- Models trained on synthetic random data produced negative R² values and near-chance directional performance.
- The results do not provide strong evidence of reliable next-day AAPL return predictability.
- A lower forecasting error alone is not sufficient evidence of a genuine financial signal.

# Code: 
https://www.kaggle.com/code/rohitkumarkhajekar/aapl-notebook
