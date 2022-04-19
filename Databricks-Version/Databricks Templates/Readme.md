###### This folder contain following five files:
  * Functions_delta
  * Join_delta_loop
  * Join_delta_reports_calculation
  * stage_delta
  * transform_delta
###### Function Delta --
    This python file deals with all the user define function.
    
###### Join_delta_loop --
    This python file deals with all the user define function.

###### Join_delta_reports_calculation --


###### stage_delta --


###### transform_delta --
    When sqlrefresh is true then newly added 'sqlrefresh_query' parameter can refresh only 7 days prior data from SQL server. 
    Note: If sqlrefresh_query = "" or sqlrefresh_query is not provided in inputjson then entire SQL table will be refreshed into ADLS.
    When sqlrefresh is "True/False" save SQL table in temporary ADLS table.
    Overwrite: It will directly overwrite ADLS and SQL table data.
    Append: SQL refresh "False": Incoming data will append to ADLS and SQL table data.
    Append: SQL refresh "True": SQL data will merge into ADLS and then incoming data will merge into ADLS and SQL.
    Upsert: If sqlrefresh is "True" or "False" then SQL table data will be loaded into temp table.
		  Sqlrefresh: "False": incoming data will merge into ADLS and then merge into internal temp(sql refresh data) with name outputDB.outputTable+"_temp". 
    Temp table extract will load into data in SQL tables.
		  Sqlrefresh: "True": incoming data will merge into ADLS and then merge into temp(sql refresh data). Temp table extract will load into sql. 
    After this, Temp table extract will merge into ADLS table.
    
		  Temp table will be dropped once load completed.
    Then merge final sql table data into ADLS.
