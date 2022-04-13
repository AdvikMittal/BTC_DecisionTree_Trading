# BTC_DecisionTree_Trading
  Building and simulating a Bitcoin trading model using Decision Trees.\

### Instrument traded:
  Bitcoin against USD

### Indicators considered: 
  Trading volume\
  30-period, 100-period price movement\
  Deviation from 30-period and 100-period moving average\
  100-period MFI - Money Flow Index\
  100-period RSI - Relative Strength Index\

  <img src="https://user-images.githubusercontent.com/36765231/163096934-8a43dd2e-d847-43e6-afc2-aaa3654037be.png" width="600">

### Signals generated to train data: 
  Buy: When potential gain in the next 4 hours is greater than top 15% percentile of potential 4 hour gains for train period
  &nbsp;&nbsp;&nbsp;&nbsp; (ideally buy before big upward mvements)
  Sell: When potential loss in the next 4 hours is greater than top 15% percentile of potential 4 hour losses for train period
  &nbsp;&nbsp;&nbsp;&nbsp; (ideally sell before big downward mvements)
  
### Goal of Decision Tree Classifier model:
  To look for and detect patterns in the given indicators to learn when to buy and sell\
  Then, use the trained model to test it on unseen data and measure its performance compared to the asset iteslf

### Train and test data: 
  Train data: 13 days\
  Test data: 3 days (21-24 Feb)

### Results:
  <img src="https://user-images.githubusercontent.com/36765231/163096548-cb311291-068e-449c-8460-e822dc6efbeb.png" width="800">
  
  Model Returns: 7.64% in 3 day period on a starting capital of $10000\
  Benchmark returns: Buying 1 share every month and holding: 12%\
  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&ensp; Investing all capital at the beginning of test period and holding: 12%
 


