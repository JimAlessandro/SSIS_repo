#SSIS ETL Proyect

#This project is configured so we can manage a production database (OLTP) connection to a DataWarehouse Database(DW)

# saving resource usage implementing isolation

# we get only the raw data from the OLTP (getting the columns and joining necessary tables to get a data set to transform)
# then we transform the dataset (applying aggregations, sorts, datatype convertions, local variables, parameters, etc)
# lastly we load the transformed data set into the DW destination (we inlcude idempotence and T-SQL or similar logic to manage bulk insert operations so we do not affect the existing data in the DW during and after the bulk insert)
