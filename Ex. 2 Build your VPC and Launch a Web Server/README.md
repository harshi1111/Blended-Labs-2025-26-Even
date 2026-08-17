# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: Harshitha V
* **Register Number**: 212223230074
* **Date of Submission**: 17-08-2026

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)

(Write the steps you followed in your own words)

1. Created a VPC with public and private subnets, along with the required Internet Gateway and NAT Gateway.
2. Created additional public and private subnets in a second Availability Zone and configured their route tables.
3. Created a security group and allowed HTTP access to the web server.
4. Launched an EC2 instance named Web Server 1 in the public subnet and configured it with the security group
5. Installed and started the web server using the launch script, accessed it through its public DNS, and verified that the web page was working

---

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1536" height="692" alt="image" src="https://github.com/user-attachments/assets/1d543661-1095-4c81-993c-2371ccf83fe5" />


---

### Screenshot 2: EC2 Instance Running

<img width="1372" height="712" alt="Screenshot 2026-08-17 154740" src="https://github.com/user-attachments/assets/c51b9594-c6f6-47bb-b412-46e162e7ab13" />


---

### Screenshot 3: Web Server Output in Browser

<img width="1345" height="533" alt="Screenshot 2026-08-17 155252" src="https://github.com/user-attachments/assets/707d2cbc-b5d9-4200-a59c-91fb4ea83dc9" />


---

## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
