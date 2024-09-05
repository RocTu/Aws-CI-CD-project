# Aws-CI-CD-project

## Description
This project demonstrates how to set up a CI/CD pipeline using AWS services, specifically AWS Elastic Beanstalk and Amazon RDS. The pipeline fetches code from a repository and deploys it to a configured environment, showcasing a complete CI/CD workflow on AWS.

## Features
- AWS Elastic Beanstalk environment setup
- Amazon RDS database configuration
- CI/CD pipeline implementation
- Automated code deployment
- Integration between Elastic Beanstalk and RDS

## Prerequisites
Before starting the project, ensure you have:
- An AWS account with appropriate permissions
- Basic knowledge of AWS services (Elastic Beanstalk, RDS, EC2, IAM)
- JDK 18 or later
- Maven 3.9 or later
- MySQL 8 or later

## Setup Steps
Then look for the file :
- /src/main/resources/accountsdb
- accountsdb.sql file is a mysql dump file.we have to import this dump to mysql db server

### 1. IAM Role Configuration
- Create an AWS IAM role for Elastic Beanstalk
- Add necessary permissions to the role for Elastic Beanstalk operations

### 2. Elastic Beanstalk Environment
- Set up Elastic Beanstalk with EC2
- Configure a load balancer to distribute incoming traffic
- Set up an Auto Scaling group for EC2 instances

### 3. Amazon RDS Setup
- Create an RDS instance using the free tier option
- Choose MariaDB as the database engine

### 4. Security Group Configuration
- Set up a security group to allow data flow from EC2 to RDS
- Configure SSH access for EC2 instances

### 5. Database Initialization
- Download the SQL file from the repository
- Connect to the EC2 instance via SSH
- Import the SQL file into the RDS MariaDB instance

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Aws-CI-CD-project.git
   cd Aws-CI-CD-project
