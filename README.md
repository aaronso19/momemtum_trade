#### Project: Momentum Trade Short Term Prediction Model for ETF

Aaron So

#### Executive summary
Momemtum trade can be done manually by observing the trend of a stock/ETF price and targeting small short term profit. However such approach is not scalable and very subjective. Since it is a routine process, it is possible to get it automated with some well defined predictive models to recommend establishing position of a Stock/EFT based on recent price data. 

#### Rationale
For individual stock, there are more variables such as earning results, dividend, rumor etc, that determing the price action of a stock. However, ETF is a basket of many stock, and such variables are mostly filtered out. So we are going to focus on ETF and determine the best predictive models and their optimal parameters to make trade action recommendation. 

#### Research Question
The question that we would like to answer is to use predictive models to give recommendation of the following trading strategy. Given the last 5 day closing price of a particular ETF, if we buy at opening today, can we get a 3% profit in the next 5 days? 

#### Data Sources
Yahoo finance

#### Methodology
For the data, we use 1 year data of a well known ETF: VOO. Each row of data consist of 5 days of closing price data. The result is a True/False column representing trade or not trade. We get the opening price of the next day and the maximum price of the next 5 days. If the difference is higher than 3 percent, we would put true on the result recommending the trade. If not we put false in the result and not recommending the trade. For the predictive model, we use KNN, Logistice regression, Decision Tree, and SVM. We will try turning the models to get the optimized parameters. 

#### Results
From all the reults we got so far, it seems like KNN with the default parameters give the best prediction. In particular, it gives good prediction on instances NOT placing a trade (true negative). We will need to find more ways to improve true positive.

#### Next steps
We can investigate a few more ETF to see the effectiveness of the models. Moreover, we can also try to add a few more parameters, such as volumn, overall index trend etc. to see if it can improve the prediction further.

#### Outline of project

- https://github.com/aaronso19/momemtum_trade


##### Contact and Further Information