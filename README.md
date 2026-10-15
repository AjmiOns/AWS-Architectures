# AWS Architectures ☁️

**Designing, Understanding, and Documenting Cloud Solutions on Amazon Web Services**

A technical learning repository dedicated to exploring AWS architectures, understanding cloud infrastructure components, and documenting how AWS services work together to build secure, scalable, highly available, and cost-efficient solutions.

---




## 📌 Overview

This repository brings together AWS architecture diagrams, infrastructure design notes, technical explanations, and practical cloud projects.

Its purpose is to connect theoretical cloud computing concepts with real-world architectural decisions, helping learners understand not only **which AWS services to use, but also why, when, and how to use them.**

The repository is intended to evolve as new architectures, diagrams, and hands-on experiments are added.

## 🎯 Objectives

- Understand the fundamentals of AWS cloud architecture.
- Explore how AWS services communicate and integrate.
- Design architectures that support scalability and high availability.
- Apply security best practices and the principle of least privilege.
- Understand networking, compute, storage, databases, and application delivery.
- Explore infrastructure automation and Infrastructure as Code (IaC).
- Evaluate architectural trade-offs involving performance, reliability, security, and cost.
- Build a documented portfolio of cloud infrastructure projects.

## 🏗️ Core AWS Architecture Components

| Category | AWS services | Main purpose |
|---|---|---|
| Compute | Amazon EC2, AWS Lambda, Amazon ECS, Amazon EKS | Run applications and workloads |
| Storage | Amazon S3, Amazon EBS, Amazon EFS | Store objects, block data, and shared files |
| Networking | Amazon VPC, Subnets, Route Tables, Internet Gateway, NAT Gateway | Connect and isolate cloud resources |
| Load Balancing | Elastic Load Balancing (ALB/NLB) | Distribute incoming traffic |
| Databases | Amazon RDS, Amazon Aurora, Amazon DynamoDB | Store and manage application data |
| Content Delivery | Amazon CloudFront, Amazon Route 53 | Deliver content and manage DNS routing |
| Security | AWS IAM, AWS KMS, AWS WAF, AWS Secrets Manager | Manage permissions, encryption, and protection |
| Monitoring | Amazon CloudWatch, AWS CloudTrail | Monitor resources and record activity |
| Automation | AWS CloudFormation, AWS CDK, Terraform | Provision and manage infrastructure as code |
| Messaging | Amazon SQS, Amazon SNS, Amazon EventBridge | Enable asynchronous and event-driven communication |

*These services represent the technologies covered or targeted by this learning repository, not necessarily services already implemented.*

## 🧩 Architecture Patterns to Explore

### 1. Basic Web Application

A foundational architecture for hosting a web application on AWS.

**Typical components:**
- Amazon Route 53 for DNS.
- Amazon EC2 for application hosting.
- Security Groups to control network traffic.
- Amazon EBS for instance block storage.
- Amazon CloudWatch for monitoring.

**Key concepts:** Compute, networking, security groups, public access, and application hosting.

### 2. Highly Available Web Application

An architecture designed to reduce downtime by distributing resources across multiple Availability Zones.

**Typical components:**
- Amazon VPC with public and private subnets.
- Application Load Balancer.
- EC2 instances in an Auto Scaling group.
- Amazon RDS with Multi-AZ deployment.
- Amazon CloudWatch alarms.

**Key concepts:** High availability, redundancy, fault tolerance, health checks, and automatic scaling.

### 3. Serverless Application

An application architecture that minimizes direct server management.

**Typical components:**
- Amazon API Gateway.
- AWS Lambda.
- Amazon DynamoDB.
- Amazon S3.
- Amazon CloudWatch.

**Key concepts:** Event-driven computing, managed services, automatic scaling, and pay-per-use pricing.

### 4. Secure VPC Architecture

A network design that separates internet-facing resources from internal application and database resources.

**Typical components:**
- Public and private subnets.
- Internet Gateway and, where appropriate, NAT Gateway.
- Route Tables and Security Groups.
- Network ACLs.
- IAM roles and policies.
- VPC endpoints where suitable.

**Key concepts:** Network segmentation, controlled connectivity, private resources, and least-privilege access.

### 5. Containerized Application

An architecture for deploying applications packaged as containers.

**Typical components:**
- Amazon ECS or Amazon EKS.
- Amazon ECR for container images.
- Application Load Balancer.
- IAM roles.
- Amazon CloudWatch.

**Key concepts:** Container orchestration, image registries, service discovery, scaling, and deployment management.

*The patterns above are reference designs and learning objectives. Each should be linked to its own diagram or implementation when added to the repository.*

## 🌐 Essential AWS Networking Concepts

Understanding networking is fundamental to designing cloud infrastructure.

- **Amazon VPC:** A logically isolated virtual network in AWS.
- **Public subnet:** A subnet whose routing allows internet connectivity through an Internet Gateway; public IP addressing and security rules are also required for direct inbound access.
- **Private subnet:** A subnet without a direct route to an Internet Gateway. Outbound internet access can be provided through a NAT Gateway when required.
- **Internet Gateway (IGW):** Enables internet connectivity for appropriately routed VPC resources.
- **NAT Gateway:** Allows resources in private subnets to initiate supported outbound connections without accepting unsolicited inbound connections through the NAT.
- **Route Table:** Determines where network traffic is directed.
- **Security Group:** A stateful virtual firewall associated with supported AWS resources.
- **Network ACL (NACL):** A stateless subnet-level traffic filter.
- **Availability Zone (AZ):** An isolated location within an AWS Region designed to support resilient infrastructure.
- **Elastic Load Balancing:** Distributes incoming traffic across registered targets.

## 🔐 Security Principles

Security should be considered at every stage of architecture design.

This repository emphasizes the following principles:

- **Least privilege:** Grant only the permissions required for a task.
- **Identity and access management:** Use IAM roles and policies to control access.
- **Network isolation:** Keep databases and internal services private whenever possible.
- **Encryption:** Protect data at rest and in transit.
- **Secrets management:** Avoid hardcoding passwords, access keys, and other sensitive information.
- **Monitoring and auditing:** Use CloudWatch and CloudTrail to observe resources and investigate activity.
- **Defense in depth:** Combine identity controls, network restrictions, encryption, and monitoring.
- **Cost-aware security:** Select appropriate controls without exposing resources unnecessarily.

Never commit AWS access keys, credentials, private keys, or sensitive configuration files to GitHub.

## 📐 AWS Well-Architected Framework

AWS architecture decisions can be evaluated against the six pillars of the AWS Well-Architected Framework:

| Pillar | Main concern |
|---|---|
| Operational Excellence | Operating, monitoring, and continuously improving workloads |
| Security | Protecting systems, identities, applications, and data |
| Reliability | Recovering from failures and maintaining availability |
| Performance Efficiency | Using resources efficiently as requirements change |
| Cost Optimization | Managing and reducing unnecessary cloud spending |
| Sustainability | Reducing the environmental impact of cloud workloads |

These pillars provide a framework for reviewing design decisions and identifying opportunities for improvement.

## 📂 Repository Structure

As the repository grows, the following structure can be used to organize its contents:

```text
AWS-Architectures/
│
├── README.md
│
├── architectures/
│   ├── basic-web-application/
│   │   ├── architecture.png
│   │   └── README.md
│   │
│   ├── highly-available-web-app/
│   │   ├── architecture.png
│   │   └── README.md
│   │
│   ├── serverless-application/
│   │   ├── architecture.png
│   │   └── README.md
│   │
│   └── secure-vpc/
│       ├── architecture.png
│       └── README.md
│
├── projects/
│   └── project-name/
│       ├── README.md
│       ├── diagrams/
│       └── src/
│
├── docs/
│   ├── networking.md
│   ├── security.md
│   └── cost-optimization.md
│
└── LICENSE
```

*This is a proposed organizational structure. Update it to match the files and directories actually present in the repository.*

## 🛠️ Tools and Technologies

Technologies that may be used to design, deploy, and document the architectures include:

- **Amazon Web Services (AWS):** Cloud infrastructure and managed services.
- **AWS Management Console:** Visual resource management.
- **AWS CLI:** Command-line infrastructure operations.
- **Python and Boto3:** AWS automation using Python.
- **Terraform / AWS CloudFormation:** Infrastructure as Code.
- **Draw.io / diagrams.net:** Architecture diagrams.
- **Git and GitHub:** Version control and project documentation.

## 🚀 How to Use This Repository

1. Browse the available architecture folders.
2. Open the architecture diagram and identify the AWS components.
3. Read the associated documentation to understand the purpose of each service.
4. Follow the request flow between components.
5. Review the networking and security configuration.
6. Examine deployment instructions or infrastructure code when available.
7. Experiment in a controlled AWS environment and clean up resources after testing.

For each architecture, the documentation should explain the use case, design decisions, traffic flow, security controls, deployment procedure, estimated costs, and known limitations.

## 💰 Cost Management

AWS resources can generate charges even when they are used for learning.

Recommended practices:

- Choose resource sizes appropriate to the workload.
- Stop or terminate unused compute resources.
- Delete temporary load balancers, NAT Gateways, and other billable resources when no longer needed.
- Use AWS Budgets and billing alerts.
- Review data transfer and storage costs.
- Check current AWS pricing before deployment.
- Never assume that a service is free simply because it is used in a learning project.

## 📚 Learning Resources

- [AWS Architecture Center](https://aws.amazon.com/architecture/)
- [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/)
- [AWS Documentation](https://docs.aws.amazon.com/)
- [AWS Solutions Library](https://aws.amazon.com/solutions/)
- [AWS Free Tier](https://aws.amazon.com/free/)
- [AWS CLI Documentation](https://docs.aws.amazon.com/cli/)
- [Boto3 Documentation](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)
- [Terraform AWS Provider](https://registry.terraform.io/providers/hashicorp/aws/latest/docs)

## 🎓 Learning Outcomes

Through the architectures documented here, the goal is to develop a stronger understanding of:

- Cloud infrastructure design and AWS service integration.
- Virtual networking and resource isolation.
- High availability, scalability, and fault tolerance.
- Cloud security and access management.
- Infrastructure automation and reproducible deployments.
- Cloud monitoring, troubleshooting, and cost management.
- Architectural trade-offs and technical documentation.

## 🤝 Contributions

Suggestions, corrections, and improvements are welcome.

If you want to contribute, open an issue to discuss the proposed change or submit a pull request with clear documentation and, where appropriate, an updated architecture diagram.

## ⚠️ Disclaimer

This repository is intended for educational and portfolio purposes. Architecture patterns are starting points rather than universal solutions. Production deployments should be reviewed against actual business requirements, security risks, service limits, regional availability, resilience objectives, and cost constraints.

## 👤 Author

**Ajmi Ons**

Cloud Infrastructure Management | AWS | Cloud Architecture | Infrastructure Automation

- GitHub: [@AjmiOns](https://github.com/AjmiOns)

---

*Learn the services. Understand the architecture. Design for security, reliability, and scale.*
