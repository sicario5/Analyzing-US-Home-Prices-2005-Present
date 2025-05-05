# Analyzing-US-Home-Prices-2005-Present-
Build a data science model to explain how key economic factors influenced US home prices (measured by the S&amp;P Case-Shiller Home Price Index) over the last 20+ years.

#Publicly available data from FRED (Federal Reserve Economic Data):
1. Target Variable:
-CSUSHPISA (Case-Shiller US National Home Price Index)

2.  Predictor Variables:
-Interest Rates: 30-Year Mortgage Rate (MORTGAGE30US)
-Employment: Unemployment Rate (UNRATE)
-Supply: Housing Starts (HOUST)
-Demand: Median Household Income (MEHOINUSA672N), Population (POPTHM)
-Macroeconomic: Real GDP (GDPC1), Rent CPI (CUUR0000SEHA)

#Methodology
1. Data Collection:
-Manually downloaded CSV files from FRED (2000–present).

2. Preprocessing:
-Aligned all data to a quarterly frequency (resampling).
-Handled missing values with forward-fill (ffill()).
-Applied log transforms to non-stationary variables (e.g., GDP, Income).

3. Exploratory Analysis (EDA):
-Time series plots to visualize trends.
-Correlation heatmap to identify key relationships.

4. Modeling:
-Linear Regression: Quantified impact of predictors on home prices.
-ARIMAX: Accounted for autocorrelation in time series data.

5. Validation:
-Residual analysis to check model assumptions.
-Train-test split (80/20) to evaluate performance.

#Key Findings
1. Primary Drivers of Home Prices:
-Negative Impact: Mortgage rates (+1% → ~1.5% decrease in prices).
-Positive Impact: Household income (+1% → ~0.6% increase in prices).
-Supply Constraints: Fewer housing starts correlated with price surges.

2. Historical Trends:
2005–2006: Prices rose due to low mortgage rates and loose credit.
2008–2012: Crash driven by high unemployment and subprime crisis.
2012–2020: Recovery fueled by low rates and limited supply.
2020–2025: Pandemic-driven demand and supply-chain disruptions caused record highs

#Tools Used
1. Python Libraries:
-pandas (data wrangling), statsmodels (regression/ARIMAX).
-matplotlib/seaborn (visualization).

2. Data Sources:
-FRED (CSV files downloaded manually).


