# Stock Price Prediction Using Deep Learning

This project is a scrap of a Master's thesis focused on predicting daily stock prices using deep learning techniques. The project utilizes the Keras library, with models implemented using the keras_tuner.HyperModel class for hyperparameter tuning. The hypers tuned: #of layers, #neurons, dropout probability, and activation function in each layer, learning rate. This repository showcases the implementation and results of recurrent neural network models trained to predict the next day's closing price, making this a regression task.

## Project Structure

The project is organized into the following key files:

- **Baselines**
  - `0_Baseline.ipynb`: Contains baseline for stock price prediction: assign tomorrow stock price as today's price.
  - `more_Baseline.ipynb`: Includes additional baseline model (Linear Regression) to compare with the deep learning approaches.

- **Python Library**
  - `my_library.py`: Contains custom classes and functions used across the project, including the Stock Features class and utility functions.

- **Neural Network Models with Hyperparameter Tuning**
  - `r_LSTM_1_close.ipynb`: Neural network model with hyperparameter tuning using only the close price as a feature.
  - `r_LSTM_2_vol.ipynb`: Neural network model with hyperparameter tuning using the close price and volume as features.
  - `r_LSTM_3_all.ipynb`: Neural network model with hyperparameter tuning using multiple features: close, open, highest, lowest prices, and volume.
  - `r_LSTM_4_tech.ipynb`: Neural network model with hyperparameter tuning using a comprehensive set of features: close, open, highest, lowest prices, volume, and technical indicators (three moving averages calculated from the closing price).

## Data and Methodology

- **Prediction Task**: The goal is to predict the next day's closing stock price based on historical data.
- **Data**: Daily stock prices are used, with 30 previous days of data utilized to predict the next closing price. Returns are used instead of the raw data.
- **Evaluation**: The models are evaluated using Mean Squared Error (MSE) as the primary metric.
- **Hyperparameter Tuning**: All neural network models utilize the `keras_tuner.HyperModel` class for hyperparameter tuning, allowing for the optimization of various parameters to achieve the best predictive performance.

> **Note**: This project is only a scrap of the full Master's thesis. The thesis also explores additional models (GRU, simple RNN, NN with only dense layers) and other data preprocessing techniques not included in this repository.
