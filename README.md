# Time-Series-Analysis----Fbprophet and Auto-Arima
# Analysis Objectives
* Perform daily time series analysis on the sales of each ditinct product.
* Forecast the sales for the next two months and validate it on the test set.
* Compare the prophet model and auto-arima model.

# Dataset that will be utilized
* [github link](https://github.com/raminstad/Sales-Forecasting/blob/main/Data.xlsx)

# Potential Packages
* Pandas
* Numpy 
* Matplotlib
* Seaborn
* Statsmodels
* Fbprophet
* Pmdarima
* Pickle

# EDA
* For this part of the analysis, I checked the distribution of the numerical variables, checked the descriptive statistics of the numerical variables, and checked for the null values.

# Data Preprocessing
* Checked the unique values in the Quantity variable and found out that we had negative quantities, and then I changed all the negative values to zero.
* Set the index of the data frame to the Invoice Date variable
* Checked for the missing dates in our data and found out we had 69 days missing. 


* I imputed the missing dates by grouping them by dates and unique products and then used resample function in pandas and it imputed the missing dates for all the products and set it to zero.
! [Screen Shot 2022-05-03 at 11 15 01 PM (3)](https://user-images.githubusercontent.com/79353291/166631114-0b8b53ad-2c86-408d-8653-3025c10fc061.png)
