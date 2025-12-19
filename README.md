# Highly Available Web Application Infrastructure on AWS

# Project Overview

This project demonstrates how to design and deploy a **highly available, scalable, and secure cloud infrastructure** on Amazon Web Services (AWS). It focuses on core AWS services commonly used in real-world cloud engineering and DevOps environments.

The goal of this project is to showcase hands-on experience with AWS compute, security, and scalability concepts rather than just theoretical knowledge.

---

# What This Project Demonstrates

* Understanding of AWS global infrastructure (Regions & Availability Zones)
* Secure access control using IAM and least-privilege principles
* Deployment and management of EC2 instances
* High availability using Auto Scaling Groups
* Traffic distribution using Elastic Load Balancing
* Secure server access using SSH

---

# Architecture Overview

* EC2 instances deployed across multiple Availability Zones
* Auto Scaling Group to maintain desired capacity and replace unhealthy instances
* Elastic Load Balancer to distribute incoming traffic
* IAM roles and policies for secure access control
* SSH access via local terminal and AWS CloudShell

---

# Services Used

* Amazon EC2
* Auto Scaling Group
* Elastic Load Balancing (ELB)
* AWS Identity and Access Management (IAM)
* AWS CloudShell
* Secure Shell (SSH)

---
# Implementation Steps

# IAM Configuration

* Created an IAM users with policy
  ![IAM User with Policy](screenshots/IAM_user.png)

* Created an IAM group with policy
 ![IAM Group with Policy](screenshots/IAM_group.png)

* Assigned least-privilege IAM policies
![IAM User with Console Least Priviledge Access](screenshots/IAM_user_with_LPA.png)


# EC2 Setup

* Created an EC2 launch template
![EC2 Template](screenshots/ec2_template.png)

* Launched two EC2 instances using Amazon Linux
![EC2 Instances](screenshots/ec2_instances.png)

* Configured security groups to allow SSH access
![Security Group](screenshots/security_group.png)


# Auto Scaling Group

* Created an Auto Scaling Group using the launch template
* Defined minimum (2), maximum (4), and desired instance capacity (2)
* Verified automatic instance replacement on failure
![Auto-Scaling Group](screenshots/ASG.png)

# Elastic Load Balancer

* Created an Application Load Balancer
![Elastic Load Balancer](screenshots/ELB.png)

* Attached the Auto Scaling Group as a target
* Verified traffic distribution across EC2 instances
![Traffic Distribution 1](screenshots/ip_traffic1.png)
![Traffic Distribution 2](screenshots/ip_traffic2.png)

# Secure Server Access
* Connected to EC2 instances using SSH via:

  * Local system terminal
  ![Local Terminal SSH](screenshots/local_ssh.png)
  
  * AWS CloudShell
  ![CloudShell SSH](screenshots/cloud_ssh.png)
  
# Testing & Validation

* Simulated instance failure and confirmed automatic replacement
* Verified load balancer health checks
* Confirmed secure access control using IAM policies

---

# Outcome

By completing this project, I gained practical experience in:

* Building fault-tolerant cloud infrastructure
* Applying AWS security best practices
* Designing scalable systems
* Managing cloud resources using the AWS Management Console

---

# Author

**Ekene Iyala Franklyn**
Aspiring Cloud Engineer | AWS Fundamentals

---

# Tags

`AWS` `Cloud Engineering` `EC2` `IAM` `Auto Scaling` `Load Balancer` `DevOps`
