# Snapnet_Data-Engineer


This Python script performs an ETL (Extract, Transform, Load) process using pandas and SQLAlchemy to interact with a PostgreSQL database:

Extraction: It reads three CSV files (menu_items.csv, order_item.csv, and orders.csv) into pandas DataFrames.

Database Connection: Establishes a connection to a local PostgreSQL database using SQLAlchemy.

Schema & Table Setup:

Creates a staging schema if it doesn't exist.

Drops and creates three staging tables (raw_menu_item, raw_order_item, raw_orders) with specified columns to hold raw data.

Data Loading: Loads the data from the pandas DataFrames into the respective PostgreSQL staging tables using to_sql.

Transformation:

Joins the three staging tables on related keys to produce a comprehensive transformed_table with enriched order details.

Drops the table first if it exists, then creates it using a SELECT SQL statement.
