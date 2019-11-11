# CloudFormation

<img width="1161" alt="c-architecture" src="https://user-images.githubusercontent.com/19339748/68586770-015aaf00-044b-11ea-8b8f-ea1058bc6386.png">

This repo contains a cloudformation script that provisions deployment resources in the Amazon Private Cloud. Within the VPC, there are two availability zones with public and private subnets. To ensure better fault tolerance and availability, it leverages a load balancer and an autoscaling group to spin up a minimum of two servers in the private subnets in each availability zones.

Access to servers are controlled through Security Groups, NAT Gateways and Route Tables. Servers access to internet are unstricted. Servers also given IAM role to download resources stored in the restricted S3 bucket.
