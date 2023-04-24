# LSTM/GRU Model for Stock Price Prediction

# Execution
To run, import to Google Collab. File already has cell output and you can visualize. However, you can start from first cell and click Run All if you want to run again.

# Abstract

In this project, I used VADER for sentiment analysis and St-Louis Federal Reserve for macroeconomic data. Stock prices were obtained from Yahoo Finance API for 10 different companies listed on the New York Stock Exchange. I trained the model using both LSTM and GRU models and found that the GRU model with specific hyperparameters performed the best in predicting stock movement, especially during the pandemic. I concluded that GRU models are easier to train and adding extra features like news sentiment did not significantly improve the model's performance.

# Methodology

## Data Collection
- Stock prices for 10 companies from Yahoo Finance API.
- News sentiment using VADER sentiment analysis on two datasets: daily world news and stock news.
- Macroeconomic variables from the St-Louis Federal Reserve for the past 10 years.
## Data Preprocessing
- Merged daily world news and stock news datasets.
- Performed sentiment analysis on the news datasets using VADER.
- Cleaned and forward-filled macroeconomic variables.
- Merged all data based on dates to create a dataset with daily features.
## Model Training
- Trained LSTM and GRU models for stock prediction.
- Performed hyperparameter tuning using grid search.
## Experimental Setup
- Dataset with 10 features (stock prices, news sentiment, and macroeconomic variables).
- Grid search for hyperparameter tuning.
- Separated data into training, validation, and testing sets.
- Tracked performance using TensorBoard.
## Experimental Results
- GRU model outperformed LSTM model with fewer epochs.
- Training split of 0.8 was optimal for capturing pandemic-related stock movements.
- A lookback of 80 sequences provided the best results.
- Training on multiple companies resulted in better generalization.
## Conclusions
- Stock market is hard to predict. RNN models do a good job but I would not risk my money based on this specific model predicts
- GRU models were easier to train and performed comparably to LSTM models. Extra features like news sentiment did not significantly improve the model's performance.
