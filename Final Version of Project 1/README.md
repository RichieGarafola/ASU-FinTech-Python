# Travel Planner Based on Currency Conversion Risk
**Project Goal:**  Create a travel planning tool that will allow the user to select a set of countries they would like to travel to and a travel timeframe (3,6,12 months).  The tool will analyze historical Forex data and predict the country that will have the most favorable currency within the given travel timeframe.

**The tool will:**
Check Forex volatility as barometer for travel decisions
Use historical forex data (up to 2 years)
3 - 6 - 12 months predictive outlook using Monte Carlo and other algorithms
Produce graphs, risk graphs, value graphs,
Variables - currency / country,  traveling times (3-6-12 months)

**Questions:**
# #
- What is the variability of budget in base currency (USD) of the three locations selected ? 
- Rank the travel location by risk of currency fluctuation ( what is the risk? )
- Give the zone of values based on Monte-Carlo simulation is it wide closely similar etc based on locations selected/
- Is there correlation between weather variability and foreign currency variability

**Analysis**
# #
The tool is able to dynamically accept ( 3 ) countrues of origin determine the currency of the selected countries dynamically pull country information and statistics the using the Alpha Vantage API pull the Forex currency trading pair to determine the current value

We then normalize the values in the pair to USD denominator so that all the comparisons are based on USD value.

We then perform a MonteCarlo simulation to determine the range of values for that pair and compare the range and variance and display that information to the traveler in the form of graphs and summary text ( In the presentaton and code example select we chose periods of 3 months, 6 months and 12 months for time till traveling time frame.

The data source we had selected for dynamically pulling historical weather data fell thru as it was cost prohibitive for the amount of data  we needed. The free version of historical weather was limited to ( 3 ) days which is not useful for this analysis so it was scrapped from the resulting project

**Results:**

Example Country 1: Singapore
#
   Monte Carlo
    ![](https://github.com/Scott-ECO/Project_1/blob/main/Final%20Version%20of%20Project%201/Resources/MonteCarloPlot1.PNG)

   Beta
    [![](https://github.com/Scott-ECO/Project_1/blob/main/Final%20Version%20of%20Project%201/Resources/Beta1.PNG)
    
Example Country 2: Turkey
#
   Monte Carlo
    ![](https://github.com/Scott-ECO/Project_1/blob/main/Final%20Version%20of%20Project%201/Resources/MonteCarloPlot1.PNG)
    
   Beta
    ![](https://github.com/Scott-ECO/Project_1/blob/main/Final%20Version%20of%20Project%201/Resources/Beta2.PNG)

Example Country 3: United Kingdom
#
   Monte Carlo
    ![](https://github.com/Scott-ECO/Project_1/blob/main/Final%20Version%20of%20Project%201/Resources/MonteCarloPlot1.PNG)
    
   Beta
    ![](https://github.com/Scott-ECO/Project_1/blob/main/Final%20Version%20of%20Project%201/Resources/Beta3.PNG)
    

### Comparison Statistics and Ratios

- Standard Deviations ( Daily ):
    - SGDUSD Daily Returns       0.003131
    - TRYUSD Daily Returns       0.012750
    - GBPUSD Daily Returns       0.005972
    - US Dollar Daily Returns    0.004215

- Standard Deviations ( Annuakized ):
    - SGDUSD Daily Returns       0.049708
    - TRYUSD Daily Returns       0.202403
    - GBPUSD Daily Returns       0.094802
    - US Dollar Daily Returns    0.066910
#
- Assets Riskier than the US Dollar
    - SGDUSD Daily Returns       False
    - TRYUSD Daily Returns        True
    - GBPUSD Daily Returns        True
    - US Dollar Daily Returns    False

### What Countries Currency is the riskiest?
    - Turkey
### What country is the most volatile?
    - Turkey

### What Country is the most stable with least volatile?
    - Singapore

### Overview or Suggestion to Traveler?

Due to the volatility and greater devaluation against the US Dollar travelers should hold off on converting currency today and exchange closer to their travel date. The risk is due to the volatility spikes in daily returns this could impact the expected receipt of income. All three of the examples including the most stable have a (negative) beta to USD and thus devaluing over time the most pronounced is Turkey however beta is relatively flat . There is little advantage to converting now and should be done closer to date of travel for all currencies selected.

## Appendix

### Volatility
![](https://github.com/Scott-ECO/Project_1/blob/main/Final%20Version%20of%20Project%201/Resources/Volatility-ALL.PNG)

### Correllation
![](https://github.com/Scott-ECO/Project_1/blob/main/Final%20Version%20of%20Project%201/Resources/Correllation-ALL.PNG)

### Skewness (Box plot)
![](https://github.com/Scott-ECO/Project_1/blob/main/Final%20Version%20of%20Project%201/Resources/Boxplot_ALL.PNG)

### Daily Returns
![](https://github.com/Scott-ECO/Project_1/blob/main/Final%20Version%20of%20Project%201/Resources/DailyReturns-ALL.PNG)

### Cumulative Returns
![](https://github.com/Scott-ECO/Project_1/blob/main/Final%20Version%20of%20Project%201/Resources/CumulativeReturns-ALL.PNG)
