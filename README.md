# Finsearch_Deep_RL
This repository contains all the codes used to train/test the RL and benchmark models on historical stock data
It also contains the weights of the trained DQN agent (dqn_model.zip) and LSTM model weights (lstm_weights.h5)

The models were trained on the historical stock data of nifty50 from jan 2010 to jun 2019 and tested on the nifty50 during the covid times july 19 to jun 21.
This was a true test on how well the model had understood the trends in the stock market and to what degree they can predict the stock prices.

The end results proved that lstm had a much deeper and complex understanding of the stock market as iit managed to turn a 10L balance before the covid times to an 18L balance in 2021 which is quite commendable.
The DQN agent on the other hand managed to perform very well on the training data but wasnt quite able to predict the drop in stock prices due to covid as it turned a 15L balance into around 22.5L which is impressive but it got majorly outperformed by the benchmark lstm model.
