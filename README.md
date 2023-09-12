# **Stock price prediction using LSTM**
#### **Video Demo**:  <https://www.youtube.com/watch?v=9uYAjFp43rU>
#### **Introduction**:

This project focuses on developing a machine learning model that can accurately predict future stock prices using an LSTM (Long Short Term Memory) neural network. Using machine learning models to predict stock prices is valuable to investors and traders, as the models can help them make informed investment decisions while minimizing risk and help them maximize their return on investment. Specifically, we will explore how to use the LSTM model to predict the VNINDEX - a market index that represents the price movement of stocks being traded at the Ho Chi Minh City Stock Exchange (HOSE), Vietnam.

The project consists of several key steps:

## 1. Data Collection and Preprocessing
The first step is to collect historical stock price data for VNINDEX using a reliable data source from <a href="https://www.investing.com/">Investing.com</a>. We collected data covering the period from January 2003 to September 2022. After the data is collected, we preprocessed it to remove any outliers, missing values, or other outliers that could affect the accuracy of the model.

## 2. Model building
Next, we built an LSTM model using Keras in Python. The model's architecture includes multiple layers of LSTM cells, which are capable of capturing and remembering long-term dependencies in the data. We used a rolling window approach to create input sequences of historical prices and trained the model using 80 percent of the historical data. We used the remaining 20 percent of the dataset for testing.

## 3. Model Training and Evaluation
We trained the LSTM model using the Adam optimizer with a learning rate of 0.001, a batch size of 128, and 100 epochs. We used Root Mean Squared Error (RMSE) and Mean Absolute Percentage Error (MAPE) to evaluate the model's accuracy.During the training process, the model will be checkpointed based on the 'loss' metric. This means that the model will be evaluated on how well it is minimizing the loss function, which is a measure of how well the model is performing on the training data. The best performing model will be saved to the file 'agent.hdf5', thanks to the 'ModelCheckpoint()' callback. The prediction results were presented visually to facilitate comparison with the actual price. This helped us to obtain valuable insights on how to enhance our model's performance.

## Results and Discussion
Our LSTM model achieved a mean squared error (RMSE) of 30.997 and a mean absolute percentage error (MAPE) of 1.79%. The accuracy of the model is about 95%, which is a reasonably good number.


## Conclusion
In summary, our LSTM model can accurately predict future long-term trends for VNINDEX with high confidence. However, it’s important to keep in mind that the accuracy of the model may vary depending on the specific dataset and the particular problem being solved. It’s also worth noting that while the model may be accurate in predicting major trends, it may not be as accurate in predicting smaller or more nuanced changes