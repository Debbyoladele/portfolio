# Electric Vehicle Analysis

## Table content
- [Project overview](#project-overview)
- [Data Sources](#data-sources)
- [Recommendation](#recommendations)


 ### Project Overview 

This project transformed messy, inconsistent business data into a clean, analysis-ready dataset and delivered an interactive Power BI dashboard that centralised Electric Vehicle charging profitability insights, enabling stakeholders to track P&L by site, region, and month, analyse sales and profit trends, and optimise infrastructure planning.
<img width="1173" height="609" alt="image" src="https://github.com/user-attachments/assets/a9aa944c-da36-47b0-b07d-13f6fe0f2c93" />




### Data Sources
Financial Data – Profit & Loss data for each site.
Master Site List – Reference dataset containing standardised site names, profit centers, regions, cities, and geographical details (latitude/longitude).

### Tools

- Excel
- SQl Server
- Python (Pandas): Data cleaning, transformations, filtering, custom mappings.
- SQL: Advanced joins, aggregations, integration with Master Site List.
- Excel Functions: XLOOKUP, UNIQUE, Find & Replace for quick validations.
- Power BI: Interactive dashboards, DAX calculations, KPIs, slicers & filters,Power Query: Unpivoting, date parsing, column profiling, reshaping.

### Data cleaning
Standardised site names, profit centers, and regions across all datasets.

Remove duplicates, invalid records, and “DO NOT USE” data entries.

Ensure complete alignment with the Master Site List for consistency and accuracy.

Handled missing data entries

### Exploratory Data analysis
The EDA phase focused on understanding the structure, quality, and relationships within the datasets (Store P&L 2019, Litres, EV, and Master Site List). The key objectives were to detect anomalies, validate consistency, and uncover initial insights before dashboard development

### Descriptive Statistics

1. Revenue & Costs (P&L):
 - What is the highest contributor
 - What is the Largest expense.

2. Is there a Positive growth trend across months?

3. Is there Monthly trends showed seasonality, with fluctuations in summer and autumn.


### Data analysis 
Some SQL codes used
``` SQL
SELECT
Clean Mapping,
Clean. ProfitCenter,
Clean. Site Mane as Unit_name,
Clean. Fiscal_year_Period，
CAST(Clean.date AS DATE) AS date,
Clean. Value
Sheet. Site_Mapping,
Sheet. City.
Sheet. County, Shee
Sheet. Latitude，
Sheet. Longitude
From
Cleandataset AS Clean
Left join

Sheet1 AS Sheet
on 
clean.profitcenter = sheet.(SAP_Profit _Contre);
```


### Data Analysis
Some Python code used
```python
import pandas as pd
df = pd.read_excel(r"C:\Users\HP\Downloads\ p&L .xlsx")
df_cleaned = df.drop_duplicates()
df_cleaned
df_cleaned = df_cleaned[df_cleaned['Site Name'] != 'DONOTUSE-Cinnabn'].copy()
df_cleaned
```

### Results/Findings
Business Insights from Dashboard

Profit & Loss Analysis:

1. North West region had the highest total value 

2.  Greater Manchester contributed 34.4% of total sales).
	
3.  Top Performer: Fuel Sales (£721m)
  
4. North West had the highest total value
5.   Showed value growth trends by month, with October being the lowest.

### Recommendations 

### Limitations



