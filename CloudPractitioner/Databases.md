# AWS RDS
RDS stands for Relational Database Service
- It`s a managed DB service for DB use SQL as query language
- It`s allows you to create databases in cloud that are managed by AWS
  - Postgres
  - Mysql
  - MariaDB
  - Oracle
  - Microsoft SQL Server
  - Aurora


## Benefits
- Coninuous backups and retore to specific timestamp
- Minitoring dashboards
- Read replicas for improved read performace
- Multi AZ
- Maintenance windows for upgrades
- Scaling capability
- Storage backed by EBS

## Aurora
Aurora is a proprietary technology from AWS
- We can use PostgreSQL and MysQL
- Aurora is cloud optimized and claims 5x performance improvement over MySQL on RDS, over 3x the performance of Postges on RDS
- Aurora storage automatically grows in increments of 10 GB, up to 128 TB
- Aurora costs more than RDS (20% more)
- Not in the free tier


## Deployment Options
- Read replicas
  - This stretagy scale the read workload of your DB creating up to 15 read replicas
  - Data is only written to the main DB
- Multi-AZ
  - This stretagy gives you high availability in case of Failover
  - Replication cross AZ
  - Data is only read/written to the main database
- Multi Region
  - This stretagy allows you to replicate data across regions
  - The data can only be written to te main database (original)
  - We have a local performance better because the applications are reading in a local database


# Amazon ElastiCache
ElastiCache is to get managed Redis or Memcached
- Caches are in-memory databases with high performance, low latency
- Helps reduce load off databases for read instensive workloads

# DynamoDB
Fully managed highly available with replication across 3 AZ
- NoSQL database 
- Scales to massive workloads, distributed serverless database
- Millions of requests per seconds, trillios of row, 100s of TB of storage
- Fast and consistent in performance
- Low latency retrieval
- Low cost
- IAM integreted for security

## type of data
key/value database
- Composed by primary key (partition key and sort key) and attributes
- Schema is defined per item

## DynamoDB Accelerator - DAX
Fully managed in-memory cache for DynamoDB
- 10x performance improvement
- Secure, highly scalable & highly available

## DynamoDB Global tables
- make a dynamoDB table accessible with low latency in multiple-regions
- Active-Active replication (read/write to any AWS Regions)

# Redshift
Database is based on PostgreSQL 
- It`s OLAP - onlyne analytical processing
- Good for data wehousing and analytics
- Load data once every hour, not every second
- 10x better performance than other data warehouses
- Columnar storage of data
- Pay as you go based on the instances provisioned

# Amazon EMR
EMR stands for Elastic MapReduce
- EMR helps creating Hadoop clusters (Big data) to analyze and process vast amount of data
- The cluster can be of hundreds of EC2 instances
- EMR takes care of all the provisioning and configuration
- Auto-scaling 
- Use cases: data processing, machine learning, web indexing and big data

# Amazon Athena
Serverless query service to perform analytics against S3 objects
- Uses standard SQL language to query the files
- Suports CSV, JSON, ORC, Avro and Parquet
- Princing: $5 per TB of data scanned
- Use cases: Business Intelligence/analytics/ reporting, analyze and query VPC flow logs, ELB Logs, Cloud trails and etc...

# Amazon QuickSight 
Serverless machine learning-powered business intelligence services to create interactive dashboards
- Allows you to create dashboards
- Use cases:
  - Business analytics
  - Building visualizations
  - Perform ad-hoc analysis
  - Get business insights using data
- Integrated with RDS, Aurora, Athena, Redshift and S3

# DocumentDB
DocumentDB is the same of Aurora for MongoDB
- NoSQL database
- is used to store, query and index JSON data
- Fully managed
- Highly available with replication across 3 AZ
- Storage automatically grows 
- Automatically scales to workloads with millions of requests per second

# Amazon Neptune
Fully managed graph database

# Amaon QLDB
QLDB stands for Quantum Ledger Database
- A ledegr is a book recording financial transactions
- Fully managed
- Serverless
- High available
- Replication across 3 AZ
- Used to review history of all the changes made to your application data over time
- Immutable system

# Amazon managed Blockchain
Blockchain makes it possible to build applications where multiple parties can execute transactions without the need for a trusted or central authority.

- Used to join public blockchain networks
- Create your own scalable private network
- Compatible with the framwoks hyperledger Fabric & Etherium

# AWS Glue
Managed extract transform and load ETL service

# AWS DMS
DMS stands for Database Migration Service
- Help you to extract the data from a source database and insert in the target database
- Support Homogeneous migrations or Heterogeneous migrations: Oracle to Oracle or Microsoft SQL Server to Aurora

