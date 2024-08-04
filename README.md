# prophet-challenge
prophet-challenge Mercado Stock Analysis

## Project Summary: 
> The following analysis takes a deep dive into the Google search trends of Mercadolibre. There's an assessment of the relationship between search traffic trends and stock price patterns. Finally, there is a forecast using the Prophet library. 

## Requirements: 
- Python (pandas and numpy)
- import pandas as pd
- Prophet to conduct forecasting
- DateTime to format dates in dateframe
- matplotlib for plotting 

## Quick Summary: 
**Step 1: Analyze Search Traffic Data for Seasonality (Hourly, Weekday, and Week of the Year)**

Investigated Google search data for May 2020 to identify spikes in search trends coinciding with the release of quarterly financial results. Findings showed that Google search traffic for MercadoLibre rose by 1.08 during the month of the financial release.

**Step 2: Identify Search Traffic Seasonality Trends by Hourly, Weekday, and Week of Year**

Assessed search traffic patterns across hourly, daily, and weekly intervals. Determined peak user activity times and days, providing valuable insights for targeted marketing strategies.

An uptrend begins at 9:30 AM when the market opens.
The uptrend starts on Monday with the market opening and continues through Tuesday, followed by a decline for the rest of the week.
There is a downtrend from the start of the year until May, followed by an uptrend during the holiday season at the end of the year.

**Step 3: Correlate Search Traffic with Stock Price Patterns**

Integrated search data with stock price movements to explore correlations. Analysis of the first half of 2020 revealed synchronized trends in search traffic and stock prices. Examined lagged search trends and calculated stock volatility and hourly returns to understand their relationships.

![](/Module%208%20Images/LaggedRelationships.PNG)

#### Interpretation of Results: 
**Stock Volatility and Lagged Search Trends:** The correlation coefficient between stock volatility and lagged search trends is -0.148938. This indicates a weak negative relationship. While there is some inverse relationship, it's not strong enough to be considered highly predictive.

**Lagged Search Trends and Hourly Stock Return:** The correlation coefficient between lagged search trends and hourly stock return is 0.017929. This indicates a very weak positive relationship. The relationship is so weak that it suggests lagged search trends have almost no predictive power over hourly stock returns.

**Based on these correlations:** There is a weak negative relationship between lagged search traffic and stock volatility, suggesting that as search traffic increases (with a lag), stock volatility might slightly decrease, but the effect is not strong enough to be considered highly reliable for prediction. There is a very weak positive relationship between lagged search traffic and hourly stock returns, indicating almost no predictive relationship. In conclusion, while there are slight correlations, the lagged search traffic does not exhibit a strong predictable relationship with either stock volatility or stock price returns based on the provided data.

**Step 4: Time Series Forecasting with Prophet**

Configured and utilized a Prophet model to forecast search popularity. Provided forecasts and decomposed the time series to highlight key periods of interest and activity throughout the year. Results indicated:

![](/Module%208%20Images/MercadoLibre_images_2016_2020.png)

## Conclusion: 
**Trend over Time (Stock Price of MecardoLibre):** The overall trend shows an increase in popularity from 2016 to late 2019. Then there is a sharp decline in 2020.

**Weekly Pattern of Search Trend (Day of the Week):** There is a noticeable weekly pattern where popularity peaks on Tuesday and declines towards the end of the week, with the lowest activity on Sunday.

**Yearly Pattern of Search Trend (Monthly):** The yearly pattern reveals multiple peaks and troughs, with significant increases in popularity around January, March, and October-November, and lower activity during mid-year months.

**Daily Pattern of Search Trend (Hourly):** Daily activity follows a clear pattern, with popularity decreasing sharply after midnight, reaching its lowest point around 6 AM, and then gradually increasing throughout the day, peaking again late in the evening toward midnight.

These patterns provide insights into user behavior, indicating specific times and periods when interest in MercadoLibre is at its highest and lowest.
