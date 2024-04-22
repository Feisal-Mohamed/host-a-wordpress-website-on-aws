# WordPress Website Deployment on AWS

This repository contains resources and scripts for deploying a WordPress website on Amazon Web Services (AWS). The deployment architecture utilizes various AWS services for reliability, scalability, and security.

## Architecture Overview

1. **Virtual Private Cloud (VPC):** Configured with public and private subnets across two availability zones for high availability.
2. **Internet Gateway:** Facilitates connectivity between VPC instances and the wider Internet.
3. **Security Groups:** Act as network firewalls to control inbound and outbound traffic to the instances.
4. **Availability Zones:** Utilized for redundancy and fault tolerance.
5. **NAT Gateway:** Allows instances in private subnets to access the Internet while remaining private.
6. **EC2 Instance Connect Endpoint:** Enables secure connections to assets within both public and private subnets.
7. **Private Subnets:** Web servers (EC2 instances) are positioned here for enhanced security.
8. **Application Load Balancer (ALB):** Distributes web traffic evenly to EC2 instances across multiple Availability Zones.
9. **Auto Scaling Group:** Manages EC2 instances automatically for website availability, scalability, fault tolerance, and elasticity.
10. **GitHub:** Web files are stored here for version control and collaboration.
11. **Certificate Manager:** Secures application communications using SSL/TLS certificates.
12. **Simple Notification Service (SNS):** Sends alerts about activities within the Auto Scaling Group.
13. **Route 53:** Registers the domain name and sets up DNS records.
14. **Amazon EFS:** Used for a shared file system.
15. **Amazon RDS:** Used for the database.

## Deployment Steps

To deploy the WordPress website on AWS, follow these steps:

1. Clone this repository to your local machine.
2. Review the scripts and configuration files provided in the repository.
3. Ensure you have an AWS account and necessary permissions to create resources.
4. Configure a VPC with public and private subnets across multiple availability zones.
5. Deploy an Internet Gateway and configure route tables to enable Internet access.
6. Create Security Groups to control traffic to your instances.
7. Configure NAT Gateway for instances in private subnets to access the Internet.
8. Set up EC2 instances in private subnets for web servers.
9. Configure an Application Load Balancer and a target group for distributing web traffic.
10. Create an Auto Scaling Group to manage EC2 instances automatically.
11. Store web files on GitHub for version control.
12. Secure application communications using SSL/TLS certificates from Certificate Manager.
13. Configure Simple Notification Service (SNS) for monitoring.
14. Register a domain name and set up DNS records using Route 53.
15. Utilize Amazon EFS for a shared file system.
16. Set up Amazon RDS for the database.

## Repository Structure

- `scripts/`: Contains scripts for setting up AWS resources.
- `diagram/`: Includes the reference architecture diagram.
- `README.md`: Provides an overview of the project, deployment instructions, and scripts.
