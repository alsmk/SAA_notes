# CIDR
classless inter domain routing 
it is used to allocate ip addresses
you can have multiple vpc in an aws region ( soft limit 5 ) but you can increase it
max cidr per vpc is 5 , for each cidr
min size is /28 16 ip addresses
max size is /16  65536  ip addresses
one vpc can not overlap others
in every subnet 5 ip addresses are always reserved they are not in use
private subnet or public subnet -> vpc -> internet gateway -> routing table -> internet

to access a ec2 instance which is currently in private subnet into a vpc, we will use a bastion host, a bastion host holds a ec2 instance which is in  public subnet into the same vpc, 
after accessing the bastion host, we can access the ec2 instance through it
NACL are stateless and security groups are state ful
vpc peering is not transitive
after peering vpc, it has to be make sure that no subnets are overlapping. 
whenever you have to connect on premise to a vpc think about site to site connection
if this fails then think about direct connection or DX but this is way mmore costly
and it takes about one month to establish the network settings
vpc peering is not transitive to make it more useful and transitive we should use transit gateway
