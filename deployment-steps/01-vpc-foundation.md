# VPC Foundation

This step builds the networking foundation for the AWS secure 3-tier architecture.

## Components

- VPC
- Public subnets
- Private subnets
- Internet Gateway
- NAT Gateway
- Route tables

## Architecture Design

VPC CIDR: 10.0.0.0/16

Public Subnets:
10.0.1.0/24
10.0.2.0/24

# VPC Foundation

This step builds the networking foundation for the AWS secure 3-tier architecture.

## Components

- VPC
- Public subnets
- Private subnets
- Internet Gateway
- NAT Gateway
- Route tables

## Architecture Design

VPC CIDR: 10.0.0.0/16

Public Subnets:
10.0.1.0/24
10.0.2.0/24

Private Subnets:
10.0.11.0/24
10.0.12.0/24

## Goal

Create a secure network architecture where:

- Load balancers live in public subnets
- EC2 application servers live in private subnets
- Databases are isolated in private subnets
