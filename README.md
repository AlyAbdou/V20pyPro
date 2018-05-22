# V20pyPro



# Machine Learning Examples

Exploring pricing data using a variety of machine learning libraries and algorithms. All examples use data from the AUD_JPY csv that contains OHLC and technical indicators' data.

## Ensemble Research

Using a basic list of six standard Sci-kit Learn ensemble methods, we can explore the effectiveness of these off-the-shelf models. Out of the box, these models can achieve 65-75% accuracy but could be improved by manipulating learning rates, increasing the number of estimators, or for some models, including a base estimator; i.e. another predictive model that improves the Booster's reliability.

*AdaBoostRegressor*
![AdaBoost png](/graphs/model1.png)

*BaggingRegressor*
![BaggingRegressor png][/graphs/model2.png)


## LSTM with Multiple Inputs 

A basic LSTM model built with Keras and using 20 input factors: open, high, low, volume, and technical indicators such as moving averages, a Stochastic Oscillator, Bollinger Bands, and others. The results are noisy and mixed, as it is unclear if more data helps or hurts the model from building meaningful connections between the data.

![LSTMulti png](/graphs/LSTMulti Score 55.4103637890938.png)

This model could be improved in a number of ways. Increasing the number of layers, normalizing the data, reducing the amount of input data, and increasing the amount of learning data are the most obvious choices.

## Linear Models

Linear regression models are natural candidates for time series analysis. Using the standard Sci-kit learn Ridge and Linear Regression models, we can achieve roughly 80% accuracy on a single currency pair before manipulating any of the parameters.

*Ridge*
![Ridge png](/graphs/Ridge 0.80991178871757.png)

*LinearRegression*
![LinearRegression png](/graphs/LinearRegression 0.8099495670315746.png)

The Autoregressive Integrated Moving Average (ARIMA) is not exactly a machine learning algorithm, but a linear model used in econometric analysis that can be applied to financial markets to make predictions. A quick build of this model can also produce 78% accurate predictions on the test data.

*ARIMA*
![ARIMA png](/graphs/ARIMA 0.7895470127761371.png)

## Tensorflow NN

This is a a FOREX adaptation of Sebastian Heinz's neural network for stocks from his Medium.com article ["A simple deep learning model for stock prediction using TensoFlow"](https://github.com/sebastianheinz/stockprediction). 

![TF NN Gif](/gifs/tf_nn_research.gif)

Running on the daily AUD/JPY chart, the model reaches 95% accuracy in less than 10 epochs.

