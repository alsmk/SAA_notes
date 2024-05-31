RPO - how much data loss are you willing to accept in case of a disaster happens
between the disaster and RTO is the amount of downtime your appication has
Disaster Recivery strategies
- Back up and Restore
- pilot light
- warm stand by
- hot site / multisite approach


pilot light , warm stand by and hot site costs more money but faster rto
back up and restore is a high rpo and high rto but its cheaper
pilot light is lower rpo and lower rto  it costs more
warm stand by uses auto scaling and load balancer ELB , which helps to decrease rpo and rto
hot site / multi site approach is very fast . Back up data within miniutes or second
but also it is very expensive , it uses in multi DC environment
here we can use multi region

Some disaster recovery tips: 
- back up : EBS snapshot , RDS snapshot ,s3 glacier life cycle policy, snowball and storage gateway
- high availability : use route 53 to migrate DNS over from region to region, rds multi az ,efs, s3, elasticache
- replication: RDS replication cross region , aws aurora + global databases
- automation: cloudformation/elastic beanstalk to re create a whole new environment
- aws lambda functions for automation

  
Database Migration Service:
Quickly and securely migrate databases to aws, resilient , self healing
the source database remains available during the migration
for heterogenous migration we need sct (sheema converision tool)
migration options:
option 1 : DB snapshots from  RDS restored as aurora DB
option 2: Create an aurora read replica from your RDS and when replicaion lag is zero promote it as its own DB CLuster
option 3 : if its in external of RDS , then create a back up and use the aurora extension

On premise strategy with AWS
vm import and export
aws application discovery
AWS database migration service dms
aws server migration service sms

# application  discovery service
plan migration projects by gathering information about on-premises data centers
when we need to migrate data from on premise to aws 
there are two types of migration 
1. agentless discovery : vm inventory , configuration , and performance history such as CPU ,memory and disk usage
2. Agen based discovery : system configuration , system performance , running processes and details of the connections between systems
   
resulting data can be viwed within aws migration hub
