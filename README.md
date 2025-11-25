# Car Dataset ETL & Exploratory Data Analysis (EDA)
## Project Overview

This project demonstrates an ETL (Extract, Transform, Load) pipeline and Exploratory Data Analysis (EDA) on a car dataset.
The goal is to extract raw data, analyze trends in car prices, mileage, age, fuel type, and ownership, and prepare the data for further transformation and loading. Insights from the EDA can support pricing strategies, inventory management, or predictive modeling.

### **1. Data Source & Extraction**

The raw dataset was obtained from Kaggle, containing information about cars including model specifications, prices, and other attributes.

*Details:*
- Platform: Kaggle
- File type: CSV (train_data)
- Purpose: Serve as input for the ETL pipeline

*Extraction Process:*
1. The dataset was downloaded manually from Kaggle.
2. Using pandas, the CSV was loaded into a DataFrame in Python.
3. Initial inspection confirmed the structure, column names, and potential quality issues.

*Outcome:*
- Raw data successfully imported into a DataFrame
- Ready for transformation and analysis

### **2. Transforming and Loading the Data**
-----------------------------------------------------------------------------------------

### **3. Exploratory Data Analysis (EDA)**

After extraction, we performed EDA to uncover trends and insights in the car dataset.

**Key Columns**
- Price_EUR – Price of the car in Euros
- Brand – Car brand
- Year – Manufacturing year
- Kilometers_Driven – Distance traveled
- Fuel_Type – Fuel type (e.g., Petrol, Diesel)
- Mileage_L/100km – Fuel efficiency
- Owner_Type – Owner category (First, Other)

**Libraries Used**
pandas, numpy, matplotlib, seaborn

**Analysis & Insights**
1. Car Price Distribution – Histogram shows typical price ranges and outliers.
2. Cars by Fuel Type – Bar chart reveals the most common fuel types.
3. Average Price by Brand – Bar and pie charts compare mean prices across top brands.
4. Car Age vs Price – Scatter plot illustrates depreciation trends.
5. Kilometers Driven Distribution – Histogram visualizes mileage patterns.
6. Fuel Efficiency vs Price – Scatter plot shows how efficiency relates to pricing.
7. Owner Type Distribution – Pie chart highlights first vs other owners.
8. Mean Price by Brand & Owner Type – Bar chart compares first-owner and other-owner pricing.
9. Average Price by Year – Bar plot shows mean price trends across manufacturing years (average_price_by_year.png).

### **4. Conclusion**

This EDA provides a comprehensive understanding of the dataset:
- Pricing trends across brands, ownership types, and manufacturing years
- Market preferences for fuel type and mileage
- Relationships between car age, mileage, fuel efficiency, and price
- These insights can guide pricing strategy, inventory decisions, or predictive modeling.