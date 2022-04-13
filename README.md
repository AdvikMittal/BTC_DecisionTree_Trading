# BTC_DecisionTree_Trading
  Building and simulating a Bitcoin trading model using Decision Trees.\
  Data used: OHLCV (Open, High, Low, Close, Volume) data at 1 minute intervals.\
  Size of train data: 18800 rows\
  Size of test data: 4435 rows

### Instrument traded:
  Bitcoin against USD

### Indicators considered: 
  Trading volume\
  30-period, 100-period price movement\
  Deviation from 30-period and 100-period moving average\
  100-period MFI - Money Flow Index\
  100-period RSI - Relative Strength Index

  <img alt="image" src="https://user-images.githubusercontent.com/36765231/163096934-8a43dd2e-d847-43e6-afc2-aaa3654037be.png" width="600">

### Starrtegy and signals used to train data:
  Buy: When potential gain in the next 4 hours is greater than top 15% percentile of potential 4 hour gains for train period\
  &emsp; (ideally buy before big upward movements)\
  Sell: When potential loss in the next 4 hours is greater than top 15% percentile of potential 4 hour losses for train period\
  &emsp; (ideally sell before big downward movements)\
  Do nothing in periods of poterntial slow movement / no movement
  
  Ideal buy and sell periods:
  
  <img alt="image" src="https://user-images.githubusercontent.com/36765231/163101260-ce766abf-afac-4971-b946-90c1d80e217f.png" width="600">

  
### Goal of Decision Tree Classifier model:
  To look for and detect patterns in the given indicators to learn when to buy and sell\
  Then, use the trained model to test it on unseen data and measure its performance compared to the asset iteslf

### Train and test data: 
  Train data: 13 days\
  Test data: 3 days (21-24 Feb)

### Results:
  
  <img alt="image" src="https://user-images.githubusercontent.com/36765231/163096548-cb311291-068e-449c-8460-e822dc6efbeb.png" width="800">
  
  Price movement of bitcoin on top chart, value of portfolio on bottom chart\
  Green and Red markers indicate buy and sell orders respectively
  
  Asset returns: -1.85%\
  Model returns: 7.64%  &emsp;&emsp;&emsp;&emsp; (in a 3 day period)\
  Asset maximum drawdown: -7.59%\
  Model maximum drawdown: -2.51%
  
  Model mostly holds the asset during periods of upwards movements.\
  More importantly, it successfully predicts most major downward movements and liquidates holdings, significantly reducing drawdown and leading to stable returns
 


