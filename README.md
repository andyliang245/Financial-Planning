# Financial Planning

## Part 1 - Personal Finance Planner

#### Under this planner, we are assuming every union member has a savings portfolio comprise of cryptocurrencies (BTC & ETH), stocks (SPY), and bonds(AGG). The analysis further assumes that all members held the same securities and shares held within their portfolios with the average housebold income of $12,000 per month. The holdings of each securities can be shown as such:

######      * 1.2 BTC
######      * 5.3 ETH
######      * 200 AGG
######      * 50 SPY

#### On March 24th, 2021, the closing price for the above securities are:

######      * BTC = $52,325.00
######      * ETH = $1,574.90
######      * AGG = $114.17
######      * SPY = $387.55

#### Based on the aforementioned prices, the planner concludes that the current market value of the portfolio is $113,348.58. Below is a breakdown of each security's market value held by each member:

######      * 1.20 BTC holding at $52,325/BTC is $62,790.00
######      * 5.30 ETH holding at $1,574.90/ETH is $8,347.08
######      * Total cryptocurrency holding is equal to $71,137.88 
######      * 200 AGG shares at closing price of $114.17 is $22,834.00 
######      * 50 SPY shares at closing price of $387.55 is $19,377.50
######      * Total stock and bond holding is equal to $ 42,211.50

#### The pie chart below demonstrates each member's aggregateportfolio value:

![Personal Finance Savings](savings_pie_chart.PNG)

#### Lastly, we have also adopted the assumption that an ideal emergency fund for each member should be equal to three times of the members' monthly income. Since the average monthly income is calculated at $12,000, we have calculated the emergency fund for each member should be $36,000. If total savings from each member's portfolio is less than the emergency fund of $36,000, we will notify the member on the difference (emergency fund minus savings less than emergency fund) for the member to reach his/her goal.

#### In conclusion per our analysis above, the member have exceeded his/her goal of saving more than three times of their monthly income in their emergency fund. As mentioned above, the total portfolio value is $113,348.58, which is  $77,348.58 above members' goal of reaching $36,000 in emergency fund.

## Part 2 - Retirement Planning

#### The retirement planning model utilizes Monte Carlo simulation tool to project the portfolio performance at 30 year period. The model assumes 60% of the holdings is comprised of SPY while the remaining 40% holds AGG for the 30 year holding period. The model pulls data from Alpaca API to model the historical performance to predict future movements. Below is a simulation plot showing 500 simulations of the cumulative portfolio return over 30 years (7,560 trading days):

![MC 30 Year Simulation](mc_30_sim_plot.PNG)

#### Through 500 simulations, the model concluded that the distribution of the final cumulative returns shows a positively skewed result, indicating that member may expect frequent small losses but also few large gains from their investment portfolio. The model also indicate that the the large gains within the probability can also cover all the frequent small losses in the span of 30 year period, assuming the portfolio remain the same with no change.   

![30 Year Distribution](mc_30_dist_plot.PNG)

#### Using the above model and the statistics shown below, there is a 95% confidence interval that an initial investment of $20,000 in the portfolio over the next 30 years will fall within the range of $65,218.85 (20,000 multiply by 95% Lower CI) and $981,341.17(20,000 multiply by 95% Higher CI).

#### If the investor decided to increase his/her initial investment of $20,000 by 50% ($30,000 initial investment), there is a 95% confidence interval that an initial investment of $30,000.00 in the portfolio over the next 30 years will fall within the range of $97,828.28 and $1,472,011.75

![30 Year Statitistics](mc_30_stat.PNG)

#### If the investor decided to retire before the 30 year mark, we have also created model projecting 5 years and 10 years holding period. However, to yield closer to project 30 year portfolio value, we have increased the initial investments to achieve close to the 30 year projected portfolio value in a less time horizon. We have also adjusted the weights on the holdings for the following 5 and 10 year simulation.

#### For 5-year holding period model, we have increased SPY holding to 90% with 10% remaining held for AGG. The rebalance of portfolio allows for the portfolio return to generate similar result at a shorter time horizon. Below a simulation plot showing 500 simulations of the cumulatie portfolio return over 5 year period (1,260 trading days):

![MC 5 Year Simulation](mc_5_sim_plot.PNG)

#### Through 500 simulations, the model concluded that the distribution of the final cumulative returns also shows a positively skewed result, much similar to the 30 year simulated model. 

![5 Year Distribution](mc_5_dist_plot.PNG)

#### For the purpose of achieveing similar portfolio value to that of the 30 year simulated model, we have increasd the required initial investment to $250,000. Using the above model and the statistics shown below, there is a 95% confidence interval that an initial investment of $250,000 in the portfolio over the next 5 years will fall within the range of $199,811.76 (250,000 multiply by 95% Lower CI) and $1,056,713.48 (250,000 multiply by 95% Higher CI).

![5 Year Statitistics](mc_5_stat.PNG)

#### For 10-year holding period model, we have updated, again, SPY holding to 70% with 30% remaining held for AGG. Below a simulation plot showing 500 simulations of the cumulatie portfolio return over 10 year period (2,250 trading days):

![MC 10 Year Simulation](mc_10_sim_plot.PNG)

![10 Year Distribution](mc_10_dist_plot.PNG)
#### We have, again, updated the required initial investment to $150,000. The decrease of the initial investment from 5-year simulated portfolio is due to increase in time horizon, allowing the model to render and achieve close to 30 year simulated portfolio. Using the above model and the statistics shown below, there is a 95% confidence interval that an initial investment of $150,000 in the portfolio over the next 5 years will fall within the range of $171,097.87 (150,000 multiply by 95% Lower CI) and $995,574.30 (150,000 multiply by 95% Higher CI).

![10 Year Statitistics](mc_10_stat.PNG)