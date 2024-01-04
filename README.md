The idea of this project is to showcase the migration of data from a traditional relational database (RDBMS) to a distributed storage system Hadoop, known for managing historical and analytical data. Its goal is to highlight the feasibility of such migration and the contribution of each technology in various project tasks.

# Edtech Data Migration Architecture
![edtech1](https://github.com/riti215/EdtechDataMigration/assets/57587827/0b52dccd-de9c-4f4a-8ba8-fb759031f7b1)

Starting with Talend Studio, the process extracts source data from a CSV folder, performs data mapping and lookups between fact and dimension tables. Next, the data is formatted, and the schema for the PostgreSQL database is defined. 
![talend_edtech](https://github.com/riti215/EdtechDataMigration/assets/57587827/d903d711-8651-430a-b7ce-9fe2e27ec35e)

PostgreSQL is then loaded with this data that undergoes data modeling and execution of some DDL/DML commands to establish its relational structure. 
![psql_edtech](https://github.com/riti215/EdtechDataMigration/assets/57587827/e6957ea7-6c78-413c-9c8a-9186860d3d65)

# Data Model
![edtech data modelling](https://github.com/riti215/EdtechDataMigration/assets/57587827/c3bb8d9d-03a4-48e7-bf87-f8b659cb26e6)

Another ETL process takes place using Apache PySpark which process the relational data, including tasks like parsing JSON strings and consolidating information into a single table. The transformed data is efficiently stored in Hadoop Distributed File System (HDFS) as Parquet format. Hive retrieves data from HDFS, allowing querying and analyzing the data and completes the journey of transforming raw EdTech Company data into a refined, accessible format that provide valuable insights through analysis.

Source Code : https://github.com/riti215/EdtechDataMigration/blob/440237963d046f5964ba87bccb8c04a8896e8c84/EdtechDataProcessing.ipynb

# Technology used
1. Programming Language - Python, SQL
2. File format - CSV, JSON, Parquet
3. ETL tool - Talend Studio
4. RDBMS - PostgreSQL
5. Data processing - Apache Pyspark
6. Distributed File Storage - HDFS
7. Hive for Analysis
