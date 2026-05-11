# Data Analysis: Exploring eBay Car Sales Data

## Project Overview
This project involves cleaning and analyzing a dataset of used car listings from *eBay Kleinanzeigen*, a classifieds section of the German eBay website. The primary focus is to prepare a "dirty" scraped dataset for analysis and identify trends in the German used car market.

## Objectives
* **Data Cleaning**: Identify and correct issues with the scraped data (e.g., incorrect data types, string-to-numeric conversion, null values).
* **Exploratory Analysis**: Investigate the relationship between car mileage and price, and identify which brands maintain the highest resale value.

## Dataset
The dataset (`autos.csv`) contains **50,000 data points**.

**Key Columns:**
* `name`: Name of the car.
* `price`: The listed selling price (requires cleaning).
* `odometer`: Distance driven in km (requires cleaning).
* `registration_year`: The year the car was first registered.
* `brand`: The brand of the car.
* `unrepaired_damage`: Whether the car has existing damage.

## Skills Demonstrated
* **Pandas & NumPy**: Advanced use of dataframes for cleaning and aggregation.
* **Data Transformation**: Converting CamelCase headers to snake_case and translating German categorical data.
* **Statistical Cleaning**: Identifying and removing outliers (e.g., unrealistic prices or registration years).
* **Aggregation**: Using the `groupby` concept (via loops and dictionaries) to analyze data by brand and mileage.
* **Translation Mapping**: Using dictionaries to translate German categorical values into English.
