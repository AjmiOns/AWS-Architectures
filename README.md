# AWS Architectures ☁️

**Designing, Understanding, and Documenting Cloud Solutions on Amazon Web Services**

A technical learning repository dedicated to exploring AWS architectures, understanding cloud infrastructure components, and documenting how AWS services work together to build secure, scalable, highly available, and cost-efficient solutions.

---

## 📌 Overview

This repository brings together AWS architecture diagrams, infrastructure design notes, technical explanations, and practical cloud projects.

Its purpose is to connect theoretical cloud computing concepts with real-world architectural decisions, helping learners understand not only **which AWS services to use, but also why, when, and how to use them.**

The repository is intended to evolve as new architectures, diagrams, and hands-on experiments are added.


🎯 Objectives

Understand the fundamentals of AWS cloud architecture.

Explore how AWS services communicate and integrate.

Design architectures that support scalability and high availability.

Apply security best practices and the principle of least privilege.

Understand networking, compute, storage, databases, and application delivery.

Explore infrastructure automation and Infrastructure as Code (IaC).

Evaluate architectural trade-offs involving performance, reliability, security, and cost.

Build a documented portfolio of cloud infrastructure projects.

---
🏗️ Core AWS Architecture Components

Category

AWS services

Main purpose

Compute

Amazon EC2, AWS Lambda, Amazon ECS, Amazon EKS

Run applications and workloads

Storage

Amazon S3, Amazon EBS, Amazon EFS

Store objects, block data, and shared files

Networking

Amazon VPC, Subnets, Route Tables, Internet Gateway, NAT Gateway

Connect and isolate cloud resources

Load Balancing

Elastic Load Balancing (ALB/NLB)

Distribute incoming traffic

Databases

Amazon RDS, Amazon Aurora, Amazon DynamoDB

Store and manage application data

Content Delivery

Amazon CloudFront, Amazon Route 53

Deliver content and manage DNS routing

Security

AWS IAM, AWS KMS, AWS WAF, AWS Secrets Manager

Manage permissions, encryption, and protection

Monitoring

Amazon CloudWatch, AWS CloudTrail

Monitor resources and record activity

Automation

AWS CloudFormation, AWS CDK, Terraform

Provision and manage infrastructure as code

Messaging

Amazon SQS, Amazon SNS, Amazon EventBridge

Enable asynchronous and event-driven communication

These services represent the technologies covered or targeted by this learning repository, not necessarily services already implemented.


🧩 Architecture Patterns to Explore

1. Basic Web Application

A foundational architecture for hosting a web application on AWS.

Typical components:

Amazon Route 53 for DNS.

Amazon EC2 for application hosting.

Security Groups to control network traffic.

Amazon EBS for instance block storage.

Amazon CloudWatch for monitoring.

Key concepts: Compute, networking, security groups, public access, and application hosting.

2. Highly Available Web Application

An architecture designed to reduce downtime by distributing resources across multiple Availability Zones.

Typical components:

Amazon VPC with public and private subnets.

Application Load Balancer.

EC2 instances in an Auto Scaling group.

Amazon RDS with Multi-AZ deployment.

Amazon CloudWatch alarms.

Key concepts: High availability, redundancy, fault tolerance, health checks, and automatic scaling.

3. Serverless Application

An application architecture that minimizes direct server management.

Typical components:

Amazon API Gateway.

AWS Lambda.

Amazon DynamoDB.

Amazon S3.

Amazon CloudWatch.

Key concepts: Event-driven computing, managed services, automatic scaling, and pay-per-use pricing.

4. Secure VPC Architecture

A network design that separates internet-facing resources from internal application and database resources.

Typical components:

Public and private subnets.

Internet Gateway and, where appropriate, NAT Gateway.

Route Tables and Security Groups.

Network ACLs.

IAM roles and policies.

VPC endpoints where suitable.

Key concepts: Network segmentation, controlled connectivity, private resources, and least-privilege access.

5. Containerized Application

An architecture for deploying applications packaged as containers.

Typical components:

Amazon ECS or Amazon EKS.

Amazon ECR for container images.

Application Load Balancer.

IAM roles.

Amazon CloudWatch.

Key concepts: Container orchestration, image registries, service discovery, scaling, and deployment management.

The patterns above are reference designs and learning objectives. Each should be linked to its own diagram or implementation when added to the repository.
