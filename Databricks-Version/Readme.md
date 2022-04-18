# Databricks_Framework
This framework is created for the ETL implementation. It extracts data from csv, EXCEL, JSON, table then transform using pyspark and load to PostgreSQL with loading strategies Append, Upsert, overwrite and Type 2. This is automated ETL framework can be useful for any ETL based project, we need to create .py job file for inputs which contains source details, Join details like sources, transformations and final column name in target tables and pass this input to the framework and load the target tables in the PostgreSQL.


This Folder deals with Databricks_templates & the input which we used to parameterized the templates we used for the project
