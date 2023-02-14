# MercadoLibre_Ecomm

Analysis and visualization of time series datasets including Google Search Trends and Stock Price for an Ecommerce company.

Here steps that were taken for the analysis and visualization:

* Find unusual patterns in hourly Google Search traffic.
* Mine the search traffic data for seasonality.
* Relate the search traffic to stock price patterns.
* Create a time series model by using Prophet.
* Forecast the revenue by using time series models.

### Google Search Traffic

There is an increase in traffic of 1841.5 during the month, i.e. May, that MercadoLibre released its financial results. Given that May was compared to approx. 4 years of monthly traffic data, it is on average a significant increase in traffic although not necessarily of "viral" proportions. See [forecast_net_prophet.ipynb](https://github.com/KSohi-max/MercadoLibre_Ecomm/blob/main/forecasting_net_prophet.ipynb) for more information.

![Avg Traffic by Day of Week](https://github.com/KSohi-max/MercadoLibre_Ecomm/blob/main/Images/Avg%20Traffic%20by%20Day%20of%20Week.png)

Early in the Week, the Search Traffic is the highest and then it slowly declines over the week.

### Seasonality

![Avg Traffic by Week of Year](https://github.com/KSohi-max/MercadoLibre_Ecomm/blob/main/Images/Avg%20Traffic%20by%20Week%20of%20Year.png)

Looking at the heatmap for Day of Week, Hours 0-3 on Days 1-4 and Hours 21-23 on Days 0-3 & 6 seem to have high search trends based on the heatmap observations.

![Hour of day and Day of Week Search Traffic Heatmap](https://github.com/KSohi-max/MercadoLibre_Ecomm/blob/main/Images/Hour%20of%20day%20and%20Day%20of%20Week%20Search%20Traffic%20Heatmap.png)

Expanding on the heatmap to Hrs of Day & Day of Week Search Traffic, Hours 0-3 and Hours 21-23 seem to consistently high search trends based on the heatmap observations throughout the year. In winter months, there is little difference when compare to the rest of the year.  But there is more traffic in the summer especially in the 22 and 23 Hours (Search Trends in ~90s).

### Search Traffic v. Stock Price

![Stock Price Close  Data](https://github.com/KSohi-max/MercadoLibre_Ecomm/blob/main/Images/Stock%20Price%20Close%20%20Data_1.png)
![Search Trend Data](https://github.com/KSohi-max/MercadoLibre_Ecomm/blob/main/Images/Search%20Trend%20Data_2.png)

In early to mid 3/2020 there is a distinct decline in the both the closing price of the stock price and the search trends. Also in early 5/2020, there is an increase in the closing stock price and a spike in search treands.  This seems to indicate that there is definitely a common trend that is consistent with the narrative that "after the initial shock to global financial markets, new customers and revenue increased for e-commerce platforms."

![Stock Volatility](https://github.com/KSohi-max/MercadoLibre_Ecomm/blob/main/Images/Stock%20Volatility.png)

Stock volatility spiked, and tended to stay high, during the first half of 2020. This is a common characteristic of volatility in stock returns worldwide: high volatility days tend to be followed by yet more high volatility days.

### Search Trends Forecast

![Near-Term Forecast/Popularity](https://github.com/KSohi-max/MercadoLibre_Ecomm/blob/main/Images/Near-Term%20Forecast:Popularity.png)

Search Trends in the near-term forecast (80 days) seem to be going down which indicates that popularity of MercadoLibre will also go down slightly.

![Forecast_Search Trends](https://github.com/KSohi-max/MercadoLibre_Ecomm/blob/main/Images/Forecast_Search%20Trends.png)
(Note: `yhat` represents the most likely (average) forecast, whereas `yhat_lower` and `yhat_upper` represents the worst and best case prediction (based on 95% confidence intervals).)

![Forecast_Search Trends_components](https://github.com/KSohi-max/MercadoLibre_Ecomm/blob/main/Images/Forecast_Search%20Trends_components.png)

Highest popularity is exhibitied at midnight and the popularity starts to increase in early morning hours until it reaches a peak at midnight. Also, Tuesday seems to be the most popular day for search traffic. And looking at the Yearly graph, search traffic plummets in October.

### Revenue Forecast

![Sales Forecast - Seasonal](https://github.com/KSohi-max/MercadoLibre_Ecomm/blob/main/Images/Sales%20Forecast_Seasonal.png)

Peak revenue day is Wednesday for the Ecomm site but Monday also seems to do very well for sales on average.

![90 Day Sales Forecast](https://github.com/KSohi-max/MercadoLibre_Ecomm/blob/main/Images/90%20Day%20Sales%20Forecast.png)

Here are the sales forecast for the quarter:
* Most Likely    $22,750 millions of USD
* Worst Case     $20,829 millions of USD
* Best Case      $24,671 millions of USD
