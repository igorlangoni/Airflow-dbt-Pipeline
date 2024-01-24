## Airflow-BigQuery-dbt Pipeline

 An end-to-end pipeline that ingests raw data from CSV files through Apache Airflow DAGs (from a Docker Container) into a Google BigQuery analytical database. From there, it uses dbt to, firstly, normalize and clean the data and afterwards to make the necessary transformations and come up with relevant reports. At each step, quality checks are run using Soda, to ensure no data is corrupted, missing or duplicated. Finally, the reports are displayed in a dashboard so stakeholders are able to visualize the data and make informed data-driven decisions.

In order to make the most out of Apache Airflow and to maximize efficiency, I have also used Astro CLI. Furthermore, as a means to integrate dbt and Airflow whilst gaining better visibility within my DAG I've utilized the Cosmos sdk.

This project was based on <a href="https://www.youtube.com/watch?v=DzxtCxi4YaA&ab_channel=DatawithMarc">Data Engineer Project</a> by <a href="https://www.youtube.com/@MarcLamberti">Marc Lamberti</a>. 


### The Dataset

https://www.kaggle.com/datasets/tunguz/online-retail

**Source:**
Dr Daqing Chen, Director: Public Analytics group. chend '@' lsbu.ac.uk, School of Engineering, London South Bank University, London SE1 0AA, UK.

**Data Set Information:**
This is a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

### Data Modeling

<img width="718" alt="data_modeling" src="https://github.com/igorlangoni/Airflow-dbt-Pipeline/assets/123383171/d418d417-ae0b-44a2-906c-ca468f91ec46">

### The Pipeline

<img width="1509" alt="pipeline_" src="https://github.com/igorlangoni/Airflow-dbt-Pipeline/assets/123383171/e5c959b7-57c7-4406-953f-a00015e6f80b">

### Dashboard

<img width="1440" alt="retail_dashboard" src="https://github.com/igorlangoni/Airflow-dbt-Pipeline/assets/123383171/313f4d77-87a6-43cb-b914-f7d8dbf52039">



