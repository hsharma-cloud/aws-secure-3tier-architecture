# AWS Secure 3-Tier Architecture

This project demonstrates a secure and scalable 3-tier architecture built on AWS.  
The goal is to simulate a real-world cloud infrastructure using core AWS services while following best practices for security, scalability, and high availability.

---

## Architecture Overview

The application follows a traditional **3-tier architecture**.

User → CloudFront → Application Load Balancer → EC2 Auto Scaling → RDS Database






## Architecture Components

This architecture is deployed inside a custom AWS Virtual Private Cloud (VPC) designed to separate public-facing resources from internal application and database layers.

### VPC

VPC CIDR Block  
10.0.0.0/16

The VPC provides network isolation for the application infrastructure.

### Public Subnets

Public subnets host resources that must be accessible from the internet.

Components deployed in public subnets:

- Application Load Balancer
- NAT Gateway
- Internet Gateway attachment

Example CIDR ranges:

10.0.1.0/24  
10.0.2.0/24

### Private Subnets

Private subnets host internal application and database resources that should not be directly accessible from the internet.

Components deployed in private subnets:

- EC2 application servers
- Amazon RDS database

Example CIDR ranges:

10.0.11.0/24  
10.0.12.0/24

### Security Controls

Security is enforced using multiple AWS mechanisms:

- Security Groups for instance-level firewall rules
- Network isolation using private subnets
- IAM roles for controlled service permissions

### Monitoring

Monitoring and operational visibility are provided using:

- Amazon CloudWatch metrics
- CloudWatch alarms
- Log monitoring

### Architecture Layers

**Edge Layer**
- CloudFront CDN
- AWS WAF (optional)

**Web Layer**
- Application Load Balancer
- EC2 instances in an Auto Scaling group

**Application Layer**
- EC2 application servers in private subnets

**Database Layer**
- Amazon RDS in private subnet

---

## AWS Services Used

- Amazon VPC
- Amazon EC2
- EC2 Auto Scaling
- Elastic Load Balancer (Application Load Balancer)
- Amazon RDS
- Amazon S3
- Amazon CloudFront
- AWS IAM
- Amazon CloudWatch

---

## Network Architecture

The infrastructure runs inside a custom VPC.

Example CIDR layout:

VPC: 10.0.0.0/16

Public Subnets
- 10.0.1.0/24
- 10.0.2.0/24

Private Subnets
- 10.0.11.0/24
- 10.0.12.0/24

Public subnets host:
- Load balancers
- NAT gateway

Private subnets host:
- EC2 application servers
- RDS database

---

## Project Structure

aws-secure-3tier-architecture

├── terraform  
├── architecture-diagram  
├── deployment-steps  
├── screenshots  
└── README.md  

### Directory Purpose

**terraform/**  
Infrastructure-as-code for deploying the architecture.

**architecture-diagram/**  
Contains architecture diagrams.

**deployment-steps/**  
Step-by-step documentation of the build process.

**screenshots/**  
Screenshots of AWS resources and deployment.

---

## Goals of This Project

- Practice designing secure AWS architectures
- Implement high availability cloud infrastructure
- Learn scalable web application design
- Build a cloud architecture portfolio project
- Document infrastructure deployment

---

## Future Improvements

- Terraform automation
- CloudWatch monitoring and alerts
- CI/CD pipeline integration
- Security hardening
- Architecture diagrams

---

## Author

Cloud architecture lab project built for learning and portfolio development.
