## Airflow-BigQuery-dbt Pipeline

 An end-to-end pipeline that ingests raw data from CSV files through Apache Airflow DAGs (from a Docker Container) into a Google BigQuery analytical database. From there, it uses dbt to, firstly, normalize and clean the data and afterwards to make the necessary transformations and come up with relevant reports. At each step, quality checks are run using Soda, to ensure no data is corrupted, missing or duplicated. Finally, the reports are displayed in dashboard so stakeholders are able to visualize the data and make informed data-driven decisions.

 In order to make the most out of Apache Airflow and to maximize efficiency, I have also used Astro CLI. Furthermore, as a means to integrate dbt and Airflow whilst gaining better visibility within my DAG I've utilized the Cosmos sdk. 
