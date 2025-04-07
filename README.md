# Databricks_1
Reading the data with different available schema options

Option 1: inferSchema()
  By setting the inferSchema() option to True, spark automatically reads a few data records, assigns the best data type to each column, and defines a schema.
Option 2: DDL Schema
  It is a manual process of assigning schema to the data, which follows the below format:
  my_ddl_schema = '''
              col_name1 data_type,
              col_name2 data_type,
              col_name3 data_type
              '''
Option 3: StructType()
  It is a manual process of assigning schema to the data, which follows the below format:
  my_structtype_schema = StructType([
                                    StructField(colname1,stringtype(),True),
                                    StructField(colname2,stringtype(),True),
                                     StructField(colname3,stringtype(),True)
                                    ])
                                    
As spark follows lazy evaluation, it performs reading only when trigger commands such as display(), show(), etc., are used.
