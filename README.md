## Overview of the PoC

This Proof of Concept (PoC) demonstrates the integration of AWS infrastructure with New Relic monitoring to observe and analyze a WordPress application hosted on AWS (Linux EC2). The setup includes a secure, scalable architecture following AWS best practices, with monitoring insights from New Relic to optimize performance and ensure application health.

## Purpose and Objectives

- Deploy a WordPress website on AWS using EC2 and MySQL RDS with a well-architected VPC setup.
- Integrate New Relic to monitor application performance, infrastructure health, and uptime.
- Document the AWS configuration and monitoring setup as a reference for cloud deployments with third-party ISV integrations.
- Highlight AWS security best practices, including VPC design, subnets, and security groups.

## High-Level Summary of AWS Setup & New Relic Integration

### AWS Setup
- **VPC Configuration:** Multi-AZ architecture with private and public subnets for high availability.
- **Security Groups:** Granular inbound/outbound rules to ensure secure access to resources.
- **EC2 & RDS Deployment:** Amazon Linux 2 instances with MySQL database for scalable application deployment.
- **ALB (Application Load Balancer):** Distributes incoming traffic across the WordPress instance to ensure optimal load balancing.
- **NAT Gateway & Internet Gateway:** Manage access to the internet for public and private subnets.
- **Route Tables:** Direct traffic within VPC subnets and control access to external resources, including routing internet-bound traffic through the Internet Gateway or NAT Gateway.

### New Relic Integration
- **New Relic Agent Installation:** Installed on EC2 instances to monitor application performance in real time.
- **Application Monitoring:** Provides detailed insights into PHP performance and MySQL database queries to optimize the application.
- **Infrastructure Monitoring:** Tracks CPU, memory, network activity, and logs to help monitor infrastructure health.

## Architecture Diagram:
![AWS + WP + New Relic integration](/Architecture-Diagrams/AWS.pdf)

## Detailed setup guide: 
![AWS + WP + New Relic integration](/Setups/AWS-VPC.md)
