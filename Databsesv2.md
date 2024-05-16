 # RDS summary :  
 - Managed databases for PostgresSQL / MySQL / Oracle / SQL server / Maria DB / Custom
 - Provisioned RDS instance size and EBS volumes and types
 - Auto scaling capability for storage
 - support for read replicas in multi az
 - security through IAM, Security Groups , KMS , SSL transit
 - Automated back up for 1 to 35 days with point in time restore feature
 - Manual snap short for long term recovery
 - Managed and scheduled maintenance
 - support for IAM authentication
 - RDS custom for access to and customize
 - Use cases : store relational databases and perform sql queries , transactions

# Aurora  Summary 
- compitable API for prostgresSQL / MysSQL separation of storage and compute
- storage : data is stored in 6 replicas across 3AZ - high available , self heaing, auto scagling
- compute: cluster of db instances across multiple az , auto scaling of read replicas
- cluster : custom end point for writer and reader DB instances
- same security / monitoring / maintenance features as RDS
- aurora serverless
- Aurora Global : up to 16 DB instances in each region , less then 1 sec to storage replication
- Aurora machine learning perform ML using SageMaker & comprehend on Aurora
- Use case : same as RDS but less maintenance / more flexibility / more performance/ more fetaures

# Amazon Elasticache 
- managed Redis/ memcached
- in memory data store , sub mili second latency
- select elasticache instances type
- support for clustering (redis) and multi az , read replicas ( sharding)
- security through IAM , security groups , kms, redis auth
- backup/snapshot . point in time restore
- managed and scheduled maintenance
- requires some application code change
- use cases : key value store, frequent reads, less writes, cache result for db quiries , store session data for websites, can not use SQL

mongoDB = documentDB
grpahed databases = neptune

# Neptune
fully managed graphed databases
a popular dataset would be a social network 
highly available across 3 az with 15 read replicas
Highly available with replicas across multiple az
great for knowledge graphs (wikipedia) fraud detection, recommendation engines, social networking



apache cassandra = amazon keyspaces
uses cql ,iot 


# Amazon QLDB
stands for Quantam ledger Database
a ledger is a book recording financial transactions
immutable system : no entry can be removed or modified cryptographically verifiable
2-3x better performance than common ledger blockchain
there is no de-centralization component 

