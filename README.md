# Life cycle of Framework

1. ### What is Framework?
  * Frameworks are platforms used to develop applications. It provides software developers with a structure to build programs that run on a specific platform. 
  * In a framework, for instance, input can be processed, hardware devices can be managed, and system software can be interacted with.
  * In addition to libraries and compilers, a framework could also contain various other programs that are typically needed in software development.
  
2. ### Why do we need?
  * Working on new applications can sometimes be complex. Over time, libraries will no longer suffice. What is needed is structure, and order in the chaos of code. 
  * That is where Frameworks come into play. 
  * Below frameworks deals with, taking input from the users in JSON file formate with pre-defined key & values and then load the data into respective layers with transformation.  
3. ### Testing the framework?
  * The purpose of a testing framework is to provide guidelines or rules for creating and designing test cases. A framework consists of practices and tools that QA professionals can use to test more effectively.
4. ### Common Transformation used? 
  * The following are some examples of user-defined transformations created with this framework:
    - Replace Invalid charater(s) like "space, ;,{},(),\n,\t" with "_"
    - Convert DataTypes into String, Integer, Long, Timestamp, dateformate etc.
    - readcsv based on the input qoute character and escap character
    - add partition, get partition.


# Databricks_Framework

##### Basic Architecture diagram

![Sample Architecture](images/Architecture_diagram.jpg "Basic Architecture Diagram")


______

Lets deep dive in the architecture :

ETL (Extract-Transform-Load) is the process of extracting, transforming, and loading data. Using Azure Data Factory pipelines in the Ingestion layer and Extract layer, we are extracting flat files from a variety of sources and adding them to a raw layer on Azure Data Lakes (ADLS). Once the data is available in the raw layer using ADF we are calling our databricks framework and perform some of the transformation on the raw data. Transformations are done on the basis of input provided to the framework.
