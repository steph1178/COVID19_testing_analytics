# COVID19 Testing Analysis


### Total Number of PCR Tests
* [Total Number of Tests Performed Yesterday: SQL Code ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/total_tests_yesterday)
* [Total Number of Tests Performed Yesterday: Results ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/total_tests_yesterday_results.csv)

This query measures the total number of PCR (COVID19) tests performed in the United States as of yesterday. The metric is measured by summing all the new test results reported yesterday. The results show that there were 326 million tests performed on 5/1/2021. The main limitation in this metric is that there is a lag in reporting times, which is up to three days as listed in the [data dictionary](https://beta.healthdata.gov/dataset/COVID-19-Diagnostic-Laboratory-Testing-PCR-Testing/j8mb-icvb) for this time series. There are also general limitations to the COVID19 diagnostic test results that should be considered when looking at this metric. One limitation is that the data is not all inclusive, and may omit some testing sites such as  non-laboratory or point of care test sites, and therefore reflect the majority of tests but not the exact total. Additionally, laboratory results are submitted to local and state officials, which may  have different reporting requirements and standards that could lead to under or over counting in some states. There is also a risk of false negatives, which may increase depending on how long the infection has been present and if it is a genetic variant. These considerations will apply to all metrics using this data.


### 7-day Rolling Average of New Cases Per Day
* [7-day Rolling Average: SQL Code ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/7day_moving_avg)
* [7-day Rolling Average: Results ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/7day_moving_avg_results.csv)

This query measures the 7-day rolling average for the past 30 days, which is an average of the positive test results on the date of measurement plus the previous 6 days' results for each of the past 30 days. A rolling average helps smooth out fluctuations in data to better reveal trends. However, a 7-day moving average only provides short-term trends, as opposed to longer averages like a 30-day moving average. Also, it is a lagging indicator as it depends on test results that have already occurred and does not take into account factors  (vaccination rates, mask wearing, etc.) that would affect the number of positive test results. 

The results from this query show a sharp decline in the 7-day rolling average of positive cases on 5/1/21 to 13,348. The last week of averages seem to indicate a downward trend in positive results. For most of April, the 7-day moving average of new positive cases were between ~40,000 and ~70,000. On 4/25/21, the 7-day average of new cases fell below the 40,000 floor to 34,695, and the susbsequent days' averages did not rise above a maximum of 52,095. However, because this is a lagging indicator, and as [vaccination rates have slowed](https://www.nytimes.com/interactive/2021/05/04/us/vaccine-rollout-slowing.html) in the US, this downward trend in positive test results may flatten instead of continuing to decrease. 


### Top 10 States With Highest Positivity Rate
* [Top Ten States By Positivity Rate: SQL Code ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/Top10States_Positivity_Rate)
* [Top Ten States By Positivity Rate: Results ](https://github.com/steph1178/COVID19_testing_analytics/blob/main/top10states_positivity_rate_results.csv)

This query measures the top ten states with the highest rate of positive tests by dividing the sum of positive test results by the total number of tests administered over the past thirty days for each state. The results show that Michigan has had the highest rate of positive tests results, followed by Puerto Rico. These results rely on data over a 30-day period and therefore may not reflect recent trends well. For instance, if you take the past week's positivity rates, Michigan has a much lower rate at 10.2% and Puerto Rico doesn't appear in the top ten. Also this statistic may be diluted in states where tests are more readily available or if the state encourages testing as a precaution instead of only when one suspects they have the virus (i.e. testing before or after traveling versus someone displaying symptoms or being directly exposed to someone with the virus). 

#### Reference Code
For reference to the column names used, this is the [SQL code](https://github.com/steph1178/COVID19_testing_analytics/blob/main/table%20_creation) that created the table in Postgres for this exercise.
