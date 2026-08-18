# Used Car - Important Factors Impacting the Price 
We explored a dataset contained information on 426K used cars. Our goal is to understand what factors make a car more or less expensive. 

# Business Understanding
## Objective: 
By understading the factors impacting the used car price, we comeup with list of items what customers value the most. With this we will help the used car dealership to manage their inventory and maximize returns.

# Data Understanding
Original dataset contains 3 million used car details, we are using the subset of 426K records.
Target Var: price
Key Features: year, odometer, manufacturer, model, title_status, transmission, drive, size, type, color, state, fuel, condition and cylinders

# Data Preparation
Data contains outliers (like <$500 or >$100000), so we cleaned up data with following conditions.
1. Price range between 500 and 100000 dollars
2. Odometer between 1 and 300000 miles
3. Missing values - dropped any missing values for the key columns listed above.
4. Categorical encoding - Columns contain string values were converted to numeric values.

# Modeling
We are using LASSO regression model with a preprocessing pipeline to scale and categorize data.

# Requirements to execute
Python - 3.X

Python libraries - pandas, numpy, matplotlib, scikit-learn

Notebook: https://github.com/sbrithiviraj/used_car_price_analysis/blob/main/usedcarpriceanalysis.ipynb

# Data
vehicles.csv (has to be downloaded from Required Assignment 11.1: What Drives the Price of a Car? )

# Report
![Top Factors influencing used car price](images\price_impact_plots.png)

## Best Model
Out of the 3 model plots shown above, Lasso Regression results looks promising though the performance metrics are not very different between 3 models. Highlights of the predictions are as follows.

## Key factors impacting price positively
1. Diesel engines are the most popular feature, customers were ready to pay 12K more.
2. Followed by year manufactured as expected the latest cars has big impact in the price
3. Size of the engine and pickup trucks also has a positive impact
4. Clean title cars are 3K more 
5. Brand - toyota has a very good resale price.

## Key factors impacting price negatively

1. FWD lost lot of value
2. Followed by car driven the most
3. Small size cars including hatchbacks and sedans are less popular
4. Gas cars lost close to $2K
5. Brand - Nissan and Hyundai are less expensive

## Recommendations to customer (Used car dealership)

| Action | Recommendation | Justification |
|--------|----------------|---------------|
|Prioritize | AWD, Trucks & Pickups | Combination of these vehicles provide the highest profit marigin |
|Target | Diesel Vehicles | Diesel trucks or SUVs have highest consumer demand |
|Avoid / Limit | High milage FWD sedans / hatchbacks | These vehicles lost lot of values and margin will be very low. |
|Brand Focus | Toyota | Toyota vehicles has good resale price whereas Nissan and Hyundai lost lot of values.

## Next steps
Upgrade the underlying data availability, consider using the vehicle history from Carfax, current market dynamics from KBB.