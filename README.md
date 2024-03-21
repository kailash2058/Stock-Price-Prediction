
# LSTM based IBM Stock Price Prediction Project

## Introduction

This project focuses on utilizing Long Short-Term Memory (LSTM) networks, a type of recurrent neural network (RNN), for stock price prediction. The aim is to forecast future stock prices based on historical data, specifically using the stock prices of IBM (International Business Machines Corporation) from 2006 to 2018.

## Motivation

Stock price prediction is a challenging yet crucial task in the financial industry. Accurate predictions can help investors make informed decisions about buying or selling stocks. LSTM networks are well-suited for this task due to their ability to capture long-term dependencies in sequential data.

## Dataset

The dataset used in this project consists of daily stock prices of IBM from January 1, 2006, to January 1, 2018. It includes attributes such as Open, High, Low, Close, Volume, and Name. The dataset is publicly available and can be obtained from various financial data sources.

## Methodology

### Data Preprocessing
- The dataset is split into training and test sets, with the training set containing data up to 2016 and the test set containing data from 2017 onwards.
- The 'High' attribute is chosen for predicting stock prices.
- The data is scaled using MinMaxScaler to ensure that all features have the same scale.

### LSTM Model Architecture
- The LSTM model architecture consists of multiple layers of LSTM units with dropout regularization to prevent overfitting.
- The architecture includes four LSTM layers followed by a dense output layer.
- The model is compiled using the Adam optimizer and mean squared error (MSE) loss function.

### Training
- The model is trained using the training set with 50 epochs and a batch size of 32.

### Testing and Evaluation
- The trained model is used to make predictions on the test set.
- The predicted stock prices are inverse transformed to obtain the actual stock prices.
- The root mean squared error (RMSE) is calculated to evaluate the model's performance.

## Usage

1. Clone the repository to your local machine.
2. Ensure you have the necessary dependencies installed.
3. Run the provided Python script to execute the LSTM model and visualize the results.
4. Experiment with different hyperparameters and architectures to improve the model's performance.

## Results

The LSTM model demonstrates reasonable accuracy in predicting future stock prices, as evidenced by the RMSE metric. However, further optimization and tuning of hyperparameters may lead to improved performance.

## Visualization

The project includes functions to visualize the predicted stock prices compared to the actual stock prices using matplotlib. These visualizations provide insights into the model's performance and its ability to capture trends in the data.
