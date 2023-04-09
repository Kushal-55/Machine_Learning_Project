# Stockpriceprediction

# Summary

In my project,I have used RNNs and Linear regression for stock analysis and prediction.

Objective - To learn about the RNNs and linear regression and to predict the closing price of a stock.

Validation loss - 0.010

Methods used -

* Linear regression
* RNN with LSTM


# Dataset Description

## Dataset Description

I used the data available for New york stock exchange. It consisted of the prices of all the stocks traded in the market from 2010 - 2016.

The dataset included -
Open - Opening price of a stock for that day
High - Highest price of a stock for that day
Low - Lowest price of a stock for that day
Close - The closing price of a stock for that day
Symbol - 562 unique symbols represented the companies which had their stocks listed on the market.
Date - The date and day of recording
Volume - The number of stocks of a particular company traded on that day

The dataset consisted of 851264 measurements and 7 features or columns.

## AUC Values

Since my dataset only contains 7 features -

|        Feature        |  AUC  |
|:----------------------|:-----:|
| High                  | 0.992 |
| Low                   | 0.982 |
| Open                  | 0.980 |
| Volume                 | 0.471 |

# Details

## Aim -

To learn about how linear regression, RNN and inturn the Long short term memory RNNS work and to implement them to predict the closing price of a stock.

## Approach -

### Data Cleaning-

My data consisted of all the companies listed on the stock market, hence I had to filter the company out in order to get the data for that company.

I chose the Apple inc stock traded as 'AAPL' on the New york stock market.


### Exploring the dataset -

The dataset consisted of the feature - symbol 'AAPL', open, low , high, close, date and of the volume of shares traded on the stock market for that day.

There were no null values in the dataset

The dataset consisted of two categorical variables - symbol and date with the datatype object.

Finding the trajectory -

I plotted the figure for the opening and closing data for the stock from 2010- 2016 to find out if it had an upward trajectory or a downward trajectory. The stock prices increased with time, hence it had an upward trajectory. I have attached a figure for reference.

### Data Extraction

I used the 'close' feature as my target variable to predict the closing price.

I found out the correlation between close price and the remaining variables and found out that symbol, volume and date features had very low correlation so I dropped these features.

Open and close prices had negative correlation whereas high and low had negative correlations.

## Linear Regression

For linear regression, I was able to achieve an accuracy of 99.3%. This was due to the fact that I had less number of variables to work with, for instance, for my target variable('close'), there were 1762 instances.

I was able to get a mean square error of 0.38

I used the default parameters for linear regression(since it gave me high accuracy) and did not want to overcomplicate the model by using ridge or lasso parameters.

## LSTM

I had to read a lot about RNN and LSTM, I have attached the references.

The LSTM model was the best performing model for stock prediction and it is used for time series forecasting.

I had to create timesteps for my data in order to make it ready for LSTM.

I used return sequences as true so that the model returns a sequence of predefined values and a hidden state output for each time step.

I added a dropout layer for better performance and set a dense layer as an output layer.

I have attached the validation loss vs number of epochs graph.
The validation loss was very low(0.010) as the test predictions were accurate.

## Conclusion

I studied and applied the linear regression and LSTM models which performed high on the test set.

Accuracy for Linear Regression- 99.3%
Accuracy for LSTM on testing data - 98.9%

## References 

I used these references to learn about lstms and how to implement them -

https://machinelearningmastery.com/use-timesteps-lstm-networks-time-series-forecasting/
https://arxiv.org/abs/1909.09586
https://direct.mit.edu/neco/article-abstract/9/8/1735/6109/Long-Short-Term-Memory?redirectedFrom=fulltext




```python

```
