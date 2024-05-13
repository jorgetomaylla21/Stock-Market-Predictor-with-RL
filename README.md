# Stock-Market-Predictor-with-RL
Predicting MSFT stock through an LSTM model and sentiment analysis, and training a reinforcement learning agent to choose when and how much stock to buy and sell over time.

Problem: We aim to predict whether Microsoft stock (MSFT) will go up or down in the
1-hour timeframe based on historical price data and social sentiment about the company.
Data: The data comes from Alpha Vantage’s API to obtain price action data and
technical indicators, as well as StockGeist, an API that keeps track of social sentiment
scores for over 2000 stocks.
Inputs/Outputs: We input the previous 50 hours of prices into our overall architecture,
along with daily news sentiment about Microsoft, and expect to output a prediction from
the model of the optimal action to do, buy, sell, or hold, and the amount to buy or sell.
Method: We train a Long Short-Term Memory model (a variation of RNN) with the
previous 50 hours of prices, preprocessed with Vector Mode Decomposition into 5
different signals, to output the price 5 hours in the future. We also train a Reinforcement
Learning model with inputs of the predicted price, the current price, and daily news
sentiment about Microsoft, and it outputs the corresponding action to do, buy, sell, or
hold, and the amount to buy or sell.
