<h1>Online Retail (Data Pipeline/Dashboard)</h1> 

#### - Python, SQL, Docker, DBT, Apache Airflow, BigQuery, Git
<br>

This challenging and exciting personal project analysed online retail data from a non-registered UK-based company, by means of an ELT pipeline that ingested and loaded raw data from a CSV file into a BigQuery warehouse before transforming it and loading into a dashboard.

#### Extraction and Load

After the dataset was downloaded from Kaggle, my first  Apache Airflow DAG task was to transfer the file from my local machine to a Google Cloud Bucket. From there, a second task created a BigQuery dataset and a third task loaded the file from the bucket into the dataset, creating the raw_invoices table.

The extraction and load phases were technically complete, but in order to guarantee the quality of the data I implemented Soda checks to ensure all the columns were present and that datatypes were kept as they were supposed to be. 

#### Transform

All the transformations were made by using SQL queries in DBT and the Cosmos SDK. It was useful in the sense that it gave visibility to the tasks when looking at them in the Airflow DAG interface. 

The first step was to transform the data in the analytical db and come up with dimension and fact tables. Those would later be used to make reports. Through the use of complex SQL queries the customer, product, datetime and invoices tables were created.

Again, after the previous step was finished, I implemented checks to ensure the results were not corrupted or missing any information.

The second transformation step was to create reports, those being a derivation of the models previously created. The reports I created answered question such as 'best-selling product by quantity sold', 'best-selling month by total revenue', and 'primary markets by total revenue'.

A final round of checks were run at this point to atest the quality of the reports. <br><br>




This project was based on <a href="https://www.youtube.com/watch?v=DzxtCxi4YaA&ab_channel=DatawithMarc">Data Engineer Project</a> by <a href="https://www.youtube.com/@MarcLamberti">Marc Lamberti</a>!!


## The Dataset

https://www.kaggle.com/datasets/tunguz/online-retail

**Source:**
Dr Daqing Chen, Director: Public Analytics group. chend '@' lsbu.ac.uk, School of Engineering, London South Bank University, London SE1 0AA, UK.

**Data Set Information:**
This is a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

## Data Modeling

The data modeling resulted in three dimension tables (customers, products and datetime) and one fact table (invoices).

<img width="718" alt="data_modeling" src="https://github.com/igorlangoni/Airflow-dbt-Pipeline/assets/123383171/d418d417-ae0b-44a2-906c-ca468f91ec46">

## The Pipeline


<img width="1509" alt="pipeline_" src="https://github.com/igorlangoni/Airflow-dbt-Pipeline/assets/123383171/e5c959b7-57c7-4406-953f-a00015e6f80b">

#### DAG

<img width="1440" alt="dag_success" src="https://github.com/igorlangoni/Airflow-dbt-Pipeline/assets/123383171/9159c9af-ffb3-4c01-8c66-83754ba7a110">

## Dashboard


<img width="1920" alt="online_retail_dash" src="https://github.com/igorlangoni/online_retail_data_pipeline/assets/123383171/6f8904ca-8548-4dc0-9a3e-b02c5903af37">


