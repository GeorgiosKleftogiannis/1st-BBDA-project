# Data Transformation

## Initial Data Loading and Inspection

The dataset was imported into a Jupyter Notebook environment using the
**Pandas** library. After loading the CSV file, the first rows, column
names, and data types were examined to understand the structure and
identify data quality issues. Summary statistics and exploratory checks
revealed several transformation requirements that guided the design of
the cleaned, analysis-ready dataset.

Key observations during this stage included:

1.  **Mixed Data Types**\
    Columns such as `Mileage`, `Engine`, and `Power` store values as
    strings combining numeric values and units (e.g., "22.5 kmpl", "1197
    CC"). These fields require parsing and normalization before being
    usable for analysis.

2.  **Unit Standardization Needs**\
    After extracting numeric components, unit conversions were required
    to align values with European measurement standards (e.g.,
    converting mileage from kmpl to L/100 km).

3.  **Missing Values**\
    Several columns contained missing or null values, particularly
    `Power`, `Engine`, `Seats`, and `New_Price`, necessitating
    appropriate handling strategies.

4.  **Opportunities for Feature Engineering**\
    Additional useful features could be derived, such as extracting the
    car manufacturer (Brand) from the `Name` column.

These insights formed the basis of the transformation workflow.

------------------------------------------------------------------------

## Transformation Workflow

The following transformation steps were applied to clean, standardize,
and structure the dataset:

1.  **Identify Missing Values**
    -   Checked the count of null entries per column to determine the
        appropriate imputation or removal strategy.
2.  **Handle Missing Data**
    -   Dropped rows with missing values in `Mileage`, `Engine`,
        `Power`, and `Seats`, where imputation was not feasible.\
    -   Filled missing values in `New_Price` with zero, where a missing
        new-car price does not affect used-car characteristics.
3.  **Mileage Parsing**
    -   Split `Mileage` into two new columns:
        -   `Mileage_Value` (numeric)\
        -   `Mileage_Unit` (kmpl or km/kg)\
    -   Dropped the original `Mileage` column.
4.  **Power Parsing**
    -   Split `Power` into:
        -   `Power_Value`\
        -   `Power_Unit`\
    -   Dropped the original `Power` column.
5.  **Engine Parsing**
    -   Extracted the numeric displacement to a new column:
        `Engine_cc`.\
    -   Removed the original `Engine` column.
6.  **Price Conversion (Indian Lakh → EUR)**
    -   Converted the used-car price to euros using:\
        **Price_EUR = Price_Lakh × 100,000 × 0.010**\
    -   Dropped the original `Price` column.
7.  **New Car Price Conversion**
    -   Extracted and converted the numeric value from `New_Price` using
        the same Lakh → EUR formula.\
    -   Dropped the original `New_Price` column.
8.  **Mileage Conversion to European Standard (L/100 km)**
    -   Defined a `fuel_density` dictionary for Petrol, Diesel, LPG, and
        CNG.\
    -   Implemented a conversion function:
        -   **kmpl → L/100 km**: `100 / mileage_value`\
        -   **km/kg → L/100 km**:
            `100 / (mileage_value / fuel_density[fuel_type])`\
    -   Created the new column `Mileage_L/100km` and removed the
        intermediate parsed columns.
9.  **Power Conversion to Kilowatts (kW)**
    -   Converted horsepower (bhp) to kilowatts using:\
        **Power_kW = 0.746 × Power_Value**\
    -   Assigned `kW` as the standardized unit.\
    -   Dropped the unconverted power columns.
10. **Value Rounding**\

-   Rounded `Mileage_L/100km` and `Power_kW` to one decimal place for
    clarity and consistency.

11. **Index Cleanup**\

-   Renamed the first column (`Unnamed: 0`) to `Index` for clarity.

12. **Brand Extraction and Normalization**\

-   Derived a new `Brand` column from the first word of the `Name`
    field.\
-   Standardized inconsistent brand representations (e.g., replaced
    "ISUZU" with "Isuzu").

13. **Seat Type Correction**\

-   Converted `Seats` from float to integer to reflect its categorical
    nature.

14. **Duplicate Check**\

-   Verified the dataset contains no duplicate records before
    finalizing.

------------------------------------------------------------------------

## Outcome

Through these transformations, the dataset was cleaned, standardized,
and aligned with European measurement conventions. This ensured that all
downstream visualizations and analyses are accurate, meaningful, and
based on a consistent data model. The resulting dataset is fully
prepared for the Exploratory Data Analysis (EDA) and dashboard
development phases.
