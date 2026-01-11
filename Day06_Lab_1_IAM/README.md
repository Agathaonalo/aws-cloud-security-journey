**Lab 1: Introduction to AWS IAM**

**Lab Overview**

In this lab, I explored pre-created users and groups to understand the concept of Implicit Deny. I then assigned users to groups to grant them the specific permissions needed for their roles, verifying Least Privilege access.

**Task Execution** 

**Task 1: Explore Users and Groups**

I inspected the IAM dashboard and verified the pre-created users (user-1, user-2, user-3). At this stage, they had valid credentials but no permissions.


**Task 2: Assign Users to Groups**

Acting as the Administrator, I granted specific permissions by adding users to their respective job-role groups:

Added user-1 to the S3-Support group.

Added user-2 to the EC2-Support group.

Added user-3 to the EC2-Admin group. 


**Task 3: Test Permissions & Policies**

I verified the permissions for each user to ensure the policies were working as expected.

**The "Implicit Deny" Check:**
Before assignment, I confirmed that user-1 received an "Access Denied" error when trying to view resources.

**S3 Access Verification:**
user-1 logged in and successfully accessed S3 buckets (Read-Only access).

**EC2 Support Check:**

Logged in as user-2.

Verified ability to view EC2 instances.

Attempted to stop an instance and was correctly DENIED (proving they only had ReadOnly access).

**EC2 Admin Check:**

Logged in as user-3.

Verified ability to stop an instance (proving they had Admin access).


**Key Learnings**

Implicit Deny: Every API call is denied by default until an Identity-based or Resource-based policy allows it.

Groups vs. Users: Managing permissions at the Group level is much more scalable than attaching policies to individual users.

Least Privilege: user-2 could see EC2 instances but could not stop them, while user-3 could stop them. This differentiation is critical for secure operations.

