# Day 2: Data Protection & Compliance 🔐

**Topic:** Securing Data, Encryption, & Compliance Tools

---

##  Key Concepts Learnt

### 1. Data Encryption (The Two States)
* **Data at Rest:** Protecting data stored on disk (e.g., in S3 buckets).
    * *Standard:* Uses **AES-256** encryption (Server-Side Encryption).
* **Data in Transit:** Protecting data moving across the network.
    * *Standard:* Uses **TLS/SSL** (Transport Layer Security) via **AWS Certificate Manager (ACM)** to prevent "Man-in-the-Middle" attacks.

### 2. S3 Security Strategies
* **Amazon S3 Block Public Access:** The "Master Switch" that prevents a bucket from ever becoming public, overriding all other permissions.
* **Bucket Policies:** JSON documents attached strictly to the resource (S3 bucket) to control who can access specific files.
* **IAM Policies:** Permissions attached to "Identities" (Users/Roles) that determine what actions they can perform.
* **Access Control Lists (ACLs):** A legacy method for managing access to buckets and objects (less common now, but still exists).
* **AWS Trusted Advisor:** An automated tool that scans the account and recommends security improvements (like closing open ports or enabling MFA).

### 3. Compliance in AWS
* **AWS Artifact:** The "Library" for downloading official audit reports (like ISO 27001 or SOC 2) to prove AWS is compliant.
* **AWS Config:** The "Camera" that continuously monitors resource configurations. It alerts me if a resource becomes non-compliant.

---


* **Ciphertext:** The unreadable, encrypted version of data.
* **HTTPS:** The secure version of HTTP, enabled by SSL/TLS certificates.
