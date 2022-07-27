# Time-Series-Champagne-Sales


In this notebook, we will conduct a time series analysis for the champagne company, that is pierre-ferre (a Switzerland based company).

It will help this firm to make a forecast about its future sales so that it can work on inventory and demand requirements.  As a result, it will be able to optimize its costs leading to a maximization of its profits.

We will using  its champagne sales [data](https://docs.google.com/spreadsheets/d/1cKOPGH4PPCLm5PV3XPCLHAp1YlYQGNJU/edit?usp=sharing&ouid=104083810998656045104&rtpof=true&sd=true) from 1964-72 given in millions
  

To achieve it , we will aply time series  techniques such as ARIMA, SARIMAX to arrive at the forecast for its future sales.


# ARIMA MODEL

## Work on train data:
![image](https://user-images.githubusercontent.com/82542269/181350140-1d788366-c4c3-42c6-b04d-adb8b50381af.png)





## Work on test data:

![image](https://user-images.githubusercontent.com/82542269/181350166-70ae7d6f-3951-4885-b867-547839bca4be.png)



It worked well on the train data but could not deliver well on the test data. The reason could be presence of seasonality in the dataset.  For this, we will make use of the SARIMAX model taking into account both seasonality and exogenous factors.


# SARIMAX MODEL


## Prediction on Test data:
![image](https://user-images.githubusercontent.com/82542269/181350030-12ece960-8f9c-4003-a371-544ba144cbf9.png)




# Conclusion:


We started our analysis with a basic exploration of the dataset. It helped in determining some important facts of dataset like presence of trend and seasonality in the dataset. We discovered that the given time series has some positive trend and seasonality in it.

After this, we began building baseline models : ARIMA model. We found that its AR, I, and MA components are 1,1 and 1 respectively, thanks to use of PACF , first differencing and ACF plots respectively.

However, it did not deliver well on the test data due to seasonality in the main dataset (as seasonality is not covered by the stationery). Consequently, we deployed SARIMAX model which not cover seasonality but also cover the exogenous component of the data. It did a much excellent job thanks to AIC of around 1110 (30 percent less error than that of ARIMA model).



