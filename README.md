# WordPress Website Deployment on AWS

This repository contains scripts and configuration files to deploy a WordPress website on AWS utilizing various services and resources. Below is a detailed guide on how to set up and deploy the WordPress website following the provided configuration.

## Architecture Overview

The deployment architecture includes the following components:

1. **Virtual Private Cloud (VPC):** Configured with public and private subnets across two availability zones for enhanced availability and fault tolerance.

2. **Internet Gateway:** Facilitates connectivity between VPC instances and the wider Internet.

3. **Security Groups:** Acts as a network firewall mechanism to control traffic to EC2 instances.

4. **EC2 Instances:** Web servers hosting the WordPress application, located within private subnets for enhanced security.

5. **NAT Gateway:** Enables instances in private subnets to access the Internet.

6. **Application Load Balancer (ALB):** Distributes incoming web traffic across multiple EC2 instances in different availability zones for scalability and fault tolerance.

7. **Auto Scaling Group:** Automatically manages EC2 instances to ensure website availability, scalability, fault tolerance, and elasticity.

8. **Amazon EFS (Elastic File System):** Provides a shared file system for storing web files.

9. **Amazon RDS:** Hosts the WordPress database.

10. **Route 53:** Registers the domain name and sets up DNS records for the website.

11. **Certificate Manager:** Secures application communications using SSL/TLS certificates.

12. **Simple Notification Service (SNS):** Sends alerts about activities within the Auto Scaling Group.

## Deployment Steps

### 1. Initial Setup

- Clone this repository to your local machine.

### 2. Configure AWS Resources

- Refer to the provided diagram and scripts for setting up the VPC, subnets, internet gateway, security groups, NAT gateway, ALB, Route 53, EFS, RDS, and other necessary resources in your AWS account.

### 3. Deploy WordPress Website

#### EC2 Instance Installation Script

- Use the provided EC2 instance installation script to install Apache HTTP Server, PHP, MySQL, and other dependencies on EC2 instances.

```bash
<Insert EC2 instance installation script here>
```

#### Auto Scaling Group Launch Template Script

- Utilize the provided Auto Scaling Group launch template script to configure EC2 instances for auto-scaling purposes.

```bash
<Insert Auto Scaling Group launch template script here>
```

### 4. WordPress Setup

- Follow the WordPress installation steps after deploying the EC2 instances:
  1. Mount the EFS volume to the EC2 instances for storing web files.
  2. Download and extract the latest WordPress files to the document root.
  3. Configure the `wp-config.php` file with database credentials.
  4. Restart the Apache HTTP Server service.

### 5. Testing and Monitoring

- Test the website to ensure proper functionality.
- Monitor the Auto Scaling Group for scaling events and utilize SNS notifications for alerts.

## Contributors

- [Mohammad Madamani]

