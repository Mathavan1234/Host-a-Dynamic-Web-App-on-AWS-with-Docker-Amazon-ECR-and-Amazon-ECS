# 🚀 Dynamic Web App Deployment on AWS ECS Fargate

## Overview

This project demonstrates the deployment of a dynamic web application using AWS ECS Fargate, leveraging a three-tier network architecture.

---

## Steps Involved

1. Setting Up SSH Access

- Created SSH key pair for secure access to private GitHub repositories.

- Added the public key to GitHub.

2. Creating the Three-Tier VPC Network

Created a VPC.

Attached an Internet Gateway to the VPC.

3. Configuring Public and Private Subnets

Created public and private subnets.

Configured public route tables to enable internet access.

Configured private route tables with NAT gateways for external connectivity.

4. Security Groups

Created necessary security groups to control inbound and outbound traffic.

5. Setting Up RDS Database

Created subnet groups.

Provisioned a MySQL RDS database instance.

6. Application Code Management

Created a GitHub repository.

Cloned the repo locally and pushed application code.

7. Docker Setup

Created a repository for storing Docker files.

Generated a personal access token for GitHub.

Developed a LAMP stack Dockerfile with environment variables.

Used .gitignore to prevent sensitive data leaks.

Created a .ps extension script for secure environment variable management.

Built the Docker image.

8. Pushing Docker Image to AWS ECR

Created an AWS ECR repository.

Configured IAM user for authentication.

Tagged and pushed the Docker image to ECR.

9. Configuring Bastion Host and SQL Migration

Created a key pair for SSH into EC2 instances.

Deployed a Bastion Host for secure database access.

Installed Flyway for SQL migrations.

Set up an SSH tunnel to migrate SQL data into the RDS database.

10. Load Balancing and Scaling

Created an Application Load Balancer (ALB).

Configured a target group for the ALB.

11. Environment File and S3 Storage

Created an environment file.

Marked it as ignored in Git.

Stored the file securely in an S3 bucket.

Configured IAM policies for S3 access.

12. Deploying the Application on ECS Fargate

Created an ECS cluster.

Defined an ECS task for containerized application deployment.

Configured an ECS service to run Fargate containers.

Verified healthy status of deployed instances.

13. Domain Configuration

Created an A record to map the domain to the ALB DNS name.

---

## Conclusion

The dynamic web application is successfully deployed on AWS ECS Fargate in a serverless manner. 🎉

