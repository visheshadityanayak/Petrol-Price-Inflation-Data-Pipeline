**Petrol Price Inflation Data Pipeline**



An end-to-end data pipeline project that tracks petrol price trends across major Indian cities, calculates yearly averages and inflation, and visualizes them in Power BI — built using Snowflake, Matillion, and Power BI.



📊 Project Overview



This project demonstrates a real-world data engineering pipeline that:



Extracts and stores petrol price data.



Transforms raw data into yearly averages using Matillion.



Calculates year-over-year (YoY) inflation rates.



Visualizes the inflation trends interactively in Power BI.



🧩 Tech Stack



Data Source: CSV (Petrol prices across Indian cities)



Data Warehouse: Snowflake



ETL Tool: Matillion (Transformation Pipelines)



Visualization: Power BI



Languages: SQL



🏗️ Architecture

CSV (Petrol Prices)

&nbsp;  ↓

Snowflake (RAW)

&nbsp;  ↓

Matillion (Transform 1: Yearly Averages)

&nbsp;  ↓

Snowflake (Analytics - PETROL\_YR\_AVG)

&nbsp;  ↓

Matillion (Transform 2: YoY Inflation)

&nbsp;  ↓

Snowflake (Analytics - PETROL\_YR\_INFLATION)

&nbsp;  ↓

Power BI (Visualization)



🗂️ Datasets

File	Description	Time Range

petrol.csv	Daily petrol prices for 5 major Indian cities (Mumbai, Delhi, Chennai, Hyderabad, Bengaluru)	2002–2020

⚙️ Steps

1\. Load Data



Upload petrol.csv into Snowflake RAW schema.



2\. Transformation – Yearly Averages



Created Matillion transformation job to:



Clean and format dates.



Group by CITY and YEAR.



Aggregate average rates.



Output table: ANALYTICS.PETROL\_YR\_AVG.



3\. Transformation – YoY Inflation



Second Matillion job to:



Compare year-over-year average rates per city.



Calculate inflation percentage.



Output table: ANALYTICS.PETROL\_YR\_INFLATION.



4\. Visualization



Connected Power BI to Snowflake.



Created charts showing:



Yearly petrol prices per city.



YoY inflation trends.



Comparative analysis across cities.





📈 Power BI Dashboard Highlights



Line chart for petrol price trends (2002–2020)



Bar chart comparing YoY inflation by city



Filters for city and time range





📸 Screenshots



Include the following:



Matillion Transformation 1 (Yearly Avg)



Matillion Transformation 2 (YoY Inflation)



Snowflake table preview (PETROL\_YR\_AVG and PETROL\_YR\_INFLATION)



Power BI dashboard visualization



Full pipeline flow diagram (hand-drawn 2D blueprint)



🧠 Learnings



End-to-end data flow from raw CSV to dashboard.



Hands-on with Snowflake schema design and SQL transformations.



Matillion ETL orchestration for real-world pipelines.



Power BI integration with Snowflake.

