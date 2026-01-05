# Day 1: AWS Foundations & Security Essentials 

**Date:** January 5, 2026
**Topic:** Shared Responsibility, IAM, & Securing Accounts

---

## What I Learnt

### 1. The Shared Responsibility Model
Studied the "Digital Property Line" between AWS and the Customer.
* **AWS Responsibility (Security OF the Cloud):** Physical hardware, data centers, cabling, and managed services.
* **My Responsibility (Security IN the Cloud):** Guest OS patching, firewall configuration, and client-side data encryption.
* **Key Takeaway:** Security is a partnership. I am fully responsible for the security of everything I put *into* the cloud.

### 2. Identity & Access Management (IAM)
* **Root User:** The account owner with unlimited privileges. Best practice is to lock this away and never use it for daily tasks.
* **IAM Users vs. Roles:**
    * *Users:* Long-term credentials for humans.
    * *Roles:* Temporary credentials for machines or services (e.g., an EC2 instance accessing S3).
* **Groups:** The efficient way to manage permissions for multiple users at once.

### 3. Securing Accounts (Hardening)
* **Principle of Least Privilege:** Granting only the specific permissions a user needs to perform a task—and nothing more.
* **Password Policies:** Enforcing length, complexity, and rotation to prevent brute-force attacks.
* **MFA (Multi-Factor Authentication):** The critical second layer of defense (Something you know + Something you have).
