# AWS Secure 3-Tier Architecture Deployment

## Architecture Overview
User → CloudFront → Application Load Balancer → EC2 Auto Scaling → RDS Database

## Components Used
- VPC
- Public and Private Subnets
- Internet Gateway
- Route Tables
- Security Groups
- EC2 Instances
- Application Load Balancer
- Auto Scaling Group
- Amazon RDS
- Amazon S3
- Amazon CloudFront
- Amazon CloudWatch

## Deployment Steps

1. Create VPC
2. Create Public and Private Subnets
3. Attach Internet Gateway
4. Configure Route Tables
5. Create Security Groups
6. Launch EC2 Web Servers
7. Install Apache Web Server
8. Create Application Load Balancer
9. Register EC2 instances in Target Group
10. Create Auto Scaling Group
11. Create RDS Database
12. Create S3 bucket for storage and logs
13. Create CloudFront distribution
14. Enable ALB access logs → S3
15. Configure CloudWatch monitoring and alarms
16. Create CloudWatch dashboard
