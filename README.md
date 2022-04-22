# Life cycle of Framework

1. #### What is Framework?
  * Frameworks are platforms used to develop applications. It provides software developers with a structure to build programs that run on a specific platform. 
  * In a framework, for instance, input can be processed, hardware devices can be managed, and system software can be interacted with.
  * In addition to libraries and compilers, a framework could also contain various other programs that are typically needed in software development.
  
2. #### Why do we need?
  * Working on new applications can sometimes be complex. Over time, libraries will no longer suffice. What is needed is structure, and order in the chaos of code. 
  * That is where Frameworks come into play. 
  * Below frameworks deals with, The company Ingredion is a food producer with many plants across the country. It needs to process data for around 40 plants. 
    For one or two plants, we will automate the process, whereas the rest will be developed using a low-code strategy. We have a team that is not trained in Spark or       DataBricks. To meet customer deadlines, we need a mechanism that automates the ETL processing, reduces maintenance costs, and saves our customers money. 
    Delta tables are used because they provide ACID transactions and isolation level to Spark, since they are parquet-based, columnar formats with transaction logs. 

    Developers will create a single JSON input for each job, which will be used for all notebooks.
    Eg. container names, stage table name, load strategies insert, update and upsert etc. 
 
3. #### Testing the framework?
  * The purpose of a testing framework is to provide guidelines or rules for creating and designing test cases. A framework consists of practices and tools that QA professionals can use to test more effectively.
4. #### Common Transformation used? 
  * The following are some examples of user-defined transformations created with this framework:
    - Replace Invalid charater(s) like "space, ;,{},(),\n,\t" with "_"
    - Convert DataTypes into String, Integer, Long, Timestamp, dateformate etc.
    - readcsv based on the input qoute character and escap character
    - add partition, get partition.
5. #### Data Validation and quality checks?
  * Validating data means ensuring that it is accurate and of high quality before using, importing, or otherwise processing it. 
  * There are different types of validations depending on the destination or objective. 
    
6. #### Continues Intgration/ Continues Deployment
  * will be comming soon.

# Databricks_Framework

##### Basic Architecture diagram

![Sample Architecture](images/Architecture_diagram.jpg "Basic Architecture Diagram")


______

#### Lets deep dive in the architecture :

ETL (Extract-Transform-Load) is the process of extracting, transforming, and loading data. Using Azure Data Factory pipelines in the Ingestion layer and Extract layer, we are extracting flat files from a variety of sources and adding them to a raw layer on Azure Data Lakes (ADLS). Once the data is available in the raw layer using ADF we are calling our databricks framework and perform some of the transformation on the raw data. Transformations are done on the basis of input provided to the framework.


[Click here](https://github.com/nhatode/databricks_framework/tree/main/Databricks-Version)
