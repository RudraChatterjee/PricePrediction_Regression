# UsedDevices_PricePrediction_LinearRegression

Explored the dataset of a company that specializes in the reselling of used and refurbished devices. The objective of this project was to determine the future price of used phones and identify the factors that significantly influence them.

EDA was carried out to answer some key business questions and draw out actionable insights. Missing values in the dataset were treated and feature engineering was performed on other variables. Outlier values in different variables were explored.

A linear regression model was used to determine the projected cost of used devices. One-Hot encoding was utilized for categorical values.  A linear regression model was made with statsmodels.api. Multicollinearity in a number of predictor variables were treated using variance inflation factors (VIF). 
Variables with  high p-values were explored and systematically removed. Final model was tested for linearity, independence, and normality—determined homoscedasticity through the Goldfeld Quandt test.
