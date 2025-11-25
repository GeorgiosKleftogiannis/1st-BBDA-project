**Exploratory Data Analysis (EDA) on Car Dataset**
*** Project Overview ***

This project performs an Exploratory Data Analysis (EDA) on a dataset of car listings. The analysis aims to uncover patterns, trends, and insights related to car prices, brands, mileage, age, fuel type, and ownership. The dataset has been preprocessed and transformed for analysis.

*Dataset*
- Source: Final_car_data.csv (transformed and cleaned)
- Columns include:
  - Price_EUR – Price of the car in Euros
  - Brand – Car brand
  - Year – Manufacturing year
  - Kilometers_Driven – Distance the car has traveled
  - Fuel_Type – Type of fuel used (e.g., Petrol, Diesel)
  - Mileage_L/100km – Fuel efficiency
  - Owner_Type – Type of owner (e.g., First, Other)

*Libraries Used*
- pandas – Data manipulation and analysis
- numpy – Numerical computations
- matplotlib – Visualization
- seaborn – Statistical data visualization

*Analysis Steps & Insights*
1. Distribution of Car Prices
Histogram shows how car prices are distributed across the dataset.
Helps identify typical price ranges and outliers.

2. Cars by Fuel Type
Bar chart visualizing the number of cars for each fuel type.
Provides insights on the most common fuel types in the market.

3. Average Price by Car Brand
Top 10 brands are selected to compare average prices.
Bar chart and pie chart display mean price per brand, highlighting premium and budget brands.

4. Car Age vs Price
Scatter plot of car age (calculated as 2024 - Year) vs price.
Helps visualize how car depreciation affects pricing.

5. Kilometers Driven Distribution
Histogram showing distribution of kilometers driven.
Useful for understanding mileage trends across the dataset.

6. Fuel Efficiency vs Price
Scatter plot of fuel efficiency (L/100km) against price.
Explores whether more fuel-efficient cars are priced higher or lower.

7. Percentage of Owner Types
Pie chart showing the proportion of first owners vs other owners.
Helps analyze market trends based on ownership.

8. Mean Price by Car Brand & Owner Type
Comparison of mean prices for each brand between first owners and other owners.
Bar chart highlights differences in pricing based on ownership history.

9. Average Car Price by Year of Manufacturing
A bar plot shows the mean (average) price of cars, grouped by their manufacturing year.
This plot helps identify trends in car pricing over the years, such as whether older cars are significantly cheaper and how prices have changed over time.

*Conclusion*
- This EDA provides a comprehensive understanding of the car dataset:
- Pricing trends across brands and ownership types
- Market preferences for fuel type and mileage
- Relationship between car age, mileage, fuel efficiency, and price
- These insights can be leveraged for pricing strategy, inventory management, or further predictive modeling.