# Databricks_Framework
For the implementation of ETL, this framework was created. The code extracts data from CSV, EXCEL, JSON, and a SQL table. It then transforms it using PySpark and loads it to MicroSoft SQL Server using Append, Upsert, Overwrite, and Type 2 loading strategies. This automated ETL framework can be used for any ETL project. For the inputs we must create .py job files that contain source details, join details like sources, transformations, and the final column names in the target tables; this is the input we pass to the framework which loads the target tables in Microsoft SQL Server.

# Repo Stucture 

This repo contain two folder, each deals with specific work.
| Folder | Purpose |
|--------|---------|
| [Databricks Templates](https://github.com/nhatode/databricks_framework/tree/main/Databricks-Version/Databricks%20Templates) | This folder hold all the templates related to the project |
| [JobInputs](https://github.com/nhatode/databricks_framework/tree/main/Databricks-Version/JobInputs) | This folder holds all the input files |
