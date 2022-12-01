# Data-warehouse---CO2-emission
## Data warehouse construction and Tableau reporting

### Step 1 : Looking for data
Data is taken from [Data Bank](https://data.worldbank.org/topic/19?end=2021&start=2000), see [dataset](https://github.com/thohoang87/Data-warehouse---CO2-emission/tree/main/dataset).
We chose many files: [CO2](https://github.com/thohoang87/Data-warehouse---CO2-emission/blob/909fd03f8f62e3d4839208e0aab250d601287e3c/dataset/CO2.xls), [GDP](https://github.com/thohoang87/Data-warehouse---CO2-emission/blob/main/dataset/GDP.xls), [Population](https://github.com/thohoang87/Data-warehouse---CO2-emission/blob/main/dataset/population.xls) and [Investment](https://github.com/thohoang87/Data-warehouse---CO2-emission/blob/main/dataset/investissementt.xls)

### Step 2 : Data Cleaning
We cleaned, transformed data by python and excel.
After cleaning, we have 8 tables : CO2, population, investment, GDP, country, region, continent and year. So we created the primary key for each file. 
Then we stocked all of them in [data warehouse-CO2 emission](https://github.com/thohoang87/Data-warehouse---CO2-emission/blob/main/dataset/data%20warehouse-CO2%20emission.xlsx).
Then we load data into Oracle for data warehouse construction.

### Step 3 : Data warehouse construction with Oracle
We connected all tables by connecting primary keys and foreign keys, then we constructed a Star schema data warehouse with Oracle.

### Step 4 : Tableau reporting
After the data warehouse construction, we used Tableau for the reporting, see [here](https://github.com/thohoang87/Data-warehouse---CO2-emission/blob/main/polution%20CO2.twbx).
