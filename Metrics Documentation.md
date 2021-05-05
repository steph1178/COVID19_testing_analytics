# COVID19 Testing Analysis


### Total Number of PCR Tests
* [Total Number of Tests Performed Yesterday:SQL Code ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/total_tests_yesterday)
* [Total Number of Tests Performed Yesterday:Results ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/total_tests_yesterday_results.csv)

This query measures the total number of PCR (COVID19) tests performed in the United States as of yesterday. The metric is measured by summing all the new test results reported yesterday. The results shows that there were 326 million tests performed on 5/1/2021. This is a point-in-time metric that is not indicative of any trend in testing rates.


### 7-day Rolling Average of New Cases Per Day
* [7-day Rolling Average:SQL Code ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/7day_moving_avg)
* [7-day Rolling Average:Results ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/7day_moving_avg_results.csv)

This query measure the 7-day rolling average for the past 30 days, which is an average of the previous 7 days of positive test results for each of the past 30 days. A moving average helps smooth out fluctuations in  data to better reveal trends. However, a 7-day moving average only provides a short-term trends, as opposed to longer averages like a 30-day moving average. Also, it is a lagging indicator as it depends on test results that have already occurred and does not take into account trends like vaccination rates, mask wearing, and other factors that would affect the number of positive test results. 

The data resulting from this query reveals that the number of positive cases sharply decreases by May 1st to 13,348, and the last week of averages seem to indicate a downward trend in positive results. For most of April, the 7-day moving average of new positive cases were between 40,000 and 70,000, then on 4/25, the 7-day average of new cases fell below the 40,000 floor to 34,695, and the days following the average did not rise above a maximum of 52,095. However, because this is a lagging indicator, and as vaccination rates have slowed in the US, this downward trend in positive test results may flatten instead of continuing to decrease. 


### Top 10 States With Highest Positivity Rate
* [Top Ten States By Positivity Rate:SQL Code ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/Top10States_Positivity_Rate)
* [Top Ten States By Positivity Rate:Results ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/top10states_positivity_rate_results.csv)

This query measures the top ten states with the highest rate of positive tests by dividing the sum of positive test results by the total number of tests administered over the past thirty days for each state. The results show that Michigan has had the highest rate of positive tests results, followed by Puerto Rico. These results are only a point-in-time measurement and aren't indicative of any trend occuring. There may also be limitations on the data as other states may have higher numbers of people being tested as they are more readily available in these states or possibly due to people being more inclined to take the tests there out of caution (i.e. testing before or after traveling versus someone displaying symptoms or being directly exposed to someone with the virus). This could lower their rates compared with other states where this is less testing availability, and possibly people only taking tests when they have a higher likelihood of having the virus.

Here is the table creation code used to work with the data in Postgres.
