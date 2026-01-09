# Day 4: VPC Security, DNS, & Content Delivery

**Topic:** Security Groups, NACLs, Route 53, & CloudFront

---

## Key Concepts Learnt

### 1. VPC Security Layers
Understanding the "Defense in Depth" strategy for network security.
* **Security Groups :**
    * *Scope:* Acts at the **Instance (Server)** level.
    * *Behavior:* **Stateful**. If traffic is allowed IN, the response is automatically allowed OUT.
    * *Rule:* All inbound traffic is blocked by default; you must explicitly allow it.
* **Network Access Control Lists (NACLs) (The "Guard at the Gate"):**
    * *Scope:* Acts at the **Subnet** level.
    * *Behavior:* **Stateless**. You must explicitly create rules for both Inbound and Outbound traffic.
    * *Rule:* Processes rules in number order (lowest number first).

### 2. Amazon Route 53 (DNS Management)
* **DNS Resolution:** The process of translating human-readable domain names (like www.google.com) into machine-readable IP addresses (like 192.0.2.1) so computers can communicate.
* **Amazon Route 53:** A highly available and scalable cloud Domain Name System (DNS) web service. Used to register domains and route end-user traffic to applications.
* **Supported Routing Policies:**
    * **Simple Routing:** Default policy for a single resource.
    * **Weighted Routing:** Distributes traffic across multiple resources based on assigned percentages (e.g., 80% to Blue, 20% to Green).
    * **Latency Routing:** Routes traffic to the AWS Region that provides the best latency (speed) for the user.
    * **Geolocation Routing:** Routes traffic based on the geographic location of the user (e.g., users in France go to French servers).
    * **Failover Routing:** Used for High Availability (Active-Passive) configurations.
* **Failover for Multi-Tier Web Apps:**
    * Uses **Health Checks** to monitor the "Primary" application.
    * If the Primary becomes unhealthy (fails health checks), Route 53 automatically shifts traffic to a "Secondary" (Passive) standby resource, ensuring the app stays online.

### 3. Amazon CloudFront (CDN)
* **Amazon CloudFront:** A fast content delivery service that securely delivers data to customers at high transfer speeds.
* **Edge Locations:** Caches content at physical locations closer to the users, reducing the load on the origin server.
* **Origins:** The source of the content (e.g., S3 Bucket, EC2, or Load Balancer).

---

* **Health Checks:** Automated requests sent by Route 53 to verify that a resource is reachable, available, and functional.
