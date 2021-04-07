# Machine-Learning-in-Finance

## 1.	Dataset:
i.	FB

ii.	FANG

iii.	Fama-French

iv.	ADS

## 2.	Models built:
i.	Farmer French, AR1

ii.	Exponential Moving Average (5 days) + Linear Regression

iii.	MACD(Moving Average Convergence Divergence)

iv.	FB Prophet 

v.	SVM

vi.	Kalman Filter

vii.	Garch

## 3.	Performance metrics of individual models: Mentioned in the presentation slides

## 4.	Bootstrapping using Resampling Residuals:
 (Bootstrap steps please refer the below link: https://en.wikipedia.org/wiki/Bootstrapping_(statistics)#Resampling_residuals)

### Bootstrap starts from t=250. We take Y[t-200:t-1] as training data, predict yhat[t], and calculate RMSE comparing all yhat[t] and Y[t]. Some of the above models either affected the overall performance or takes too long to run. Hence, only below models are used in the bootstrapping:

i.	AR1 (bootstrap 300 times)

ii.	Exponential Moving Average (300 times)

iii.	Kalman Filter (100 times; increase times will increase performance (lower RMSE) but drag running time significantly)

iv.	SVM (3 times; increase times will not increase performance that much but drag running time significantly)

## 5.	Trading Strategies and assumptions:
•	Buy Hold, Long Short, Day Trade

•	Assumption:

i.	initial trading account balance: $1 million

ii.	number of shares traded in each position: 500

•	Exact numbers will be different after running random forest every time; a .csv file will be generated each time the program is running to check the exact numbers

## 6.	Risk Management
•	We evaluate all the trading strategies with our portfolio separately and get metrics for each trading strategy (see slides for details)

•	Under “BUY HOLD”, we do not have any negative return, since the first day’s price is the lowest in the data given, and the Sortino Ratio does not apply to this case (denominator is 0).

###  Notes on Final Project Files: Change the directory of data in 'bootstrap.py' before you run the program. Run 'trading.py' directly and it will call the functions in all other files.
