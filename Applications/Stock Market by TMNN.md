# Example Prediction of Stock Market Indexes

**Prediction of stock market indexes by analogues complexing**

On the base of observations in the period of February, 22 to May 30, 1995 (66 days) the analogue complexing algorithm was used. Table shows prediction error (MAD [%]) of four variables (Dollar, Dax, F.A.Z., Dow Jones) and the mean prediction error over 7 variables. The width of the patterns varies from 6 to 15 days.

|   |   |   |   |   |   |   |   |   |   |   |
|---|---|---|---|---|---|---|---|---|---|---|
|**Width**|**6**|**7**|**8**|**9**|**10**|**11**|**12**|**13**|**14**|**15**|
|Dollar|2.61|3.28|2.62|2.79|2.91|2.91|1.86|1.48|2.16|8.96|
|F.A.Z.|1.42|2.61|1.59|1.48|1.19|1.39|1.43|1.87|0.72|1.12|
|Dax|1.48|1.70|1.7|2.31|2.96|2.76|2.76|2.61|2.37|1.12|
|Dow J|1.36|1.71|1.62|6.98|5.39|4.65|4.97|3.85|3.36|2.79|
|**_Mean_**|**_1.17_**|**_1.57_**|**_1.58_**|**_2.36_**|**_2.46_**|**_2.08_**|**_1.94_**|**_1.79_**|**_1.63_**|**_1.88_**|

The forecasts are obtained by means of linear combination of the continuations of 5 selected analogues patterns, where the unknown weights gj of complexing are estimated by means of parametric [algorithms](http://www.gmdh.net/GMDH_alg.htm).