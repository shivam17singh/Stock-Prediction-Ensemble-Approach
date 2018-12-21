

```python
DATASET CREATION :

For data collection we used  Yahoo finance. We collected Yahoo Stock data from Yahoo Finance. We collected data from April 1996 to april 2016. The stock market took a toll during 2007-2008 financial crisis. This time around, companies went in loss and stock data of companies completely unpredictable. Training our model using this data would cause our system to be less accurate because of a lack of trend during the crisis period. So,we avoid data that can result into uncertain behaviour.
For our problem we kept technology and software services as a sector. The stock data obtained  contains the following parameters:
•Date
•Open
•High
•Low
•Close
•Adj Close
•Volume
We took the daily closing values of each of the stock as the stock value for a day.

TOOLS:

Language Used: Python
We have used the following libraries:
•Numpy 
•Scikit-learn 
•Pandas 
•Keras

IMPLEMENTATION:

Multiple Regression:
We are using the linear model from scikit learn library. We are using  Open , High, low, Volume  as our dependent variable in multiple regression for the prediction of closing price of stocks of the particular day. We are predicting the closing stock price of latest 100 days of the dataset and we are using the 90% of the remaining stock details for the training set and 10% for testing set. After, the prediction of the stocks and for the purpose of comparing accuracy with the actual closing price we are plotting graphs between them using the matplotlib library and are calculating the mean accuracy.

LSTM:
We are implementing LSTM using  keras deep learning library . We are using open and high features for the prediction of closing stock prices of latest 100 days . We have used our dataset in sets of 5 and then predicted every 5th value of that set . We are using the 90% of the remaining stock details for the training  set and 10% for testing set. For training purpose we have added 128 classes in the hidden layer than by adding another dense layer with 64 classes we have narrowed it down. We have further narrowed it down to 16 classes then to the final output, we have used Rectified Linear Unit as our activation function. We are then computing the mean accuracy and are plotting graph between predicted and actual stock prices.

SVR:
We are implementing SVR using Scikit learn library. We have used open feature as a base for prediction of closing price for our  regression
technique .We have used Radial Basis Function for the prediction of closing stock.

Ensemble Method:
We have multiplied the outcomes of the SVR, LSTM, Multiple Regression with the respective weights that were assigned to them on the basis of their accuracy (Weights:LSTM=1,Multiple Regression=3,SVR=2) the output is then divided by the sum of all weights assigned to the algorithm.

MEAN ACCURACIES:
Support Vector Regression-98.56306691
Multiple Regression-99.02800116
Long short term memory network-97.63474000
Ensemble Learning-99.07562496

```
