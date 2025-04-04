# 1. Analysis
## 1.1 Dataset Overview
- Numerical Features - temp, atemp, Windspeed, Casual, Registered, Count
- temp are in wide range starting from 0.82 to 41 celcius
- atemp is also in wide range, and seems 3 to 4 degrees more than temp.
- windspeed is also in wide range, but right skewed
- causal and registered are right skewed, registered have higher counts than casual.
- count is also right skewed

## 1.2 Ride Distribution
- Median of Rides are 145,
- Q1 and Q3 of Rides are 42 and 284 resp
- Rides are Right skewed with skewness of 1.24
- There are a lot of outliers and data is right skewed, suggesting customers are not regularly availing Yulu Services.
- Highest peak near 0 suggests mostly customers are using Yulu occasionally/seasonally.

## 1.3 Ride Proportions
- 39.7% Rides are taken on day when Ride Volume is High
- 27.3% Rides are taken when Ride Volume is Moderate 
- Only 14% Rides are taken when Ride Volume is Low or Very Low 
- Observations were identified to be similar for both Casual and Registered Rides

## 1.4 Ride Trends
- There are large fluctuations in Trend of Total Counts
- Trend plot suggests, in past 2 years, there has not been much change in Casual Rides
- 81.2% Customers take Registered Rides, Yulu usage is highly dominated by Registered Rides.
- Casual Rides are more skewed (skewness = 2.49) than Registered Rides (1.52), that implies Registered Rides are more distributed in Yulu than Casual rides.
- There are large fluctuations in Trend of Total Counts
- Rides across days of Week
- 25.7% of Casual Rides are taken on Saturdays and 23.0% Casual Rides are taken on Sundays
- Registered Rides are spread more evenly across all week days (Mon-Fri), almost 15% each day
- Registered Rides shrink to about ~12% on weekends, suggesting Customers are more inclined to Casual Rides on Weekends
- Holidays on Wednesday contribute about 300 Rides average rides compared to less than 200 avg Rides on normal days.
- Holidays on Fridays, receive less avg rides than Working days on Friday.
- Overall Wednesday receives the highest average Rides.

## 1.5 Rides across Hours
- 33.5% of Rides are in Evening Hours, followed by 17.4% in Morning and 16.5% in Afternoon.
- Early Morning and Late Night receive negligible rides
- Customers prefer casual rides in Afternoon and Late Morning.
- Customers prefer casual rides in Afternoon and Late Morning (contribute to 56% of Casual Rides).

## 1.6 Other Factors on Rides
- Season 1 only contributes to 15% or Ride Volume, other Seasons contribute more evenly (~25-30%)
- 68.6% of Ride Volume comes from Working Days
- More than 70% of the Rides were taken in Weather 1

## 1.7 Temperature
- atemp follows a Normal Distribution, with no Outliers (confirmed in Box plot and negative Kurtosis of -0.85)
- atemp is slightly left skewed (skewness of -0.102), suggesting that temperatures are on hotter side.
- Almost 78% of Rides are in Hot or Moderate Temperatures
- Customers do not prefer Winters, only 18% Rides in Cold Temperatures
- Customers do not prefer Rides on Very Hot or Very High Temperatures (contribute to only ~2% Rides)
- 55% of Casual Rides are on Hot Temperatures.
- 81% Casual Rides are in Moderate or Hot Temperatures
- 20.6% of Registered Rides are in Cold Temperatures whereas only 9.9% of Casual Rides are in Cold Temperatures, suggesting Customers more prefer Registered Rides in Cold.

## 1.8 Regularity in Sales
- Data is not Normal Distributed, Shapiro test resulted in p value of 5.36e-68.
- P value of 3.6298403519396414e-116 for Kruskal test suggested that Sales in 2011 and 2012 are not same.
- Sales in Quarters 1, 2, 3 and 4 are not same, Kruskal test with p value 1.838386652415837e-58 confirmed observation.
- Median Sales in Quarter 2 almost doubled from 120 to 239
- Median Sales in Quarter 4 have dropped from 251 to 211
- In Trend plot of Months, we noticed consistent dip in Sales starting Aug 2012, up to latest month December 2012
- There is steep fall from in Sales from October 2012
- Similar Pattern was observed in 2011 also, where Sales started dropping from July 2011 and fell sharply on November 2011
- These observations suggest Seasonality in Sales
- Median sales in 2011 were 111, they increased to 199 in 2012
- Trend plots confirm that Ride volume have significantly increased in 2012.

## 1.9 Seasonality in Rides with Months
- Chi Square Test with p value 1.1013614967072462e-180 suggest that Rides are dependent on Month.
- Chi Square Test with P value of 1.0505381541371918e-34 suggest Weather is dependent on Month

## 1.10 Seasonality in Rides with Weather
- Chi Square test with p value 1.7458251535301088e-40 suggest Ride Volumes are dependent on Weather
- Given it is a Weather 1, there is 53.71% Probability of Moderate to very High Ride Volume
- Given it is a Weather 2, there is 48.35% Probability of Moderate to very High Ride Volume
- Weather 1 and Weather 2 alone receive 92.16% of Ride Volumes
- Seasonality with Temperature
- Chi Square Test of P values of 0.0 suggest Temperature is dependent on Month
- As Temperature surges to mostly hot and sometimes Very Hot from July or August, the Rides start dropping.
- From October Cold Weather begins, and we identify a sudden drop in Rides, that stays till February.
- Given it is a Hot day, there 44.51% Probability of High or very High Ride Volume
- Given it is a Moderately Hot day, there 22.86% Probability of High or very High Ride Volume
- Given it is a Cold day, there 66.4% Probability of Low or very Low Ride Volume
- Given it is a very Cold day, there 86.63% Probability of Low or very Low Ride Volume
- Temperature and Weather with Ride Volumes
- Weather 1 with Hot or Moderate Temperature accounts for 60.49% of High Ride Volumes
- For all Temperatures, Weather 1 dominates the Ride Volumes

## 1.11 Temperature and Weekdays with Ride Volumes
- Given it is a Weather 1 and Working Day, there 45.35% Probability of High Ride Volumes
- Given it is a Weather 1 and Working Day, there 54.58% Probability of very High Ride Volumes


# 2. Recommendations
## 2.1 Existing Strategy has increased Ride Volumes Significantly
- Median Rides in 2011 were 111, they increased to 199 in 2012
- There has been high improvement in Year-wise Ride Volumes, so existing strategies are working good

## 2.2 Ride Volumes are Highly Seasonal with Months
  - Customers are preferring Rides in specific Temperature and Weather conditions
  - As temperature rises to Very Hot, there is significant impact on ride Volumes
  - As Temperature drops to Cold or very Cold, Ride Volumes sharply drop
  - Overall, Ride Volumes and consequently revenues will be seasonal
## 2.3 Leverage Casual Rides when Ride Volumes are low
  - Trend plot suggested that in the past 2 years, there has not been much change in Casual Rides 
  - As only 18.8% rides are Casual, these can be more promoted, especially in off-season time to leverage more Volumes.
  - Customers prefer casual rides in Afternoon and Late Morning, this can be promoted as Casual rides share a very low Volume.
  - Early Morning and Late Night receive negligible rides (less than 3%)	
  - Overall, Casual Rides can be promoted to leverage increased ride volumes during off-season, off-hours and weekends, as Casual Rides contribute more for these cases.
## 2.4 Introduce Surge Charges
  - Introducing premium charges on High Volume days can significantly increase revenues
  - Best Events for charging Premiums
    - Weather 1 (contributes to more than 70% of Ride Volumes) 
    - Hot Temperature days
    - Holidays on Weekdays, except Friday
