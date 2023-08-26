# Finsearch_Deep_RL
This repository contains all the codes used to train/test the RL and benchmark models on historical stock data
It also contains the weights of the trained DQN agent (dqn_model.zip),LSTM model weights (lstm_weights.h5) and the  weights of the trained PPO agent for 3M steps (best_model_3000000.zip).

For RL models we decided to train two different agents on two different RL algorithms to see how each one performs in the real world.One using the DQN(Deep Q Network) and another using the PPO(Proximal Policy Optimization)

The models were trained on the historical stock data of nifty50 from jan 2010 to jun 2019 and tested on the nifty50 during the covid times july 19 to jun 21.
This was a true test on how well the model had understood the trends in the stock market and to what degree they can predict the stock prices.

Environment and  Training 

So  I used an environment where I have two actions buy,sell. Starting balance of 10L and a reward function that maps the change in net worth per step also to make sure the agent doesnt go below 0 balance and 0 shares I enforced that for each step that the agent spends with <0 balance or shares, a large negative penalty is given, this made sure there werent any such problems hereon. This DQN model was trained for 5 million steps and its weights were saved afterwards. LSTM was also trained and tested on the same environment, ofcourse lstm only predicted stock proce rather than suggesting an action to take. to make a policy using lstm I made the action= 1(buy) if the predicted price is rising and 0(sell) if it is falling . Also I enforced the action to be 1(buy) if the shares were 0 and 0(sell) if the balance was 0.

Results

The end results proved that lstm had a much deeper and complex understanding of the stock market as it managed to turn a 10L balance before the covid times to an 18L balance in 2021 which is quite commendable.
The DQN agent on the other hand managed to perform very well on the training data but wasnt quite able to predict the drop in stock prices due to covid as it turned a 15L balance into around 22.5L while the PPO agent managed to turn a 10L balance into a 16L networth which is impressive but they got majorly outperformed by the benchmark lstm model.

This makes sense as intuitively, analysing the complex and unpredictable behaviour of the  stock market can best be done by complex architectures like LSTM(Long Short Term Memory) in neural networks. This is especially true when the prices of thee stock market are governed by a 2 year long pandemic which is as unpredictable as it gets!

References used 

1 referred to the youtube video https://www.youtube.com/watch?v=D9sU1hLT0QY

2 Edited the source code of the environment https://github.com/AminHP/gym-anytrading

3 used this article as reference to create the benchmark lstm model https://www.analyticsvidhya.com/blog/2021/10/machine-learning-for-stock-market-prediction-with-step-by-step-implementation/

4 last but not least https://chat.openai.com/ and  https://stackoverflow.com/ were used to help with the pesky bugs encountered while coding everything up!
