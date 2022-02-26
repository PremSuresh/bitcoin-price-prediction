# bitcoin-price-prediction:
The project attempts to predict the future value of Bitcoins by identifying the correlation between social media sentiment and past market prices of Bitcoin. We can achieve this by collecting user feeds from social media such as twitter, facebook and linkedin. We gather the real-time Bitcoin prices using the coinmarketcap API.  For our specific example we use twitter data extracted from the twitter API.  Once we have our corpus we will map their associated sentiments using the TextBlob python package. I use these as feature vectors to our DL algorithm. Then we compare the results of the different algorithms and choose the one with the best accuracy score.

### Data Collection
For this project I use the historic prices of bitcoin and sentiments on the keyword bitcoin from twitter. Bitcoin (₿) is a cryptocurrency. It is a decentralized digital currency without a central bank or single administrator that can be sent from user to user on the peer-to-peer bitcoin network without the need for intermediaries. Bitcoins are created as a reward for a process known as mining. They can be exchanged for other currencies, products, and services. Sentiment analysis is contextual mining of text which identifies and extracts subjective information in source material, and helping a business to understand the social sentiment of their brand, product or service while monitoring online conversations. We use tweets from twitter users on the hashtag bitcoin and btc as source material
1) CoinMarketCap API
2) Twitter API

### Features:
After performing various preprocessing on the data we get the following features (timestamp,price,sentiment)

### Methodology
After extensive research and experimentation I have identified LSTM’s to work the best as they hold long range context in memory and use this context in predictions. After tuning the parameters to achieve the best output we arrive at the following model with 2 LSTM layers and 2 Dense layers which use mean absolute error as the loss function with 150 epochs .
  
### Mapping the predictions of the test data with the actual values are mapped below:
![alt text](https://github.com/PremSuresh/bitcoin-price-prediction/blob/main/testdatacomparison.png?raw=true)

### The following is the comparison between the actual and predicted values on the real-time which seem to be promising.
![alt text](https://github.com/PremSuresh/bitcoin-price-prediction/blob/main/comparisonpredictedvsactual.png?raw=true)
