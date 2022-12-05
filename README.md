# Data-warehouse---CO2-emission
## Data warehouse construction and Tableau reporting

### Step 1 : Looking for data
Data is taken from [Data Bank](https://data.worldbank.org/topic/19?end=2021&start=2000), see [dataset](https://github.com/thohoang87/Data-warehouse---CO2-emission/tree/main/dataset).
We chose many files: [CO2](https://github.com/thohoang87/Data-warehouse---CO2-emission/blob/909fd03f8f62e3d4839208e0aab250d601287e3c/dataset/CO2.xls), [GDP](https://github.com/thohoang87/Data-warehouse---CO2-emission/blob/main/dataset/GDP.xls), [Population](https://github.com/thohoang87/Data-warehouse---CO2-emission/blob/main/dataset/population.xls) and [Investment](https://github.com/thohoang87/Data-warehouse---CO2-emission/blob/main/dataset/investissementt.xls)

### Step 2 : Data Cleaning
We cleaned and transformed data by using python and excel.

After cleaning, we have 8 tables : CO2, population, investment, GDP, country, region, continent and year. So we created the primary key for each file, and we added foreign keys into CO2's table. 

Then we stocked all of them in [data warehouse-CO2 emission](https://github.com/thohoang87/Data-warehouse---CO2-emission/blob/main/dataset/data%20warehouse-CO2%20emission.xlsx).

Then we load data into Oracle for data warehouse construction.

### Step 3 : Data warehouse construction with Oracle
We connected all tables by connecting primary keys and foreign keys, then we constructed a Star schema data warehouse with Oracle.

<img width="900" alt="Capture d’écran 2022-11-30 à 18 37 23" src="https://user-images.githubusercontent.com/114235978/205741538-d1249239-39ff-4588-b31d-473d4f50e59a.png">

<img width="279" alt="Capture d’écran 2022-11-30 à 18 37 45" src="https://user-images.githubusercontent.com/114235978/205741565-a7ee82f9-ec20-430b-8f90-fce3572a5b0d.png">

We also prepared some SQL queries :

<img width="1168" alt="Capture d’écran 2022-11-30 à 18 25 43" src="https://user-images.githubusercontent.com/114235978/205742130-9e8fa183-3b93-4810-a27e-3cb9f6a2ec2f.png">


### Step 4 : Tableau reporting
After the data warehouse construction, we used Tableau for the reporting, see [here](https://github.com/thohoang87/Data-warehouse---CO2-emission/blob/main/polution%20CO2.twbx).

<img width="1359" alt="Capture d’écran 2022-12-05 à 22 00 49" src="https://user-images.githubusercontent.com/114235978/205741934-833ce4e3-f750-4d48-8a8d-e084b0c8ebba.png">

  - Map of the average of C02 and the population by year :
  
  <img width="1436" alt="Capture d’écran 2022-12-02 à 20 46 34" src="https://user-images.githubusercontent.com/114235978/205374188-ab06ec4e-4fef-4942-b75c-151d64500b24.png">

  - Line chart to explain the relationship between the average of CO2, GDP and the foreign direct investments by year : 
  
  <img width="1438" alt="Capture d’écran 2022-12-02 à 20 49 12" src="https://user-images.githubusercontent.com/114235978/205374761-bb57691e-1c17-44fc-a29f-b2ab9bcb2afe.png">

  - Line chart allows to see the average of CO2 by year and by country :
  
  <img width="1435" alt="Capture d’écran 2022-12-02 à 20 49 32" src="https://user-images.githubusercontent.com/114235978/205374897-7d543a22-aa14-467c-984d-67136efa8842.png">

  - Bar chart allows to see the relationship between the average of CO2 and GDP by region and by year :
  
  <img width="1438" alt="Capture d’écran 2022-12-02 à 20 49 52" src="https://user-images.githubusercontent.com/114235978/205375164-88264454-201a-4af8-b92e-5d391a25c7d4.png">

  - Bar chart allows to see the relationship between the average of CO2 and GDP by continent and by year :
  
  <img width="1440" alt="Capture d’écran 2022-12-02 à 20 50 07" src="https://user-images.githubusercontent.com/114235978/205375327-98dbddbf-d1e4-463f-a0b5-a7774559f634.png">

  - Buble chart allows to see the relationship between the average of CO2 and the foreign direct investments by year and by country :
  
  <img width="1435" alt="Capture d’écran 2022-12-02 à 20 50 25" src="https://user-images.githubusercontent.com/114235978/205375478-f13ead0a-2378-4162-aafb-f793e2c5a50a.png">

Finally, we obtain this dashboard :

<img width="1063" alt="Capture d’écran 2022-12-02 à 20 50 44" src="https://user-images.githubusercontent.com/114235978/205375698-3324b37d-065c-4cae-bd6f-73bd7c208d14.png">
