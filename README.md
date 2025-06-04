# RNN_Stock_Price_Prediction
> Stock price prediction by using RNN


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
### Problem
- Given the stock prices of Amazon, Google, IBM, and Microsoft for a set number of days, predict the stock price of these companies after that window.
### Dataset
- The dataset consists of four CSV files corresponding to four stocks: AMZN, GOOGL, IBM, and MSFT
- We use historical stock data containing:
  - `Date`
  - `Stock Name`
  - `Open`, `High`, `Low`, `Close`, `Volume`
- Data is preprocessed, reshaped, and windowed to form time sequences with different window sizes (e.g., 65) and strides for model training.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
- We avoid data leakage by:
  - Fitting scalers **only on training data**.
  - Applying the same transformations to test sets.
  - Scaling each stock’s target column **independently** (per-stock scaling).
- We ensure model generalization using:
  - Early stopping
  - Dropout
  - Multiple hyperparameter trials using both **Simple RNN** and **LSTM** models.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- numpy: 2.0.2
- pandas: 2.2.2
- matplotlib: 3.10.0
- seaborn: 0.13.2
- scikit-learn: sklearn: 1.6.1
- tensorflow: 2.18.0

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->



<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->