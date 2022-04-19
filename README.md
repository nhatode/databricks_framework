# Databricks_Framework

##### Basic Architecture diagram

![Sample Architecture](images/Architecture_diagram.jpg "Basic Architecture Diagram")


______

Lets deep dive in the architecture :

ETL (Extract-Transform-Load) is the process of extracting, transforming, and loading data. Using Azure Data Factory pipelines in the Ingestion layer and Extract layer, we are extracting flat files from a variety of sources and adding them to a raw layer on Azure Data Lakes (ADLS). Once the data is available in the raw layer using ADF we are calling our databricks framework and perform some of the transformation on the raw data. Transformations are done on the basis of input provided to the framework.
