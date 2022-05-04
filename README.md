# Time-Series-Analysis----Fbprophet and Auto-Arima
# Analysis Objectives
* Perform daily time series analysis on the sales of 20 ditinct product.
* This dataset had more than 4000 unique products and I didn't have the computing power to perform this analysis on all of them.
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
![Screen Shot 2022-05-03 at 11 15 01 PM (3)](https://user-images.githubusercontent.com/79353291/166631275-8740e111-6ae5-4d79-8e2b-853209319bf1.png)

* Imputed the missing dates by grouping them by dates and unique products and then used resample function in pandas and it imputed the missing dates for all the products and set it to zero.
![Screen Shot 2022-05-03 at 11 18 10 PM (3)](https://user-images.githubusercontent.com/79353291/166631391-f122f9f2-fcae-42fe-b504-46a828e8413e.png)

* Since I’ve decided to only use this analysis on 20 products, my strategy and logic were to find the products which have the same date range of sales as our main
data frame ('2010-12-01' : '2011-12-09'), after doing such an operation I found that out of 4070 distinct products only 566 of them had the same date range. I decided to check every one of them and count the number of non-zero sales for every day in them, and take the top 20 products with the least amount of zero sales.

# Model Building
Train Date Range: ('2010-12-01' : '2011-09-30') 
Test Date Range: ('2011-10-01' : '2011-12-09')





