# Infrastructure

## AWS Zones
Identify your zones here
us-east-2 and us-west-1

## Servers and Clusters

### Table 1.1 Summary
| Asset      | Purpose           | Size                                                                   | Qty                                                             | DR                                                                                                           |
|------------|-------------------|------------------------------------------------------------------------|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Asset name | Brief description | AWS size eg. t3.micro (if applicable, not all assets will have a size) | Number of nodes/replicas or just how many of a particular asset | Identify if this asset is deployed to DR, replicated, created in multiple locations or just stored elsewhere |
udacity-ami-image-ped, S3 bucket, us-east-1
udacity-terraform-image-ped, S3 bucket, us-east-1
udacity-tf-pedersen, S3 bucket, us-east-2
udacity-tf-pedersen-west, S3 bucket, us-west-1
Ubuntu-Web, t3.micro, EC2 Instance, us-east-2
unnamed, t3.medium, EC2 Instance, us-east-2
unnamed, 20 GiB Volume snapshot, us-east-2
unnamed,  8 GiB Volume snapshot, us-east-2
unnamed, Snapshot, 8 GiB, us-east-2
ec2_sg, security group, ec2_sg, us-east-2
udacity, security group, SG-eks-cluster, us-east-2
eks-cluster-sg-udacity, security group, eks-cluster-sg-udacity-, us-east-2
unnamed, security group, default, us-east-2
unnamed,, security group, default, us-east-2
udacity-project-us-east-2a, Elastic IP addresses, us-east-2
udacity, key pairs, us-east-2
LoadBalancer, , us-east-2
udacity-project-us-east-2a, Elastic IP addresses, us-east-2

### Descriptions
More detailed descriptions of each asset identified above.

## DR Plan
### Pre-Steps:
List steps you would perform to setup the infrastructure in the other region. It doesn't have to be super detailed, but high-level should suffice.

Basically you would start with using Terraform to automate the process.  Initially you would completely build your primary production environment within Terraform.  Once completed and happy with that you would make a duplication within a secondary region by copying the Terraform code and replacing the current region with a new region and availability zones.  You would then need to initialize and deploy Terraform again.  

## Steps:
You won't actually perform these steps, but write out what you would do to "fail-over" your application and database cluster to the other region. Think about all the pieces that were setup and how you would use those in the other region

Within AWS go to RDS databases and select region.  Click on the writer instance-1, click actions and select failover. 
Now do the same with instance-0.  Another option would be to delete both instances then the cluster.  You may do the same for the application.
