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
