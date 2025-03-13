🚀 Host a Dynamic Web App on AWS with Docker, Amazon ECR, and Amazon ECS

📌 Overview

This project demonstrates how to deploy a dynamic web application on AWS using Docker, Amazon ECR (Elastic Container Registry), and Amazon ECS (Elastic Container Service). The application utilizes a LAMP stack (Linux, Apache, MySQL, PHP) and follows best practices for security and deployment.

🔧 Prerequisites

✅ An AWS account

✅ AWS CLI installed and configured

✅ Docker installed on your local machine

✅ GitHub account for code storage

✅ SSH key pair for secure access

✅ Basic knowledge of AWS services

📜 Deployment Steps

1️⃣ Set Up SSH Keys

-- Create an SSH key pair to clone a private GitHub repository.-- Add the public key to GitHub.

2️⃣ Create a Three-Tier VPC Network

-- Create a VPC, Internet Gateway, and attach it to the VPC.-- Configure public and private subnets.-- Set up NAT Gateways for private subnet internet access.

3️⃣ Configure Security Groups

-- Create security groups with appropriate inbound and outbound rules.

4️⃣ Set Up RDS Database (MySQL)

-- Create subnet groups for RDS.-- Launch a MySQL database instance in a private subnet.

5️⃣ Clone and Push Application Code

-- Clone the GitHub repository locally.-- Push the application code to GitHub.

6️⃣ Create Docker Configuration

-- Write a Dockerfile for the LAMP stack.-- Use .gitignore to prevent sensitive information from being pushed.-- Implement environment variables for security.-- Build the Docker image.

7️⃣ Push Docker Image to Amazon ECR

-- Create an ECR repository.-- Authenticate AWS CLI for ECR access.-- Tag and push the Docker image to ECR.

8️⃣ Set Up Bastion Host and Migrate SQL Data

-- Create an EC2 instance as a Bastion Host for secure access.-- Use SSH tunneling to connect to the RDS instance.-- Install Flyway for database migrations.-- Execute SQL migration scripts.

9️⃣ Configure Load Balancing

-- Create a Target Group.-- Set up an Application Load Balancer (ALB).

🔟 Store Environment Variables Securely

-- Use an S3 bucket to store environment variables.-- Assign IAM roles with proper permissions to access S3.

1️⃣1️⃣ Deploy the Application on ECS Fargate

-- Create an ECS cluster.-- Define a task with CPU and memory allocation.-- Deploy the containerized application using ECS Fargate.

1️⃣2️⃣ Configure DNS for the Application

-- Create an A record in Route 53.-- Point it to the ALB DNS name.

🎉 Final Outcome

Your dynamic web application will be successfully deployed on AWS ECS Fargate in a serverless manner. 🚀✨
