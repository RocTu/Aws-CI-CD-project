# Aws-CI-CD-project

## Description
This project demonstrates how to set up a CI/CD pipeline using AWS services, specifically AWS Elastic Beanstalk and Amazon RDS. The aws pipeline fetches code from a repository and deploys it to a configured environment, showcasing a complete CI/CD workflow on AWS.

## Features
- AWS Elastic Beanstalk environment setup
- Amazon RDS database configuration
- CI/CD pipeline implementation
- Automated code deployment
- Integration between Elastic Beanstalk and RDS
- java 17
- using mysql mariadb in Rds
- 
## Prerequisites
Before starting the project, ensure you have:
- An AWS account with appropriate permissions
- Basic knowledge of AWS services (Elastic Beanstalk, RDS, EC2, IAM)
- 

## Setup Steps

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
- insert sql file into the msql rds login by -h -p -u than < db_backup.sql (File name is db_backup.sql )
  

### 4. Security Group Configuration
- Set up a security group to allow data flow from EC2 to RDS
- Configure SSH access for EC2 instances in order to ssh mariadb

### 5. Database Initialization
- Download the SQL file from the repository
- Connect to the EC2 instance via SSH
- Import the SQL file into the RDS MariaDB instance (file name is db_backup.sql )

### 6. fetch the code via github than update code into bitbucket
- Creating an bitbuck acount then setting the workspace inclouding remoto repository
- replace the remote url into bitbucket repositpry url of local repository which is cloned via git hub then feth the tags
- commit local repository into bitbucket repositpry

### 6. set up aws codecommit 
- login aws account setting aws codecommit fetch the source code from bitbucket
- upload the buildspec.yml file into the codecommit to build archive (The file was including java mvn install)
- Matters needing attention！⚠️ don't forget the replace username password endpoint of database into yours
- The archive will stream into s3 bucket don't forgot to creat one bucket to store your aechive

### 7.Using awspipline to  Deploy archive into beanstalk 
- use pipline to set uo the stage setting up the connection between the bitbucket and pipline
- Don't forget by using trigger in order to monitor repositpry push
- The final stage is deploy the archive to beanstalk access the url of beanstalk to testing your app connection
- 



## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Aws-CI-CD-project.git
   cd Aws-CI-CD-project
