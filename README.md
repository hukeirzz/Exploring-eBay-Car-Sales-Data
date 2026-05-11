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

## Key Findings & Results

### 1. Brand Price Hierarchy
Our analysis of the top 6 brands (those representing >5% of total listings) revealed a clear pricing structure in the German used car market:
* **Luxury Tier**: **Audi, Mercedes-Benz, and BMW** lead the market with average prices ranging between **$8,000 – $9,300**.
* **Mid Tier**: **Volkswagen** sits in the middle at approximately **$5,400**.
* **Budget Tier**: **Ford and Opel** are the most accessible, averaging between **$3,000 – $3,700**.

### 2. Brand Value vs. Mileage
Interestingly, average mileage remained remarkably consistent across all top brands, regardless of price tier, typically hovering between **128,000 km and 130,000 km**. 
* **Conclusion**: The significant price gap between luxury and budget brands is driven by **brand prestige** and original market positioning, rather than the luxury cars having lower mileage.

### 3. Impact of Unrepaired Damage
The condition of the vehicle is one of the strongest predictors of price. After translating and aggregating the data, we found:
* **Non-Damaged Cars**: Average price of **$7,164**.
* **Damaged Cars**: Average price of **$2,241**.
* **The "Damage Tax"**: On average, cars without damage are **$4,923 more expensive** than those with unrepaired damage—a price difference of nearly **220%**.

### 4. Market Trends
* **Dominance**: **Volkswagen** is the most popular brand by a wide margin, accounting for nearly **20%** of all listings.
* **Age Profile**: The most common registration years in the dataset are **1999–2005**, indicating a high volume of cars aged 10–15 years at the time the data was crawled.
