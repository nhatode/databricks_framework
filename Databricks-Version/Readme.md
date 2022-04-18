# Databricks_Framework
This framework is created for the ETL implementation. It extracts data from csv, EXCEL, JSON, table then transform using pyspark and load to MicroSoft SQL Server with loading strategies Append, Upsert, overwrite and Type 2. This is automated ETL framework can be useful for any ETL based project, we need to create .py job file for inputs which contains source details, Join details like sources, transformations and final column name in target tables and pass this input to the framework and load the target tables in the Microsoft SQL server.

# Repo Stucture 

This repo contain two folder, each deals with specific work.
| Folder | Purpose |
|--------|---------|
| [Databricks Templates](https://github.com/nhatode/databricks_framework/tree/main/Databricks-Version/Databricks%20Templates) | This folder hold all the templates related to the project |
| [JobInputs](https://github.com/nhatode/databricks_framework/tree/main/Databricks-Version/JobInputs) | This folder holds all the input files |
