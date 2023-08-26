# Finsearch_Deep_RL
This repository contains all the codes used to train/test the RL and benchmark models on historical stock data
It also contains the weights of the trained DQN agent (dqn_model.zip),LSTM model weights (lstm_weights.h5) and the  weights of the trained PPO agent for 3M steps (best_model_3000000.zip).

For RL models we decided to train two different agents on two different RL algorithms to see how each one performs in the real world.One using the DQN(Deep Q Network) and another using the PPO(Proximal Policy Optimization)

The models were trained on the historical stock data of nifty50 from jan 2010 to jun 2019 and tested on the nifty50 during the covid times july 19 to jun 21.
This was a true test on how well the model had understood the trends in the stock market and to what degree they can predict the stock prices.

The end results proved that lstm had a much deeper and complex understanding of the stock market as it managed to turn a 10L balance before the covid times to an 18L balance in 2021 which is quite commendable.
The DQN agent on the other hand managed to perform very well on the training data but wasnt quite able to predict the drop in stock prices due to covid as it turned a 15L balance into around 22.5L while the PPO agent managed to turn a 10L balance into a 16L networth which is impressive but they got majorly outperformed by the benchmark lstm model.

This makes sense as intuitively, analysing the complex and unpredictable behaviour of the  stock market can best be done by complex architectures like LSTM(Long Short Term Memory) in neural networks. This is especially true when the prices of thee stock market are governed by a 2 year long pandemic which is as unpredictable as it gets!
