# Amazon athena 
- serverless query service to analyze data that stored in s3
- uses sql to analyze data
- pricing $5 per tera byte of data scanned
- commonly used for amazon quicksight for reporting dashboards
- usecases:  business intelligence , analytics , reporting query vpc flow logs elb logs cloud trail
- analyze data with sql serverless = athena
- recommended format for athena is orc or parquet for better performance (columnar data )

# Redshift
- Redshift is based on PostgresSQL but it is not used for oltp
- its OLAP - online analytical processing
- it gives 10x better performance than other data wirehousing
- columnar storage of data
- pay as you go based on the instead of row based & parallel query engine
- has a SQL interface for performing the sql quiries
- Business intelligence tools such as amazon quicksight or tableu intergate with it
- vs athena: faster quiries joins and aggregate functions, when complex task comes into the play we should use redshift , and for ad hoc quiries athena is enough
  
# Amazon EMR
- EMR stands for "Elastic MapReduce"
- EMR helps to Hadoop Clusters to analyze and process vast amount of data
- the clusters can be made of 100 of ec2 instances
- comes bundeled with Apache spark , Hbase, Presto, Flink
- EMR takes care of all provisioning and configuration
- auto scaling and integrated with Spot instances
- Use cases: data processing , machine learning , web indexing , anything related to big data
- There are three kinds of nodes in EMR , master node(long run), core node(long run), task node(spot run).

## Others
amazon glu = ETL service ( extract transform, load)
Aws lake formation = is a central place to have all your data for analytics purposes
kinesis data analytics - can read data from kinesis data firehose and kinesis data streams. two types of processing 1. sql application 2. kinesis data analytics for apache flink  
Output sink can have kinesis data stream and kinesis data firehose
