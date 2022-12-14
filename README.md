# Comparison_of_GARCH_variants_and_StochVol_Model
I have compared the various variants of GARCH available in the rugarch package and the Stochastic Volatility Forecasting Model in the Stochvol package.

I have used Skewed Student-t Distribution to model the Return process in the GARCH models because the market does not react to positive and negative news in the same way (there is more volatility when any bad news comes in as compared to the volatility on the coming of any good news). 

There are seven variants available for GARCH models in rugarch: **sGARCH, fGARCH, eGARCH, gjrGARCH, apARCH, iGARCH, and csGARCH**. Further, eight sub-variants are available for the fGARCH variance model: **GARCH, TGARCH, AVGARCH, NGARCH, NAGARCH, APARCH, GJRGARCH, and ALLGARCH**.

The in-sample data consists of NIFTY50 daily (Adj. Closing Price) returns from "2007-09-18" to "2020-12-31". I have backtested the forecasting results on the daily returns of 248 trading days of the year 2021. I have calculated the VaR on 90%, 95%, and 99% confidence intervals for all models.

I have obtained the following results: The top performers at 90% confidence interval are: model alpha(10%) **apARCH 91.53226%, gjrGARCH 91.53226%, csGARCH 91.53226%, fGARCH_APARCH 91.53226%, fGARCH_GJRGARCH 91.53226%**

The top performer at 95% confidence interval is: model alpha(5%) **csGARCH 95.96774%**

The top performer at 99% confidence interval is: model alpha(1%) **fGARCH_AVGARCH 98.79032%**

**The stochastic Volatility Forecasting Model performed poorly at all three levels giving a meager accuracy of 86.29% (breached 90% confidence bar 34 out of 248 trading days), an accuracy of 92.74% (breached the 95% confidence bar (18 out of 248 trading days) and an accuracy of 98.39% (breached 99% confidence bar 4 out of 248 trading days).**
