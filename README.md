# Snowflake_ETL_SQL_Project
ETL Workflow explaining medallion architecture in Snowflake 

Project Overview:

this project gives an overview on the below following :
	How to make Snow Pipe, Stream and tasks work together 
	How to integrate stream and task 
	How fast data moves from bronze layer to gold layer in a medallion architecture

We have used five datasets customers, restaurants, items, food and orders containing more than 100.00K data. Since Snowflake is a  cloud data warehouse the data from source system should be extracted and placed in an internal stage.Once data is available in internal stage we will ingest data to a snowflake cloud data warehouse. All the data including the history data and incremental data are loaded via stages, pipes and tasks and data is uploaded to the gold layer for analytical purpose.


Step-up Instructions:

Part 01:
> Create 5 schemas (5 logically layers or zones)
> Create Tables (DDL) under Bronze zone schema
> Initial Data Load Via WebUI/ create file formats and stages
> Load the data into the stage.
> create pipes under the bronze layer and auto_resume it for the data to load from stage
> Verify the tables and data.

Part 02:
> Create Tables (DDL) under the Silver Zone Schema
> Load data from the bronze layer via tasks
> Also create streams to capture the change
> verify the tables and data in silver zone.

Part 03:
> Create tables(ddl) under gold zone schema
> Load the data from silver zone to gold zone as insert statements
> also create tasks in this zone to upload CDC data from the silver zone



