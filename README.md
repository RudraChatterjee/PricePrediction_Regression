# UsedDevices_PricePrediction_LinearRegression

## Summary

Explored the dataset of a company that specializes in the reselling of used and refurbished devices. The objective of this project was to determine the future price of used phones and identify the factors that significantly influence them.
EDA was carried out to answer some key business questions and draw out actionable insights. Missing values in the dataset were treated and feature engineering was performed on other variables. Outlier values in different variables were explored.

A linear regression model was used to determine the projected cost of used devices. One-Hot encoding was utilized for categorical values.  A linear regression model was made with statsmodels.api. Multicollinearity in a number of predictor variables were treated using variance inflation factors (VIF). 
Variables with  high p-values were explored and systematically removed. Final model was tested for linearity, independence, and normality—determined homoscedasticity through the Goldfeld Quandt test.


## Business Context
Buying and selling used phones and tablets used to be something that happened on a handful of online marketplace sites. But the used and refurbished device market has grown considerably over the past decade, and a new IDC (International Data Corporation) forecast predicts that the used phone market would be worth $52.7 billion by 2023 with a compound annual growth rate (CAGR) of 13.6% from 2018 to 2023. This growth can be attributed to an uptick in demand for used phones and tablets that offer considerable savings compared with new models.

Refurbished and used devices continue to provide cost-effective alternatives to both consumers and businesses that are looking to save money when purchasing one. There are plenty of other benefits associated with the used device market. Used and refurbished devices can be sold with warranties and can also be insured with proof of purchase. Third-party vendors/platforms, such as Verizon, Amazon, etc., provide attractive offers to customers for refurbished devices. Maximizing the longevity of devices through second-hand trade also reduces their environmental impact and helps in recycling and reducing waste. The impact of the COVID-19 outbreak may further boost this segment as consumers cut back on discretionary spending and buy phones and tablets only for immediate needs.

## Objective
The rising potential of this comparatively under-the-radar market fuels the need for an ML-based solution to develop a dynamic pricing strategy for used and refurbished devices. A startup company aiming to tap the potential in this market wants to analyze the data provided and build a linear regression model to predict the price of a used phone/tablet and identify factors that significantly influence it.

## Data Description
The data contains the different attributes of used/refurbished phones and tablets. The data was collected in the year 2021. The detailed data dictionary is given below.

brand_name: Name of manufacturing brand
os: OS on which the device runs
screen_size: Size of the screen in cm
4g: Whether 4G is available or not
5g: Whether 5G is available or not
main_camera_mp: Resolution of the rear camera in megapixels
selfie_camera_mp: Resolution of the front camera in megapixels
int_memory: Amount of internal memory (ROM) in GB
ram: Amount of RAM in GB
battery: Energy capacity of the device battery in mAh
weight: Weight of the device in grams
release_year: Year when the device model was released
days_used: Number of days the used/refurbished device has been used
normalized_new_price: Normalized price of a new device of the same model in euros
normalized_used_price: Normalized price of the used/refurbished device in euros





## Actionable Insights and Recommendations
- Final linear regression model can explain 84% of the data variability and can be used to predict the normalized used price for smartphones/tablets within 4.6% of their actual price based on test data. This indicates that the model is broadly well suited for prediction as well as inference purposes.

- Broadly, the company can look to increase in acquiring used/refurbished devices in their inventory with certain attributes
    * higher new price
    * increased RAM size
    * higher main and selfie camera resolutions
    * higher weight
    * availability of 4G
    * newer release dates

- The company can also try to obtain user demographic data such as age, gender, annual income, occupation, geographic location to have a better sense of demand understanding and customer segmentation. For example, there may be a preference for phones with better camera resolutions or 4G availability based on gender or in younger individuals.

- 73% of all brands in the dataset offer high quality selfie cameras (greater than 8 MP). The startup can focus on acquiring used devices from those brands and also develop targeted ads for those brands towards demographics that prefer phones with better camera resolutions

- Income/occupation/location information may gauge better understanding the affordability preferences of individuals. Higher income individuals may be more willing to buy more expenesive smartphones and/or replace existing smartphones to buy a new one compared to lower income individuals

- Understanding these behaviors can help the company create better targeted ads for different customer segments accordingly which can lead to higher sales and greater revenue

- 50% of the used device dataset comprises of older devices with release years from 2013-2015 while only 30% make up newer devices released between 2018-2020. This may suggest a larger market availability for older devices. The company is recommemded to increase their inventory share of used devices with newer release dates as these sell for higher prices relative to devices with older release dates.

- Alternatively given the right customer segmentation strategy, older devices may be more appealing to lower income customers or customers looking to spend less money and this segment could be targeted for older devices
