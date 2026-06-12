# Project Overview
This project delivers data transformation and business intelligence solution designed to analyze global corporate sales performance. The objective was to take a raw financial dataset, orchestrate a data cleaning pipeline via Power Query, and build a Power BI dashboard.

This dashboard gives a clear, comprehensive view of the company’s health. It outlines key metrics like revenue and total orders alongside regional and product breakdowns, making it easy to track growth and see which products are driving the highest margins.

## Data Cleaning & Power Query ETL Architecture
To guarantee absolute reporting integrity, the raw transactional dataset (Table1) was run through the Excel Power Query Editor to standardize text structures, eliminate anomalies, and align data types. 

1. Blank Row Elimination: Removed structural blank rows across the spreadsheet matrix to prevent analytical distortions and calculation gaps in aggregate fields.
2. Duplicate Row Purging: Removed duplicate records to enforce strict row-level uniqueness.
3. Whitespace Trimming: Trimmed the Country column to strip leading or trailing spaces.
4. Text Case Standardization: Applied the Proper function to the Country column to capitalize first letters and standardize the column, as some rows were uppercase or lowercase.
5. Acronym Normalization: Performed explicit value-replacements on structural anomalies, correcting case errors by transforming "Usa" to its official abbreviation "USA" to prevent broken, split groupings.
6. Selecting Right Data Types: Converted generic numbers and text fields into accurate data properties. This included casting numeric fields into Currency and raw strings into a Date data type to unlock advanced time-series rendering. 

<img width="1366" height="768" alt="Screenshot (26)" src="https://github.com/user-attachments/assets/92a2c8a3-3467-4d8e-8616-4b44d8b577ae" />

## The Dashboard
The dashboard was created using PowerBI and it features a Filters Panel, allowing interactive slicing across Segment, Country, Product, and Year. Users can seamlessly toggle between three custom views using top navigation buttons while keeping all filters completely intact:

### View A: Sales Overview Matrix
Designed to analyze market share, sales channels, and seasonal demand. 
- Geographic Distribution: Highlights revenue generation across global lines.
- Market Segmentation: Confirms Government ($53M) and Small Business ($42M) command the majority of top-line revenue, while Midmarket and Channel Partners act as minor revenue drivers ($2M each). 


### View B: Profit Overview Matrix
Exposes the financial health of regions, products, and discount structures. 
•	Regional Market Profitability: Positions Germany as the top profit generator at $3.3M, with Mexico following at $3.0M, proving these regions manage lower underlying operational expenses. 
•	Product Deficit Hotspots: Flags deep structural losses in the Amarilla (-$23M) and VTT (-$22M) product lines. 
•	Discount Mix Realities: Confirms that promotional pricing heavily strains margins, with high discount tiers creating a deep net loss. 

### View C: Orders Overview Matrix
Tracks physical logistics and order volume distribution to assess underlying supply chain activity. 
•	Logistical Load Balances: Order frequencies are evenly split across major geographic lines, with Canada leading at 0.25M transactions, followed closely by France (0.24M) and the USA (0.23M). 
•	Operational Strain by Segment: The Government segment commands the highest order density with 0.47M individual units processed, highlighting its high administrative and supply chain requirements. 
•	Promotional Volume Dependency: Confirms that promotional discounting heavily drives total order velocity, with High and Medium discount structures accounting for 35% and 34% of total transaction frequency. 

## Analytical Stack & System Architecture
•	ETL Core Engine: Microsoft Excel Power Query
•	Visualization: PowerBI Desktop
 
## How to Use the Repository
1.	Download the Global Sales Project.pbix (Power BI) and Sales_Data_Cleaned.xlsx files.
2.	Open the Power BI dashboard file.
3.	Utilize the left-hand Filters panel to interactively slice through demographics, product types, and timelines. 
4.	Click the top right bookmark buttons to switch instantly between the Sales, Profit, and Orders overview dashboards. 

