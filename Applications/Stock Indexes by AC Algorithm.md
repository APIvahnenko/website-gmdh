# Example Stock Market Forecasting

Currency, international stock trading and derivatives contracts play an increasing role for many investors. Commonly used a portfolio consisting of a number of contracts. Assets returns must be predicted and controlled by a prediction/control module. Control of risk via prediction/control module of individual investments returns inside the portfolio provides the most likely process.

It is known that in most economic applications i.e. financial risk control, neural networks gives success only of 70-80%. By means of the new approach of GMDH twice-multilayered neural networks it can be improved by 5-10%. Prediction accuracy for short and very noised data also increases in short and long-time predictions by 10-50% in comparison to statistical methods and neural networks, especially for stochastic processes [30,31]. On the base of predictive control it increases the results of a repetitive control.

**_Stock market indexes forecasting_**

As an example prediction of the activity on the stock exchange in New York was considered in [10]. In the following on the base of observations in the period of February 22 up to June 14, 1995 in seven periods 7 variables of the stock market (Dax, Dow Jones, F.A.Z., Dollar and other) are predicted. In the information base delays of all variables up to 35 are included. Also there were used not only linear reference functions to describe the variables, but also non-linear. It was to model and to predict 7 time series not independently as time series models but rather as highly interactions network (input - output - model). Table 1 shows the accuracy of predictions for all variables (mean MAD [%])

_Table 1:_ Observation and prediction periods.

|   |   |   |   |   |   |   |   |
|---|---|---|---|---|---|---|---|
||**Observation period**|   |**Long-term prediction period**|   |   |**Model**|**Prediction**|
||Period up to|Days|Begin|End|Days|Max delay|Mean MAD [%]|
|**a**|March, 17|18|March,20|March, 31|10|5|0.985 %|
|**b**|March, 31|28|April,3|April, 18|10|10|2.055 %|
|**c**|April, 18|38|April, 19|May, 3|10|15|0.809 %|
|**d**|April, 28|46|May, 2|May, 15|10|20|1.642 %|
|**e**|May, 15|56|May, 16|May, 30|10|26|1.217 %|
|**f**|May, 30|66|May, 31|June ,14|10|30|1.206 %|
|**g**|June, 14|76|June, 16|June, 29|10|35|0.760 %|

Using the results of model generation (at first layer of neuronet) it is possible to improve the accuracy of models in a second model generation, where the model outputs are used as input variables for next layer. This procedure can be continued up to increase accuracy of models.

Table 2 shows the resulting model error (MAPE [%]) and prediction error (MAD [%]) of Dollar, Dax, F.A.Z., Dow Jones and the mean values for all 7 variables obtained on 3 levels. It is shown that the repeated application of self-organization gives more accurate approximation, which results in better predictions in the second level. The models obtained in the third level are overfitted, therefore the prediction error increases.

_Table 2:_ Multilevel application (model **f**).

|   |   |   |   |   |   |   |
|---|---|---|---|---|---|---|
||MAPE [%]|   |   |MAD [%]|   |   |
|Level|1|2|3|1|2|3|
|Dollar|0.68|0.51|0.11|2.32|2.17|11.67|
|Dax|0.35|0.24|0.10|2.20|1.24|5.21|
|F.A.Z.|0.22|0.23|0.03|1.54|1.27|2.32|
|Dow Jones|0.27|0.16|0.06|2.15|0.84|4.84|
|**Mean**|**0.267**|**0.184**|**0.051**|**1.43**|**0.98**|**3.67**|

The efforts in construction and using of the GMDH neural networks are much less than in neural networks, where the architecture must be chosen by trial and error. Only an adaptive synthesis of the network structure allows an automatic model generation and therefore applications in the fields where lots of decisions and forecasts (monitoring of complex systems with many controlled variables) repeating over short time periods are needed.

**_Objective selection of the best model_**

It is the aim of self-organizing modeling to get in an objective way models of optimal complexity. But there is several freedom in choice of class of systems to be model (linear/non-linear), time lag and in selection of appropriate parameters (number of best models, complexity etc.). To reduce such a subjectivity it is recommended to generate several alternative models (linear, non-linear, with several complexity and time lags) and in a second layer to select the best model outputs or to generate there combination. Table 3 shows obtained results.

_Table 3_: Selection of best model results (model **g**): prediction error MAD [%].

|   |   |   |   |   |   |   |   |
|---|---|---|---|---|---|---|---|
||Linear|   |   |Non-linear|   |   |Second  <br>layer|
|Model|1|2|3|1|2|3|
|Dollar|2.88|2.1|0.89|1.25|1.41|1.4|1.55|
|F.A.Z.|1.22|1.45|1.01|0.82|1.12|1.57|0.88|
|Dax|1.36|2.41|1.51|1.69|2.43|4.54|1.94|
|Dow Jones|1.14|1.26|1.44|3.75|3.25|3.79|2.93|
|Mean|1.14|1.29|0.9|1.21|1.35|1.81|1.2|

This results were obtained by Prof.J.-A.Müller from Hochschule fur Technik und Wirtschaft (Dresden) and Dr.F.Lemke. We express our deep acknowledgments for their help.