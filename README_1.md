# AWS VPC - Virtual Private Cloud
# Table of Contents

1. **Project Overview**
2. **Project Steps and Commands**
   - 2.1 [Create Project Directory](#21-create-project-directory)
   - 2.2 [Initialize Git Repository](#22-initialize-git-repository)
   - 2.3 [Create the Bash Script File (.sh)](#23-create-the-bash-script-file-sh)
   - 2.4 [Make the Script Executable](#24-make-the-script-executable)
   - 2.5 [Set Up GitHub Repository and Link Remote](#25-set-up-github-repository-and-link-remote)
3. **Script Implementation Steps**
   - 3.1 [Prompt for User Input](#31-prompt-for-user-input)
   - 3.2 [Ask for Table Type (Full or Partial)](#32-ask-for-table-type-full-or-partial)
   - 3.3 [Full Multiplication Table](#33-full-multiplication-table)
   - 3.4 [Partial Multiplication Table](#34-partial-multiplication-table)
   - 3.5 [Validate Input Range for Partial Table](#35-validate-input-range-for-partial-table)
   - 3.6 [Handle Invalid Options](#36-handle-invalid-options)
4. **Troubleshooting (Common Issues and Solutions)**
   - 4.1 [Script Permission Denied](#41-script-permission-denied)
   - 4.2 [Invalid Input for Number](#42-invalid-input-for-number)
   - 4.3 [Invalid Range in Partial Table](#43-invalid-range-in-partial-table)
   - 4.4 [Git Remote Connection Issues](#44-git-remote-connection-issues)


## 1. Project Overview
********.

## 2. Project Steps and Commands

### 2.1. Go to VPC page
- ![Vpc](image.png)

   

### 2.2 Create VPC 
-![Create vpc](image-1.png)

### 2.3. Configure VPC 
![Configure](image-2.png)

- Created successfully
![Created](image-3.png)

### 2.4. Goto to Subnets on the sidebar and create a subnet
![subnet](image-4.png)

![Created subnet](image-5.png)

![New subnet](image-6.png)

![Second subnet created](image-7.png)

![subnets](image-8.png)

### 2.5. Internet Gateway
- ![Go to Internet gateway and create](image-9.png)

![Created internet gate way](image-10.png)


### 2.5. Internet Gateway
- Go and attach vpc 

![Attach vpc](image-11.png)

- VPC attached 

![Attached](image-12.png)

### 2.6 Route Tables

- Goto the route table
![Route table](image-13.png)

- Create route table

![alt text](image-14.png)

Go to subnet associations and edit them 

- ![Subnet associations](image-15.png)

- Save association 
- ![association](image-16.png)

 - Go to routes and edit  
- ![alt text](image-17.png)

- Configure route to Internet gate way
 ![IGW](image-18.png)


## 2.7 NAT Gateway
- Goto Nat Gateway

- ![Nat gateway](image-19.png)

- Create Nat gateway

- ![Create nat gw](image-20.png)

- New Nat Gateway
 - ![Nat gateway](image-21.png)

 - On the subnet got to the route table section and add the nat gateway
 - ![route table](image-22.png)

 - Click on the route table id 
 - ![route table](image-23.png)

  - Go to the routes section and edit route
   - ![alt text](image-24.png)

   - Add nat gateway route and save
   -![alt text](image-25.png)

   Go to the subnet part of the route table 
   -![subnet](image-26.png)

   Save private subnet association
   - ![association](image-27.png)

### 3.1. VPC Peering
- Create a two new vpcs Accepter and requester 

- ![Requester vpc](image-28.png)

- ![Accepter vpc](image-29.png)

- Create vpc peering 
- ![Peering](image-30.png)

- Put you two vpcs that you want to peer
- ![Peers](image-31.png)

- ![Create peering connection](image-32.png)

-In the peering connection click on action
-![Action](image-33.png)

- Then accept the request

-![Accept request](image-34.png)

- Click on the accepter vpc main routing table 
- ![Main route table](image-35.png)


- Go to route section and click on edit routes
-![route](image-36.png)

Got to requester vpc and copy out the ipv4 CIDR 
- ![CIDR](image-37.png)

- Add it as a route to the main route table , do same for the accepter vpc
- ![accepter vpc](image-39.png)
- Got to the requester main route table
-![requester main route table](image-40.png)

- Go to route section 
-![Route](image-41.png)

- Then add route 
-![Add route](image-42.png)









## 4. Troubleshooting (Common Issues and Solutions)

