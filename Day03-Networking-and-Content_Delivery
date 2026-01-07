# Day 3: Networking Basics & VPC 

**Topic:** IP Addressing, CIDR, Subnets, & AWS VPC Connectivity

---

## Key Concepts Learnt

### 1. Networking Fundamentals
* **IPv4 Addresses:** 32-bit numbers represented as four decimals (e.g., 192.168.1.1).
    * *Binary Basics:* Learned binary conversion for 8-bit octets (e.g., 192 = 11000000).
* **IPv6:** The future standard, utilizing 128-bit addresses formatted in hexadecimal.
* **The OSI Model:** A framework for network troubleshooting. Reviewed **Layer 3 (Network/IP)** and **Layer 4 (Transport/Ports)** as critical layers.

### 2. CIDR (Classless Inter-Domain Routing)
* **Definition:** The method for allocating IP addresses and defining network sizes.
* **VPC Sizing:** Typically uses a **/16** (65,536 IPs) for the main network.
* **Subnet Sizing:** Typically uses a **/24** (256 IPs) for subnets inside the VPC.
* **AWS Constraint:** The minimum subnet size allowed is **/28** (16 IPs).

### 3. Amazon VPC & Subnets
* **VPC (Virtual Private Cloud):** A private network logically isolated in the AWS Cloud.
    * *Scope:* Spans an entire **Region**.
* **Subnets:** Segments of the VPC network.
    * *Scope:* Confined to a single **Availability Zone (AZ)**.

### 4. AWS Reserved IP Addresses
* **The Rule:** In every subnet, AWS reserves the first 4 and the last 1 IP address (5 total).
* **Usable IPs:** This means a standard /24 subnet has **251** usable IPs instead of 256.
* **Reserved List:** Network address, VPC Router, DNS, Future Use, and Network Broadcast.

### 5. Public vs. Elastic IP Addresses
* **Standard Public IPs:** Dynamic addresses that change if the instance is stopped and started.
* **Elastic IPs:** Static IPv4 addresses designed for dynamic cloud computing; they persist until released.

### 6. VPC Networking Components
* **Internet Gateway (IGW):** The logical connection that allows resources in a public subnet to connect to the internet.
* **Route Tables:** The rules that determine where network traffic is directed (e.g., pointing to the IGW).
* **NAT Gateway:** Allows instances in a private subnet to connect to the internet (for updates) without receiving inbound traffic.
* **VPC Wizard:** An AWS Console tool that automates the creation of a VPC, subnets, and route tables in a single step.
* **VPC Peering:** A direct network connection between two VPCs that allows them to communicate as if they were in the same network.
* **VPC Sharing:** Allows multiple AWS accounts to create resources into centrally managed, shared subnets.
* **AWS Site-to-Site VPN:** A secure, encrypted connection between your VPC and your on-premises data center over the public internet.
* **AWS Direct Connect:** A dedicated, private physical network connection from your office to AWS (bypassing the public internet).
* **AWS Transit Gateway:** A central "hub" that connects thousands of VPCs and on-premises networks together in a simplified topology.
