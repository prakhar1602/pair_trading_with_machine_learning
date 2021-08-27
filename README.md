# Pair Trading for Machine Learning

Pair trading has been one of the most popular trading strategies since a long time for finding statistical arbitrage opportunities in the stock market. The technique is based on identifying similar pairs of stocks and taking linear combination of them based on the high positive correlation. Relying on the historical notion that the two securities will maintain a specified correlation, the pair trade gives highest returns at the time when this correlation falters. However, given the complex workings of the markets, forecasting spread typically requires developing predictive models based on deep financial knowledge. Current state of the art models uses statistical methods to perform spread prediction. 

![alt text](https://github.com/prakhar1602/pair_trading_with_machine_learning/blob/ba19fc82fad68193cea9cf2f873630b00e43a65f/Pair_trade_diag.png?raw=true)

In this project, we investigate the application of machine learning methods to find statistical arbitrage opportunities in the stock market using pair trading strategy. Pairs are recognized using clustering methods and an LSTM based Recurrent Neural Network (RNN) is utilized for predicting the spread between the stocks. This prediction is then used to generate trade signals to optimize the profits.


Historical stock data of S&P 500 companies was gathered for the scope of this project. The metadata containing the stock ‘tickers’, ‘sector’ and ‘industry’ for the S&P 500 companies was scraped from the Wikipedia. These stock tickers were used to extract data features such as daily ‘close’, ‘open’, ‘high’, ‘low’, ‘volume’ and ‘Adjacent volume’ for the 5-year time period of 06/16/2016 to 06/16/2021 from Yahoo! Finance Live.

In order to facilitate learning, we additionally calculate and extract technical indicators from the gathered data which could be used as additional inputs for our deep learning model. The missing data points are handled by imputing them by the median values of the features for each stock. Additional features such as annual ‘returns and ‘volatility’ were extracted, and the data was standardized to be used for the next steps.

