# COVID19 Testing Analysis


### Total Number of PCR Tests
* [Total Number of Tests Performed Yesterday:SQL Code ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/total_tests_yesterday)
* [Total Number of Tests Performed Yesterday:Results ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/total_tests_yesterday_results.csv)

This query measures the total number of tests performed in the United States as of yesterday. The metric is measured by summing the total results from each category of outcomes using the current date minus 1 to narrow down the results to yesterday. The result shows that there were 326 million tests performed on 5/1/2021.


### 7-day Rolling Average of New Cases Per Day
* [7-day Rolling Average:SQL Code ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/7day_moving_avg)
* [7-day Rolling Average:Results ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/7day_moving_avg_results.csv)

This query measure the 7-day rolling average of positive test results from the past 30 days by summing the new results that had 'positive' outcomes by day, then using a window function to average the current and previous 6 rows of data.  The resulting data shows that the number of positive cases sharply decreases by May 1st to 13,348. For most of April, the 7-day moving average of new positive cases did not fall below 40,000 and were most often close to 70,000. There seemed to be a turning point on 4/25, when the 7-day average of new cases was only 34,695, and the days following did not rise above a maximum of 52,095. 


### Top 10 States With Highest Positivity Rate
* [Top Ten States By Positivity Rate:SQL Code ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/Top10States_Positivity_Rate)
* [Top Ten States By Positivity Rate:Results ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/top10states_positivity_rate_results.csv)

This query measures the top ten states with the highest rate of positive tests by dividing the sum of positive test results by the number of overall tests administered over the past thirty days by state. The results show that Michigan has had the highest rate of positive tests results, followed by Puerto Rico.

Here is the table creation code used to work with the data in Postgres.
