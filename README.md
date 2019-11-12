# Architecture

<img width="1161" alt="c-architecture" src="https://user-images.githubusercontent.com/19339748/68663826-ef3d4700-0504-11ea-8ae7-d768d82688ed.png">

# Description
This repo contains a CloudFormation script that provisions deployment resources in Amazon Private Cloud. Within the VPC, there are two availability zones with public and private subnets. To ensure better fault tolerance and availability, it leverages a Load Balancer and an Autoscaling Group to spin up a minimum of two servers in the private subnet in each availability zone.

Access to resources are controlled through Security Groups, NAT Gateways, and Route Tables. Servers have unstricted access to the internet, but go through the NAT Gateways. Servers are also given IAM role to download resources stored in the restricted S3 bucket.
