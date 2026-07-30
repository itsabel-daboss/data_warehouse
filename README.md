# Local Data Warehouse Stack

This project is a local, containerized data engineering environment. 
It simulates cloud infrastructure to extract, load, and transform data.
Think of this project as an automated factory that takes raw materials, refines them, and stores them for use.

MinIO (The Loading Dock): This is your local version of an AWS S3 bucket. When you download raw data (like messy CSVs or JSON files), it lands here first. It's built for bulk, raw storage.

PostgreSQL (The Warehouse): This is your local relational database, acting like Amazon RDS or Redshift. Once data is structured, it gets moved here so you can write SQL queries against it.

dbt (The Refinery): This is the "data build tool." It takes the raw, messy data that has been loaded into PostgreSQL and transforms it into clean, analysis-ready tables.

n8n & Apache Airflow (The Managers): These tools schedule and automate the work. n8n is great for quickly pulling data from the internet (like APIs), and Airflow makes sure your heavy data pipelines run in the correct order every single day without you pressing a button.

Git (The Save Button): This tracks every change you make to your code so you can always undo mistakes or look back at your history.
