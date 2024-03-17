### Project Title: Momentum Trade Short Term Prediction Model for ETF and stock

**Author**
Aaron So

#### Executive summary
Momemtum trade can be done manually by observing the trend of a stock/ETF price and targeting small short term profit. However such approach is not scalable and very subjective. Since it is a routine process, it is possible to get it automated with some well defined predictive models to recommend establishing position of a Stock/EFT based on recent price data. 


#### Rationale
For individual stock, there are more variables such as earning results, dividend, rumor etc, that determing the price action of a stock. However, ETF is a basket of many stock, and such variables are mostly filtered out. For this reason, we were going to focus on ETF and determine the best predictive models and their optimal parameters to make trade action recommendation. However, from the initial data analysis, ETF prices are relatively stable, and the models are mostly recommending not to buy for the short team since it is not likely to have a high up swing for the price. In this final study, we analyzed stocks that are volatile, and we see the models performs much better to determing instances that a trader should buy a stock for short term trade.

#### Research Question
The question that we would like to answer is to use predictive models to give recommendation of the following trading strategy. Given the last 5 day closing price of a particular ETF/stock, if we buy at opening today, can we get a 3% profit in the next 5 days? 

#### Data Sources
Yahoo finance

#### Methodology
For the data, we use 1 year data of two ETFs: VOO and SCHD, and two well known volatile stocks: TSLA and NVDA. Each row of data consist of 5 days of closing price data. The result is a True/False column representing trade or not trade. We get the opening price of the next day and the maximum price of the next 5 days. If the difference is higher than 3 percent, we would put true on the result recommending the trade. If not we put false in the result and not recommending the trade. For the predictive model, we used KNN, Logistice regression, Decision Tree, and SVM. We tried turning the models to get the optimized parameters. 

#### Results
Like previously for ETF, we found that almost all models are good at producing true negative, but not good at finding true possitive. This is fine, as it will help avoid investment mistake, but it is not good enough to give us good trade recommendation for making short term profit. This is possibly due to the relatively stable price of the ETFs.

In this analysis, we tried 2 volatile stocks. NVDA was known to be performing well in last 1 year, while TSLA was not. We applied the same models to them and found that KNN gave the best results in term on finding true positive (recommendation that results in profit) and produce relatively small number of false positive( recommendation that results in loss or only minor profit) This give insight into the characteristics of the underlysing asset that we should use in a momemtum trade strategy. For non-volatle asset, momentum trade is not a good strategy as the models won't recommend trading most of the time. However, with volatile stock, regardless of it is performance, a simple model is able to recommend good trading position which can results in profit, and also the recommendation that results in loss is relatively small.

#### Next steps
One interesting next step that i would like to try is to implement the exact same strategy with neural network. I would expect the same trend for volatile vs non-volatile assets. However, i would expect improvement in accuracy to recommend true positive, which will result in short term profit. 

The second aspect that i would like to try is to use more parameters for the underlying asset such as volume, volatility indicators, option pricing, sentiment index etc. However, i will need to study more into these indicators to see how they can fit into the model effectively.

Lastly, this model give recommendation for short term trade, which only expect trader to hold the asset for a short period of time. However, different holding time can be tried to see at which holding timeframe is more effective. I would guess if we increase the holding timeframe for the ETFs, we might have a better chance to get more true positive.


#### Outline of project

- https://github.com/aaronso19/short_term_trade


##### Contact and Further Information