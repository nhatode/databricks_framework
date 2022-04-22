###### This folder contain following five files:
  * Functions_notebook
  * Stage_notebook
  * Transform_notebook
  * Join_Notebook
  * Join_reports_calculation_notebook

###### Functions_notebook --
    This notebook deals with all the user define function.
    The following are some examples of user-defined functions/transformations created in this framework:
    - Replace Invalid charater(s) like "space, ;,{},(),\n,\t" with "_"
    - Convert DataTypes into String, Integer, Long, Timestamp, dateformate etc.
    - readcsv based on the input qoute character and escap character
    - add partition, get partition.
    - set default values if input json does not have it.
    - date_func (this will create partition based on the date parameter inputed)

###### Stage_notebook --
   
    - Extracting data from different formats:
       csv, Excel, json and text files from ADLS. 
    - Data Cleaning: remove unwanted character.
    - Data type conversion: Create tables in a stage container with the required schema and then convert the datatypes of all columns, loading data into stage tables with the required structure.
    - Adding the partitions when loading data to the stage tables.

###### flow diagram of Stage_delta --    
![dataflow](https://github.com/nhatode/databricks_framework/blob/main/images/Stage_Template.jpeg "dataflow")

  


###### transform_notebook --
    This Transform notebook deals to load the final table with following loadstrategies: 
    
    - Read data from stage tables. 
    - Then apply transformations on the data as per given SQL query in input json. 
    - Load the transformed data as per load strategies apend only, update, overwrite, upsert and type 2.
	     For load we used Business key which combination of columns which we will use for identify new inserts, updated records. 
    - Then data will loaded to adls and csv, xml, sql server table formats.
    
###### Join_notebook --
    This notebook work on joining tables from transform layer and load into transform/cureted layer.
    
    - Once data loaded to transform container and we need further processing then join notebook can be used. 
    - Multiple sources of data like sql server table, sql query based on transform table and stage table can be joined and select required column's data and then load to the data mart container. 
    - once joined data is generated this notebook reuses transform notebook to load data to datamart container
    

###### Join_reports_calculation_notebook --
    This notebook specificly created to load data for reporting tables from transformed layered.
    
    - There were various reports getting generated which have calculations and formulas.
    - For this you can simply pass csv format data with formulas mentioned in one column and any other transformations.
    - This notebook were automatically generates the reports usning csv file given.
    - Again reuses transform notebook for loading final output to datamart.


