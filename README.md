# AWS VPC - Virtual Private Cloud

## Table of Contents

1. **Project Overview**
1.1**Objectives**
2. **Project Steps and Commands**
   - 2.1 [Go to VPC Page](#21-go-to-vpc-page)
   - 2.2 [Create VPC](#22-create-vpc)
   - 2.3 [Configure VPC](#23-configure-vpc)
   - 2.4 [Create Subnets](#24-create-subnets)
   - 2.5 [Set Up Internet Gateway](#25-set-up-internet-gateway)
   - 2.6 [Configure Route Tables](#26-configure-route-tables)
   - 2.7 [Set Up NAT Gateway](#27-set-up-nat-gateway)
   - 2.8 [VPC Peering](#28-vpc-peering)
3. **Troubleshooting (Common Issues and Solutions)**
   - 3.1 [VPC Not Connecting to Internet](#31-vpc-not-connecting-to-internet)
   - 3.2 [Subnet Routing Issues](#32-subnet-routing-issues)
   - 3.3 [VPC Peering Not Working](#33-vpc-peering-not-working)
   - 3.4 [NAT Gateway Connectivity Issues](#34-nat-gateway-connectivity-issues)

---

## 1. Project Overview
This document provides a step-by-step guide to setting up an AWS Virtual Private Cloud (VPC) with subnets, an internet gateway, a NAT gateway, and VPC peering. The guide includes images for reference.

## 1.1 Objectives
The objective of this project is to **design and deploy a custom AWS VPC** that meets the following requirements:
- Create a private and public subnet to isolate internal and external resources.
- Establish secure internet access using an **Internet Gateway (IGW)** for public resources.
- Enable secure outbound traffic for private subnets using a **NAT Gateway**.
- Set up proper **Route Tables** to ensure correct network traffic flow.
- Implement **VPC Peering** to allow communication between two different VPCs.

By following this guide, users will gain hands-on experience in AWS networking, which is essential for cloud infrastructure management and security best practices.

## 2. Project Steps and Commands

### 2.1. Go to VPC Page
![VPC Page](https://github.com/user-attachments/assets/1d4cff53-61c7-47c8-984d-1c51ea9514b7)

### 2.2 Create VPC
![Create VPC](https://github.com/user-attachments/assets/d3a9ae6b-e881-4362-bbbb-af9d7803ce1d)

### 2.3. Configure VPC
![Configure VPC](https://github.com/user-attachments/assets/bda10683-6e7f-49fa-a1d6-b667cc2b9aaa)

### 2.4. Create Subnets
![Create Subnet](https://github.com/user-attachments/assets/01c4215d-38f2-491d-b64c-31a6f4680ed2)

![Subnet Created](https://github.com/user-attachments/assets/10a4477b-e7c1-4e2f-acae-4e4465f587f4)

### 2.5. Set Up Internet Gateway
![Create Internet Gateway](https://github.com/user-attachments/assets/1d7edf2b-7fd7-4a0b-827c-02baef3274dc)

![Attach Internet Gateway](https://github.com/user-attachments/assets/b9b9d9c3-dc26-4436-b188-0d2ad8d586a6)

### 2.6. Configure Route Tables
![Route Table](https://github.com/user-attachments/assets/f60c8df0-3afd-4b81-8ece-a5dc76baa4a0)

![Edit Routes](https://github.com/user-attachments/assets/2d81aa2f-82b7-4f60-a734-c72f8f6cfbb1)

![Configure IGW Route](https://github.com/user-attachments/assets/66af302b-f308-4af8-a411-e513288f1580)

### 2.7. Set Up NAT Gateway
![Create NAT Gateway](https://github.com/user-attachments/assets/cd3be463-0464-443d-8edf-1b8bc82918b8)

![Add NAT Gateway to Route Table](https://github.com/user-attachments/assets/49af1a84-55d5-4229-ab44-1ae1dadb4030)

### 2.8. VPC Peering
![Create VPC Peering](https://github.com/user-attachments/assets/a5146609-256e-4f1b-af4d-bcf5544b9a76)

![Accept Peering Request](https://github.com/user-attachments/assets/fde028d0-f948-4a2a-b7a0-b1658310afe9)

![Edit Peering Route Table](https://github.com/user-attachments/assets/7b2b5e93-75c4-43aa-9a2a-0df4b809f256)

---

## 3. Troubleshooting (Common Issues and Solutions)

### 3.1. VPC Not Connecting to Internet
**Issue:** Instances in the VPC cannot access the internet.
**Solution:**
- Ensure an Internet Gateway is attached.
- Verify route tables include a route to `0.0.0.0/0` via the Internet Gateway.

### 3.2. Subnet Routing Issues
**Issue:** Private instances are not communicating with public instances.
**Solution:**
- Confirm that the route table for private subnets has a NAT Gateway route.
- Ensure the correct subnet associations are applied.

### 3.3. VPC Peering Not Working
**Issue:** Two VPCs are peered but cannot communicate.
**Solution:**
- Make sure both VPCs have updated route tables with the peer’s CIDR block.
- Verify security groups allow inbound and outbound traffic between the VPCs.

### 3.4. NAT Gateway Connectivity Issues
**Issue:** Instances in a private subnet cannot access the internet.
**Solution:**
- Verify NAT Gateway is correctly attached to the correct public subnet.
- Ensure route tables for private subnets route traffic via the NAT Gateway.

---


