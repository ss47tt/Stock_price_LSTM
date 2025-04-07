# Stock_price_LSTM

How to do stock data training, validating, and testing?

1. I took year 2023 and 2024 data of Nvidia stock prices from Yahoo Finance and saved as nvda_stock_data_2.csv.

2. Load the csv file.

3. Choose the Close price of the stock and using minmax scaler, scale the close prices from 0 to 1.

4. Split the dataset into training : validating : testing of ratio 8 : 1 : 1, in order from earliest to later dates.

5. Create the sequences for LSTM by setting input sequence length of 5, and output sequence length of 1.

6. Using Pytorch LSTM model, we can set the hidden layer size of 128, 2 LSTM layers, dropout of 20 percent.

7. We can then train and validate the model, with ReduceLROnPlateau patience of 5 and early stopping patience of 10 to prevent overfitting.

8. We can then use the model to test the data.

9. Before plotting the predictions and ground truths of train, validate, and test sets, we need to inverse transform the scaler of the data.

10. The plots of the predictions and ground truths of train, validate, and test sets are in continous lines and marked with different colors.

Note: Stock prices normally fluactuate due to economy and news, and it usually do not follow a predictive pattern like weather.
