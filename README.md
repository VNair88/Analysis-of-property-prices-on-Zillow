# Analysis-of-property-prices-on-Zillow
Analysis of prices of properties listed on Zillow and their interaction with social stats such as unemployment and cime rates

### Datasets
County Dataset - County wise property information for all states for each month from 04/1996 to 12/2017. 
City Dataset - City wise property information for all states for each month from 04/1996 to 12/2017. 
Lookup files - Files that link county and city information to State level information.
Unemployment statistics - Unemployment rates for the following states: Massachusetts, New Jersey, Washington, California and DC for each month from 04/1996 to 12/2017. 
Crime statistics - Crime statistics for each city for all states for 2014, 2015 and 2016.
Statecode file - File that links states to corresponding state abbreviations. Used for plots.


### Tech Stack
The following packages are used for the analysis:
numpy, pandas, matplot, seaborn, sklearn.

### Analysis 1
#### Do unemployment rates affect property prices?

Trend of property prices in MA, NJ, WA, CA & DC
![alt text][logo]

[logo]: https://github.com/VNair88/Analysis-of-property-prices-on-Zillow/blob/master/Plots/Picture1.png  "Plot1"

Trend of unemployment rates in MA, NJ, WA, CA & DC
![alt text][logo1]

[logo1]: https://github.com/VNair88/Analysis-of-property-prices-on-Zillow/blob/master/Plots/Picture2.png  "Plot2"


Knowing the unemployment rate threshold which dictates whether houses will majorly gain in value is valuable information for real estate firms, lenders, insurance companies and even for homeowners seeking to buy (or sell). In case of a recession, this information is very useful for economists who might be devising bailout or loan-forgiveness strategies. For real estate firms, it can help reconfigure their investment strategies, or their marketing strategies, if already invested in areas of high unemployment.

### Analysis 2
#### County-level analysis of well-performing housing markets 
A sign of a well-performing housing market (as measured by higher than average home values) is the number of days it spends on the market while being sold, and additionally, also the inventory present in that region.

Trend of unemployment rates in MA, NJ, WA, CA & DC
![alt text][logo2]

[logo2]: https://github.com/VNair88/Analysis-of-property-prices-on-Zillow/blob/master/Plots/Capture.JPG  "Plot3"

'>State_avg' - denotes average property prices in a county are more than the state average <br>
'DaysonZillow_bin' - If the average number of days, properties in a county spend on Zillow is less than or equal to 80.063 days then the value is 1, otherwise 0 <br>
'Inventory_bin' - If the inventory size is less than or equal to 288.5, then the value is 1 otherwise 0


If a county's market is relatively active and big, it has a better chance of outperforming the state (wrt avg house prices).  

### Analysis 3
#### Impact of Crime on Home Values 

Classification tree
![alt text][logo3]

[logo3]: https://github.com/VNair88/Analysis-of-property-prices-on-Zillow/blob/master/Plots/Capture1.JPG  "Plot4"

In general, if a city has a crime rate below the state average, that city will likely have above the state average home values which is expected. 
However, it is interesting to note when looking at a lower depth on the left, that some cities have high crime rate(above 120 per 10,000) but within that group, if property crime rate is above 215 per 10,000 then the city has high home values where less property crime has low home values.
