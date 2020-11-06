# Conclusions



- R-squared - 0.532, which means a little more than half of the observed variation in price can be explained by the model's inputs
- All p-values in the model are lower than a 0.05 threshold. With the null hypothesis being that any particular characteristic of a house has no effect on the house's price, we can reject that hypothesis when discussing these features. In other words, there is a less than 5% chance that the included features do not have an effect on a home's price. 

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

- For area-related categories such as living square footage, basement square footage, and lot square footage, the data is likely influenced as to whether a home is in an urban, suburban, or rural area. An apartment in Seattle is different than a rural farmhouse. I would develop more useful models for different zip codes.

- See if older houses being worth more is correlated to zip codes. I suspect that this finding is related to urban areas with older housing stock.
- Dive into the engineered feature of “active market score” and investigate more how these scores affect prices.



 