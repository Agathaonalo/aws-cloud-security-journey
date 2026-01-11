**Lab 2: Build Your VPC and Launch a Web Server**

**Lab Overview**

In this lab, I built a custom Virtual Private Cloud (VPC) from scratch, configured the networking (Subnets, Route Tables, Internet Gateway), and deployed a public-facing Web Server.

**Task Execution**

**Task 1: Create the VPC**

I created a new VPC named Lab VPC with a CIDR block of 10.0.0.0/16. This defined the private network space for the project.

**Task 2: Configure Subnets**

I performed the necessary networking steps to create the public zone:

Created a Public Subnet within the VPC.

Configured the Route Table association to direct traffic to the Internet Gateway, making the subnet truly "public."

**Task 3: Security Group Configuration**

I configured the firewall (Security Group) to allow HTTP (Port 80) traffic from Anywhere (0.0.0.0/0), ensuring the web server is accessible to the public.

**Task 4: Launch Web Server**

I launched an EC2 instance into the Public Subnet and used a "User Data" script to install the Apache web server.

**Instance Creation:**

I verified the instance was running and associated with the correct Public IP.

W**ebsite Accessibility:**

I accessed the server via its Public DNS. The successful load of the AWS Academy page proves that the VPC networking (Route Tables + IGW) and the Security Group are correctly configured.

