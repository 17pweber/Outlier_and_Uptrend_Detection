To identify which categories should be flagged as significant to our client, we were comparing average 6 mo rate to the historical average and calculated the percent change between these 2 numbers. 
The goal is to understand which categories have had a recent uptrend or a recent significant event.

I saw gaps in this logic. For instance, averages are influence by outliers. Really high or low rates may have caused misleading results. 
Additionally, even if there were no outliers present, if there had been a really big downtrend in years ~2017-2023, and then a slight uptrend in ~2024-2025, 
the percent change between the historical average and recent average may still be negative despite the recent uptrend.

What we are really looking for is an analysis of the overall trend (robust to outliers). 

I created a process comparing Least Squares Regression to the more robust RANSAC Regression model to create a trend line. 
Then, I used +/- 3 standard deviations away from the trend line as outliers and calculated the slope within the recent data threshold (~6 months).
