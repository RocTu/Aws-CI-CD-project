# AWS CI/CD Project with Elastic Beanstalk and RDS

## Description
This project demonstrates a complete CI/CD workflow on AWS, utilizing Elastic Beanstalk and Amazon RDS. It showcases how to set up a pipeline that automatically fetches code from a repository and deploys it to a configured environment.

## Features
- AWS Elastic Beanstalk environment setup
- Amazon RDS (MariaDB) database configuration
- CI/CD pipeline implementation using AWS CodePipeline
- Automated code deployment
- Integration between Elastic Beanstalk and RDS
- Java 17 runtime
- MySQL MariaDB in RDS

## Prerequisites
- AWS account with appropriate permissions
- Basic knowledge of AWS services (Elastic Beanstalk, RDS, EC2, IAM, CodeCommit, CodePipeline)
- Git installed locally
- Bitbucket account

## Setup Steps

### 1. IAM Role Configuration
- Create an AWS IAM role for Elastic Beanstalk
- Add necessary permissions for Elastic Beanstalk operations

### 2. Elastic Beanstalk Environment
- Set up Elastic Beanstalk with EC2
- Configure load balancer for traffic distribution
- Set up Auto Scaling group for EC2 instances

### 3. Amazon RDS Setup
- Create an RDS instance (free tier, MariaDB engine)
- Import SQL file:db_backup.sql


### 4. Security Group Configuration
- Configure security group for EC2 to RDS data flow
- Set up SSH access for EC2 instances

### 5. Code Repository Setup
1. Clone GitHub repository: https://github.com/RocTu/Aws-CI-CD-project.git
2. Create Bitbucket repository and workspace
3. Update remote URL to Bitbucket:yours bitbuck url

### 6. AWS CodeCommit Setup
- Create CodeCommit repository
- Import code from Bitbucket
- Upload `buildspec.yml` for Java Maven build
- ⚠️ Update database credentials in configuration files
- Create S3 bucket for build artifacts

### 7. AWS Pipeline Configuration
- Set up AWS CodePipeline
- Configure Bitbucket connection
- Set up trigger for repository pushes
- Add build stage using CodeBuild
- Configure deployment stage to Elastic Beanstalk

## Usage
1. Make changes to your code and push to Bitbucket
2. CodePipeline will automatically trigger the build and deployment process
3. Monitor the pipeline stages in AWS Console
4. Access your application via the Elastic Beanstalk URL

## Troubleshooting
- Check CodePipeline logs for build or deployment failures
- Verify RDS connection strings in your application configuration
- Ensure security groups allow proper communication between services

## Contributing
Contributions are welcome! Please fork the repository and create a pull request with your features or fixes.

Project Link: [https://github.com/your-username/Aws-CI-CD-project](https://github.com/your-username/Aws-CI-CD-project)




