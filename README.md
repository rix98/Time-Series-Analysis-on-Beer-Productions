# Time-Series-Analysis-on-Beer-Productions
## Summary
In this final project I will go over to try to forecast the data of Monthly beer production in Australia Jan 1956 – Aug 1995. I chose this data set because beer production really interest me. I also love to drink beer on the weekends so I wanted to know more about the production of beer. This data comes from the tsdl library. To achieve this, I split the data into two parts to a training set and a test set. Then I will perform time series analysis on the train set from looking at the acf pacf, differencing, transforming , looking at the AICc to choose the best model and Diagnostic checking of the model and forecast.
First I take 90% of the the first observation from the dataset to be my training set and last 10% observations to be my test set. I then transform my training set in hope that it can assume normality. I transform it with log and box cox. After interpreting the result from a histogram viewpoint, the box cox transformation did better. After transforming the data with box cox I then proceed to see the data PACF and ACF for model assumputions. The model I assume at first is SARIMA(0, 1, 0) × (1, 1, 0)6. I then compare the AICc of the model with a pure AR(1) and pure MA(1) model to see if my model really did better than a pure model. Turns out it did. After assuming the model to be SARIMA(0, 1, 0) × (1, 1, 0)6, I then proceed to do diagnostic check to improve and check asummptions for the model. From diagnostic checking and seeing the residuals PACF and ACF I ended with the model SARIMA(8, 1, 1) × (2, 1, 2)6. This model resiudals pass the Box pierce and Box ljung test but failed the Mcloid test.
After doing the diagnostic check , I did forecasting with the model to predict the test set (last 10% of the original data). It turn out pretty good as the prdict the observation quite close .
