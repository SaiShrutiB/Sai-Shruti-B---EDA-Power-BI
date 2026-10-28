**Week 9 – Housing Data Cleaning & Transformation**

**About the Project**
This project focuses on cleaning and transforming the King County housing dataset using Power BI. The aim was to prepare the raw housing data for further analysis by correcting data types, creating new columns, and filtering out invalid property records.

**Tools Used**
Power BI
Power Query
DAX

**Work Done**
Imported kc_house_data.csv into Power BI.
Checked column quality and reviewed the data for errors and missing values.
Corrected data types and converted the sale date using the appropriate locale.
Created new columns:
Sale Year – extracted from the sale date.
Sale Month – extracted from the sale date.
Property Age at Sale – calculated using the sale year and construction year.
Price per SqFt – calculated from price and living area.
Total Area – calculated by adding living area and lot area.
Is Renovated – identifies whether a property has a recorded renovation year.
Property Size – classifies properties as Small, Medium, Large, or Luxury.
Price Tier – classifies properties as Budget, Mid-Range, Premium, or Luxury.
Filtered out properties with zero bedrooms and zero bathrooms.
Loaded the transformed data into Power BI for further analysis.

**Outcome**
The housing dataset was cleaned and enriched with additional columns that make it easier to compare properties based on their size, price, age, and renovation status. The prepared data was then used for the Week 10 real-estate dashboard.

**Dataset**
kc_house_data.csv – King County housing dataset.
