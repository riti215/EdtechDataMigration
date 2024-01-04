The idea of this project is to showcase the migration of data from a traditional relational database (RDBMS) to a distributed storage system Hadoop, known for managing historical and analytical data. Its goal is to highlight the feasibility of such migration and the contribution of each technology in various project tasks.

# Edtech Data Migration Architecture
![edtech1](https://github.com/riti215/EdtechDataMigration/assets/57587827/b7af7ed1-6d8e-49af-845c-1115e2538a2c)

Starting with Talend Studio, the process extracts source data from a CSV folder, performs data mapping and lookups between fact and dimension tables. Next, the data is formatted, and the schema for the PostgreSQL database is defined. 
![talend_edtech](https://github.com/riti215/EdtechDataMigration/assets/57587827/9c424c3a-cdaf-4aaa-98d1-470f8ae475c3)

PostgreSQL is then loaded with this data that undergoes data modeling and execution of some DDL/DML commands to establish its relational structure. 

![psql_edtech](https://github.com/riti215/EdtechDataMigration/assets/57587827/1ee61b87-3137-4b24-b9b6-ecb17c0e2ab6)

# Data Model
![edtech data modelling](https://github.com/riti215/EdtechDataMigration/assets/57587827/da282427-fe49-460d-ae9c-2e678b13e3ca)

Another ETL process takes place using Apache PySpark which process the relational data, including tasks like parsing JSON strings and consolidating information into a single table. The transformed data is efficiently stored in Hadoop Distributed File System (HDFS) as Parquet format. Hive retrieves data from HDFS, allowing querying and analyzing the data and completes the journey of transforming raw EdTech Company data into a refined, accessible format that provide valuable insights through analysis.

https://github.com/riti215/EdtechDataMigration/blob/1f59cd372f9004d85acb54480e1ed1c19536f5d8/EdtechDataProcessing.ipynb

# Technology used
1. Programming Language - Python, SQL
2. File format - CSV, JSON, Parquet
3. ETL tool - Talend Studio
4. RDBMS - PostgreSQL
5. Data processing - Apache Pyspark
6. Distributed File Storage - HDFS
7. Hive for Analysis
