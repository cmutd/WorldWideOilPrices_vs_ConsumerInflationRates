# ETL Project REPORT



## WORLDWIDE Oil Prices Vs Consumer Inflation Rates



## 1. Objective

Create a database of Worldwide country oil and gas volumes and prices data with the inflation rates for the year 2000. 



### 2.  EXTRACT - Data Source for ETL project

>2 CSV files were downloaded from Kaggle
>
>File 1 - inflation_consumer_prices.csv - Contains worldwide consumer inflation data for countries from 1960 - 2017
>
>File 2 - Oil and Gas 1932-2014.csv - Contains world wide oil and gas production volumes and prices from 1932 - 2014



### 3. **TRANSFORM - Data Cleanup and Analysis**

>In Jupyter Notebook the following was performed
>
>* Put each CSV into a pandas DataFrame
>
>* The files were filtered to show only data for the year 2000.
>
>* Copy Only the columns needed into a new dataFrame from the 2 data files
>  * For file 1 - Inflation Data - columns - "Country Name", County Code", "2000: Inflation",	
>  * For file 2 - Oil and Gas-"cty_name","id","year","oil_price_2000","oil_value_2000","gas_price_2000","population
>
>* Rename as required to cleanup data set
>
>* Perform transformation on the "oil gas price" dataframe and group on country id to get data rolled up to country level since the inflation data file information is given at country level. 
>
>* Drop the null data from the inflation data file
>
>* Use aggregation averages to get the right values for oil price, gas price, oil volumes and population columns from the "oil and gas Data"



### 4.  LOAD Data into Database

>1. The Extracted data is in rows and columns so it will be loaded into the Postgress relational database
>
>2. Create 2 tables in Postgress Database to hold the 2 data sets
>
>*  Country Oil and Gas Volumes and Prices data
>
>* Country inflation data
>
>3. Create a connection to database.
>
>4. Check for a successful connection to the Postgres database and confirm that the tables have been created.
>
>5. Append DataFrames to tables. Use indexes as required.
>
>6. Confirm successful **Load** by querying database.
>
>7. Join the two tables and select the data to review and perform further analysis

