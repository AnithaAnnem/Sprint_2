
![image](https://github.com/user-attachments/assets/db001cfb-79bf-4c83-9e64-00f31a845bc8)


|**Author**        | **created on**       | **Version** |**Last edited on**| **Review Level**   | **Reviewer**      |
|---------------|------------|---------|--------|--------|----------------------|
| Anitha Annem  | May 13  | v1.0|  May 14    | Pre-Reviewer   | Priyanshu            |
| Anitha Annem  |  |  |   | L0             | Khushi Malhothra    |
| Anitha Annem  |      |      |         | L1             | Mukul Joshi       |
| Anitha Annem  |      |      |         | L2             | piyush Upadhyay      |
  


# Infra Setup of SonarQube

![image](https://github.com/user-attachments/assets/0846c225-ef41-409d-a5c5-5d419adac028)


## 1. Start with VPC Creation
I created a custom VPC named sonarqube-vpc with the CIDR block 10.0.0.0/16.

This provides a large address range to create multiple subnets and isolate components securely.

## 2. Subnet Architecture Across Two Availability Zones
I divided the VPC across two Availability Zones (e.g., us-east-1a and us-east-1b) to ensure high availability.

Public Subnets:

One in each AZ (e.g., 10.0.1.0/24 and 10.0.2.0/24)

These host the Bastion Host and NAT Gateway.

Private Subnets:

One in each AZ (e.g., 10.0.3.0/24 and 10.0.4.0/24)

These are used to host the SonarQube instance and optionally the database (e.g., RDS).

## 3. Internet Gateway and Public Route Configuration
I created and attached an Internet Gateway to the VPC.

The public subnets are associated with a public route table that routes 0.0.0.0/0 to the Internet Gateway, enabling public internet access.

## 4. NAT Gateway for Private Subnets
I provisioned a NAT Gateway in one of the public subnets, and associated an Elastic IP with it.

The private route table (used by private subnets) routes internet-bound traffic (0.0.0.0/0) to the NAT Gateway.

This allows instances in private subnets (like SonarQube) to access the internet outbound only, for things like downloading plugins or updates.

## 5. Security Groups and NACL Configuration
Security Groups:

Bastion Host SG allows SSH (port 22) from my local IP.

SonarQube SG allows:

Internal traffic from the Bastion Host SG (SSH or HTTP via tunnel)

HTTP/HTTPS if accessed via internal load balancer or port 9000 for SonarQube UI.

Database SG (optional): Allows only SonarQube SG to connect on port 5432.

Network ACLs:

Public subnets allow inbound/outbound HTTP, HTTPS, and SSH.

Private subnets allow only required internal ports, blocking all other unnecessary traffic.

## 6. Bastion Host Setup
Deployed in a public subnet.

Used to securely connect to the SonarQube instance in the private subnet via SSH.

Acts as the jump server.

## 7. SonarQube EC2 Deployment in Private Subnet
Launched an EC2 instance (SonarQube) in a private subnet without a public IP.

Used the Bastion Host (SSH tunneling or port forwarding) to access SonarQube.

Alternatively, could access through an internal ALB if a web UI is needed from within the VPC.

## 8. Access Flow
Developer/Admin connects to Bastion Host (public).

From Bastion, connects to SonarQube EC2 instance (private).

SonarQube can reach the internet (for plugin updates, etc.) via NAT Gateway.

If a web UI is needed, use SSH tunneling or place a load balancer in front (internal or public with restricted access).




