# Databricks_1
Reading the data with different available schema options 


Option 1: inferSchema() <br>
  By setting the inferSchema() option to True, spark automatically reads a few data records, assigns the best data type to each column, and defines a schema. <br>
Option 2: DDL Schema <br>
  It is a manual process of assigning schema to the data, which follows the below format:<br>
  my_ddl_schema = '''<br>
              col_name1 data_type,<br>
              col_name2 data_type,<br>
              col_name3 data_type<br>
              '''<br>
Option 3: StructType()<br>
  It is a manual process of assigning schema to the data, which follows the below format:<br>
  my_structtype_schema = StructType([<br>
                                    StructField(colname1,stringtype(),True),<br>
                                    StructField(colname2,stringtype(),True),<br>
                                     StructField(colname3,stringtype(),True)<br>
                                    ])<br>
                                    
As spark follows lazy evaluation, it performs reading only when trigger commands such as display(), show(), etc., are used.<br>
