# airflow_dbt_pipeline
 An end-to-end pipeline that ingests raw data from CSV files through Apache Airflow DAGS into Google BigQuery. From there, it uses dbt to, firstly, normalize and clean the data and afterwards to make the necessary transformations and come up with relevan reports. At each step, quality checks are run using Soda, to ensure no data is corrupted, missing or duplicated. 
