# Aws-vpc-network-lab

## Project Overview
This project demonstrates how to design and configure a custom Virtual Private Cloud (VPC) using Amazon Web Services (AWS).
The architecture includes public and private subnets, routing configuration, and EC2 instances to showcase network isolation and controlled internet access.

## Objectives
- Create a custom VPC
- Configure public and private subnets
- Set up route tables
- Attach an Internet Gateway
- Launch EC2 instances in each subnet
- Demonstrate network isolation

## Architecture Diagram
<img width="1122" height="1402" alt="VPC Architecture" src="https://github.com/user-attachments/assets/ab81064f-ec7f-40ce-8da0-9cfa41540eeb" />

## Technologies Used
- AWS (Amazon Web Services)
- Amazon VPC
- Amazon EC2

## Implementation Steps

1. VPC Creation
- Created VPC with CIDR block:
10.0.0.0/16

2. Subnet Configuration
- Public Subnet:
10.0.1.0/24

- Private Subnet:
10.0.2.0/24
  
3. Internet Gateway
- Created and attached Internet Gateway to VPC
- Enables internet access for public subnet

4. Route Tables

Public Route Table
- Destination: 0.0.0.0/0
- Target: Internet Gateway

Private Route Table
- No internet route configured

 5. EC2 Instances

#### Public EC2
- Located in Public Subnet
- Assigned Public IP
- Accessible from internet

#### Private EC2
- Located in Private Subnet
- No Public IP
- Not accessible from internet

## Subnet Calculations
- VPC: 10.0.0.0/16 → 65,536 IPs
- Public Subnet: 10.0.1.0/24 → 256 IPs
- Private Subnet: 10.0.2.0/24 → 256 IPs

## Testing & Validation
- Verified public EC2 is accessible via browser
- Confirmed private EC2 is not publicly accessible
- Validated route table configurations

## Screenshots
VPC
<img width="1920" height="293" alt="VPC" src="https://github.com/user-attachments/assets/af1fcb97-fa85-4e86-a66c-bb8c1e5b62c9" />
Subnets
<img width="1920" height="253" alt="Done3111" src="https://github.com/user-attachments/assets/b7875bf8-3aa5-479d-ac3e-45ecf31ed48b" />
Route tables
<img width="1920" height="317" alt="Done311" src="https://github.com/user-attachments/assets/f837b880-bef3-41f2-9ff1-e568dc5ab33a" />
EC2 Instance
<img width="1920" height="382" alt="Done 3" src="https://github.com/user-attachments/assets/587540f0-cc86-4404-a06d-90e572fea171" />
Public EC2
<img width="1142" height="248" alt="public subnet" src="https://github.com/user-attachments/assets/728aca67-9c25-446a-9a77-d739c18ae2a6" />
Private EC2
<img width="1101" height="402" alt="private ec2" src="https://github.com/user-attachments/assets/6b12baf5-d814-44c7-b9a6-b2046055a46e" />

## Key Learnings
- Designed a custom cloud network using VPC
- Implemented subnet segmentation (public vs private)
- Configured routing for internet access control
- Understood network isolation in cloud environments

## Author
A.A Micheal
