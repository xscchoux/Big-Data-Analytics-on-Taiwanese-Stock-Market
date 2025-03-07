# Big-Data-Analytics-on-Taiwanese-Stock-Market

### Abstract
Since many people crave to maximize their profits on all their stock trades, this project will focus on the analysis of stock data from the website of Taiwan Stock Exchange Corporation. We tried spark regression algorithms to make predictions, built a stock screener, and made a thorough trend analysis by conducting a comprehensive backtest. We will introduce some APIs and show how we fetch stock data and build the whole analysis system. Some regression results and the backtesting results filtered by our stock screener will be shown. Finally, we made an HTML interface for users to easily access our results of data analysis.

### Algorithms
For API tools, besides Numpy and Pandas, which are basic tools for data analysis, we first used String IO to request and crawl stock data from the website of TWSE, and convert them into a DataFrame object. Then, we sort data by our stock screener, and use TA-lib to compute the exponential moving average (EMA) for all stocks we pick. Finally, Matplotlib (especially MPL.Finance) helps us to draw candlestick charts and visualize the fluctuations of stock prices.

We then obtain a pair of short-period EMAs for each stock by performing backtest based on a modified double crossover method. Unlike conventional double crossover method, our trading strategy is subject to a set of rigorous conditions, thus the selected pairs of EMA curves correspond to higher ROI.

We used three kinds of typical regression. First of all, Linear Regression is a regression which predicts a response Y on the basis of a single predictor X assuming that there is approximately a linear relationship between X and Y. On top of that, Decision Tree Regression is composed of edges and nodes to represent possible paths for prediction. The last one, Random Forest Regression, is an ensemble of untrained Decision Trees with several bootstrap samples.

### Results
The Python program will generate candelstick plots of stocks which meet the given criteria, and CSV files with stock ID, transaction count, ROI and winrate. Moreover, we can mount the user interface online. In this website, we can pick a stock ID, then the transaction information and candelstick plot will be shown.
