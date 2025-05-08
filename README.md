## Ramp Assessment Time Series


Here are some numbers:

          date  transaction_amount  rolling_3d_avg
30  2021-01-31               59.43          682.15


Dickey-fuller test of stationarity

ADF Statistic: -5.7767
p-value:        0.0000
Critical Value (1%): -3.6699
Critical Value (5%): -2.9641
Critical Value (10%): -2.6212


Observations:

Time series will need a lot of transformations because ADF statistic is well below 1% critical value. So this time series is weakly stationary).


This is an incredibly volatile time series.

Fixing it would probably need: 
- Log transformation.
- Outlier elimination
- a first difference on the log series.
- searsonal adjust

Finally.

on 31st Jan 2021, the sum of all transactions that day was $59.43, however, the 3 day rolling average ending on the 31st Jan, is $682.15. 
    date  transaction_sum
28  2021-01-29          1520.90
29  2021-01-30           466.12
30  2021-01-31            59.43


(1520.90 + 466.12 + 59.43)/3 = 682.15$

