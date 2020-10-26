# Overview

Created for a data science course with Flatiron School, the idea behind this project was to analyze housing data as if I were an advisor to a real estate company. The model created will help the company understand what features contribute to a property's worth in King County, Washington.



The main notebooks in this repository are:

- 1_Data_Cleaning_and_EDA
- 2_Iterative_Modeling



# Process and Tools

Data for the analysis came from a dataset of sales in King County. I also merged the dataset with 2015 U.S. Census data.

Some high level info about this data: 

- Number of homes sold: 21,597
- Dates of sale: 2014 - 2015
- Price range: $77,000 - $7,700,000
- Mean price: $540,200
- Year houses built: 1900 - 2015
- Living area (mean): 2080 sq. ft.
- Lot area (mean):15,100 sq. ft.
- Population of King County (2015): 51,477,000



# Exploratory Data Analysis

I began this project by exploring the dataset, deciding which features were relevant to my goal and eliminating outliers. 

I ran Seaborn heatmaps to check for collinearity among features and checked for Variance Inflation Factors (VIF), and I eliminated certain features that were above a threshold.

With the census data, I also engineered a feature I called "active market score" which is a ratio based on the number of sales in a zip code per the zip code population.  

# Modeling

My original model didn't work well for higher price homes, so I ended up limiting the homes to those priced $900,000 or less. I also standardized some continuous features related to a home's square footage (living space, lot, and basement). Also to get a better model, I broke "year built" into groups of six categories and also created a category called "recently renovated" for properties that had been renovated in the previous 25 years. 



# Conclusions

- R-squared - 0.532, which means a little more than half of the observed variation in price can be explained by the model's inputs
- All p-values in the model are lower than a 0.05 threshold. With the null hypothesis being that any particular characteristic of a house has no effect on the house's price, I can reject that hypothesis when discussing these features. In other words, there is a less than 5% chance that the included features do not have an effect on a home's price. 

### Coefficient Interpretation

#### Area data

If all other variables stay constant:

- For each 910.9 increase/decrease in living square footage, we expect a home's price to average increase/decrease $61,380.
- For each 39,842 increase/decrease in lot square footage, we expect a home's price to average increase/decrease $2,565.
- For each 437.5 increase/decrease in basement square footage, we expect a home's price to average increase/decrease $722.

#### Other data

- For every grade a house increases, its value is expected to rise $112,000 
- Houses in an active market command higher prices than similar houses in less active markets
- If a house is located on a waterfront, it is expected to be worth $143,200
- Houses renovated within the last 25 years are expected to be worth $21,180 more.
- Each additional floor added to a house is expected to increase its worth $29,520.
-  The model does not incorporate the age of houses built since 1980. Houses in older age groups tend to be worth more, perhaps because of urban locations.  
  - 1900-1919



## Additional research 

If I had more time to spend with this project, I would have investigated other areas. 

- For area-related categories such as living square footage, basement square footage, and lot square footage, the data is likely influenced as to whether a home is in an urban, suburban, or rural area. An apartment in Seattle is different than a rural farmhouse. I would develop more useful models for different zip codes.

- I would see if my finding that older houses being worth more is correlated to zip codes. I suspect that this finding is related to urban areas that have older housing stock.
- I would dive into the engineered feature of “active market score” and investigate more how these scores affect prices.



 