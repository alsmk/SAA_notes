# RDS 
RDS stands for Relational Database service, it allows you to create databases in the cloud that are managed by AWS
- Postgres
- MySql
- MariaDB
- Oracle
- Microsoft SQL server
- Aurora
RDS - storage Auto scaling
Helps you to increase storage on your RDS DB instance dynamically
We should avoid manually scaling your database storage
Automatically modify storage happens if:
- Free storage is less than 10% of allocated storage
- low storage lasts at least for 5 min
- 6 hours have passed since last modifications
this is very useful with unpredictable workloads

# read replicas
we can create up to 15 replicas(they can be within same az, cross az or cross region)
replication is async, so reads are eventually consistent
in same region read replicas has no charge
in cross region it has some costs

#RDS multi AZ 
uses for disaster recovery
in some one az it has the master DB, and in another there is RDS stand by instance(which is sync replication of master DB, every changes in master DB synchronusly make changes in stand by RDS)
not manual intervention in apps
not used for scaling
The read replicas can be set up as MULTI AZ for disaster Recovery

RDS custom is only available for mysql and oracle

# Amazon Aurora
Aurora gives 5x better perfomance for MySql and 3x better perfomance for Postgres(vs RDS)
Aurora storage automatically grows (10 gb to 128 tb)
Aurora can have  15 replicas ( It latency is much less than rds 10 ms)
Aurora is like multi az RDS
It has 6 copies of your data across 3 AZ
The master DB has only the write permission 
If the master fails the failover time is just 30 s
instance configuration can be of three types serverless, burstable classes (t) , memory optimized classes (r)
Aurora capacity units - acu 
A aurora datbase has 2 endpoints 
- reader endpoint
- writer endpoint
promoting another region (for disaster recovery ) has an RTO of <1 min
Typical cross region replication takes less than 1 second
Aurora supported macine learning services
- sage maker
- amazon comprehend


# RDS back up
Automated backups:
Daily full backup of the databases
transaction logs are backed up by RDS every 5 min 
ability to restore to any point in time (from oldest time to 5 min ago)
retention time is 1 to 35 days (set 0 to disable automated backup)
Manual DB snapshot
- manually trigged by user
- Retention of backup for as long as you want

For restoring S3 works as mediator 
Aurora Database Cloning is very cost effective and fast
Useful to create a staging databases from a productiion database without impacting the prodcution database

## RDS security
 At rest encryption 
 - Database master and replicas encryption using AWS KMS
 - if the master is not encrypted replicas can not be encrypted
 - to encrypt an unencrypt we must have to take a snapshot of this rds and restore as encrypted
in flight encryption : TLS
IAM authentication
Security groups
No SSH available
Audit logs can be enabled and sent it to cloud watch for longer retention

# Elasticache 

![image](https://github.com/alsmk/SAA_notes/assets/43688097/6c9ce965-0177-4f06-bf4e-c6d697620d69)


