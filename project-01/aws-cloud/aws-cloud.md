# 🏆 AWS Foundation Services - Beginner-Friendly Course Notes

This document serves as a structured, easy-to-reference guide for AWS Foundation Services, helping students revise key concepts before interviews.

---

## 1️⃣ **AWS EC2 (Elastic Compute Cloud)**

### 🔹 **Overview**
- EC2 provides resizable compute capacity in the cloud.
- Used to deploy virtual machines (instances) for applications.

### ✅ **Key Features**
- **Key Pair**: Secure authentication using SSH keys.
- **Security Group**: Acts as a virtual firewall to control inbound/outbound traffic.
- **AMI (Amazon Machine Image)**: Pre-configured OS and application packages.
- **AMI Snapshot**: Backup of an AMI.
- **Custom AMI**: Users can create their own AMI from existing instances.

### 🔄 **How It Works**
- Launch an EC2 instance from an AMI.
- Attach an EBS volume for storage.
- Configure security groups and IAM roles.
- Connect via SSH for Linux or RDP for Windows.

### 💡 **Real-World Use Cases**
- Hosting web applications.
- Running backend services.
- Development and testing environments.

### ❓ **Common Interview Questions**
1. What are the different EC2 instance types?
2. How do you secure an EC2 instance?
3. What is the difference between an AMI and an AMI Snapshot?

### 🏆 **Best Practices**
- Use IAM roles instead of storing credentials in EC2.
- Enable termination protection for critical instances.
- Use Auto Scaling for high availability.

---

## 2️⃣ **AWS EBS (Elastic Block Store)**

### 🔹 **Overview**
- Persistent block storage for EC2 instances.

### ✅ **Key Features**
- **EBS Snapshots**: Backup mechanism for EBS volumes.
- **Volume Types**:
  - **GP3, GP2**: General-purpose SSDs.
  - **IO1, IO2**: Provisioned IOPS SSDs.
  - **ST1, SC1**: Throughput and Cold HDDs.

### 🔄 **How It Works**
- Attach an EBS volume to an EC2 instance.
- Format and mount it for use.
- Create snapshots for backup.

### 💡 **Real-World Use Cases**
- Database storage.
- Boot volumes for EC2.
- Disaster recovery with snapshots.

### ❓ **Common Interview Questions**
1. What are the different EBS volume types?
2. How do you back up an EBS volume?
3. Can an EBS volume be attached to multiple EC2 instances?

### 🏆 **Best Practices**
- Use snapshots for regular backups.
- Encrypt EBS volumes for security.
- Resize volumes dynamically as needed.

---

## 3️⃣ **AWS IAM (Identity and Access Management)**

### 🔹 **Overview**
- Manages access to AWS services and resources securely.

### ✅ **Key Features**
- **Users**: Individual AWS accounts.
- **Roles**: Assign permissions without credentials.
- **IAM Profiles**: Attach roles to EC2 instances.
- **Policies**: Define permissions using JSON documents.

### 🔄 **How It Works**
- Create users and assign roles.
- Define policies with JSON syntax.
- Grant or restrict access via IAM policies.

### 💡 **Real-World Use Cases**
- Implementing least privilege access.
- Assigning roles to EC2 instances.
- Managing access to S3 buckets.

### ❓ **Common Interview Questions**
1. What is the difference between an IAM user and an IAM role?
2. How do you enforce multi-factor authentication (MFA) in IAM?
3. How do IAM policies work?

### 🏆 **Best Practices**
- Use IAM roles instead of root access keys.
- Enable MFA for all IAM users.
- Implement least privilege access.

---

## 4️⃣ **AWS Load Balancer (LB)**

### 🔹 **Overview**
- Distributes incoming traffic across multiple EC2 instances.

### ✅ **Types**
- **Application Load Balancer (ALB)**: Operates at Layer 7 (HTTP/HTTPS).
- **Network Load Balancer (NLB)**: Operates at Layer 4 (TCP/UDP).
- **Classic Load Balancer (CLB)**: Legacy load balancer.

### 🔄 **How It Works**
- Define target groups for back-end instances.
- ALB routes traffic based on HTTP rules.
- NLB provides low-latency, high-performance routing.

### 💡 **Real-World Use Cases**
- Load balancing web traffic.
- Distributing traffic to microservices.
- Providing failover and redundancy.

### ❓ **Common Interview Questions**
1. What are the differences between ALB, NLB, and CLB?
2. How does an ALB handle session stickiness?
3. How do you configure SSL termination on a Load Balancer?

### 🏆 **Best Practices**
- Use ALB for web applications.
- Use NLB for low-latency applications.
- Enable health checks for better fault tolerance.

---

## 5️⃣ **AWS Auto Scaling Group (ASG)**

### 🔹 **Overview**
- Automatically adjusts EC2 capacity based on demand.

### ✅ **Key Features**
- **Scaling Policies**: Target Tracking, Step Scaling, and Scheduled Scaling.
- **Health Checks**: Replaces unhealthy instances.
- **Load Balancer Integration**: Works with ALB/NLB.

### 🔄 **How It Works**
- Define a launch template or configuration.
- Set scaling policies.
- ASG automatically adds/removes instances based on policies.

### 💡 **Real-World Use Cases**
- Handling sudden traffic spikes.
- Ensuring high availability.
- Cost optimization by scaling down when not needed.

### ❓ **Common Interview Questions**
1. How does AWS Auto Scaling work?
2. What are the different types of scaling policies?
3. How does ASG work with Load Balancers?

### 🏆 **Best Practices**
- Use Target Tracking for automatic scaling.
- Set up health checks for better reliability.
- Optimize instance warm-up settings.

---

## 6️⃣ **AWS VPC (Virtual Private Cloud)**

### 🔹 **Overview**
- AWS VPC enables users to create isolated networks within AWS.
- Provides control over networking, security, and routing.

### ✅ **Key Features**
- **Public & Private Subnets**: Public for internet access, Private for internal services.
- **Internet Gateway (IGW)**: Allows public subnet instances to access the internet.
- **NAT Gateway**: Enables private subnet instances to access the internet securely.
- **Route Tables**: Define traffic flow between subnets.

### 🔄 **How It Works**
- Create a VPC with CIDR block.
- Add subnets (public/private).
- Attach an IGW for internet access.
- Configure security groups and route tables.

### 💡 **Real-World Use Cases**
- Hosting secure applications with internal and external communication.
- Multi-tier architecture (Web, App, Database layers).

### ❓ **Common Interview Questions**
1. What is the difference between a Public and Private Subnet?
2. How does a NAT Gateway work in a VPC?
3. Can a VPC span multiple AWS regions?

### 🏆 **Best Practices**
- Use NAT Gateway for private subnet internet access.
- Implement security groups and NACLs.
- Enable VPC Flow Logs for monitoring.

---

## 7️⃣ **AWS CloudFront (CDN)**

### 🔹 **Overview**
- CloudFront is AWS’s Content Delivery Network (CDN) service.
- Improves performance by caching content at edge locations.

### ✅ **Key Features**
- **Edge Locations**: Global network of caching servers.
- **Caching Strategies**: Controls TTL and cache invalidation.
- **HTTPS Support**: Secure content delivery.

### 🔄 **How It Works**
- CloudFront caches content from S3, EC2, or external sources.
- Requests are served from the nearest edge location.
- Reduces latency and speeds up content delivery.

### 💡 **Real-World Use Cases**
- Accelerating website load times.
- Serving video content efficiently.
- Protecting APIs with AWS Shield.

### ❓ **Common Interview Questions**
1. How does CloudFront improve performance?
2. What is the difference between CloudFront and S3 Static Website Hosting?
3. How does CloudFront handle HTTPS and SSL certificates?

### 🏆 **Best Practices**
- Enable **Origin Shield** for additional caching.
- Use **Lambda@Edge** for advanced request processing.
- Optimize caching policies to reduce costs.

---

## 8️⃣ **AWS SQS & SNS**

### 🔹 **Overview**
- **SQS (Simple Queue Service)**: Message queue for decoupling services.
- **SNS (Simple Notification Service)**: Publishes messages to multiple subscribers.

### ✅ **Key Features**
- **SQS**:
  - Standard and FIFO queues.
  - Message retention up to 14 days.
  - Dead-letter queues (DLQ) for failed messages.
- **SNS**:
  - Publishes messages to multiple endpoints (email, SMS, Lambda, SQS).
  - Supports push notifications.

### 🔄 **How It Works**
- SQS stores messages for asynchronous processing.
- SNS distributes messages to multiple subscribers.
- Works together for event-driven architecture.

### 💡 **Real-World Use Cases**
- **SQS**: Order processing, background job queues.
- **SNS**: Sending notifications, real-time alerts.

### ❓ **Common Interview Questions**
1. What is the difference between SQS and SNS?
2. How does FIFO queue work in SQS?
3. Can SNS send messages to multiple SQS queues?

### 🏆 **Best Practices**
- Enable **dead-letter queues** in SQS.
- Use **SNS filtering** to optimize message delivery.
- Configure **message encryption** for security.

---

## 9️⃣ **AWS RDS (Relational Database Service)**

### 🔹 **Overview**
- Managed relational database service for PostgreSQL, MySQL, MariaDB, SQL Server, and Aurora.

### ✅ **Key Features**
- **Automated Backups**: Point-in-time recovery.
- **Multi-AZ Deployments**: High availability setup.
- **Read Replicas**: Improves read scalability.

### 🔄 **How It Works**
- Create an RDS instance with the desired engine.
- Configure backups and replication.
- Scale up/down as needed.

### 💡 **Real-World Use Cases**
- Hosting enterprise databases.
- Scaling read-heavy applications.

### ❓ **Common Interview Questions**
1. What is the difference between Multi-AZ and Read Replicas?
2. How does RDS automate backups?
3. Can you manually scale an RDS instance?

### 🏆 **Best Practices**
- Enable **Multi-AZ** for critical applications.
- Use **parameter groups** for performance tuning.
- Encrypt database connections.
  
---

## 🔟 **AWS ACM (AWS Certificate Manager)**

### 🔹 **Overview**
- AWS ACM provides SSL/TLS certificates for secure applications.
- Simplifies certificate management and renewal.

### ✅ **Key Features**
- Free SSL/TLS certificates for AWS services.
- Automatic renewal and management.
- Integration with ALB, NLB, and CloudFront.

### 🔄 **How It Works**
- Request a certificate via ACM.
- Validate using DNS or Email.
- Attach the certificate to AWS resources.

### 💡 **Real-World Use Cases**
- Enabling HTTPS for websites hosted on AWS.
- Securing API Gateway endpoints.

### ❓ **Common Interview Questions**
1. How does ACM validate domain ownership?
2. Can ACM certificates be used outside AWS?
3. How does ACM handle certificate renewals?

### 🏆 **Best Practices**
- Use **DNS validation** for automated renewals.
- Enable **certificate transparency logging**.
- Rotate certificates regularly for security.

---

## 1️⃣1️⃣ **AWS Route 53 (DNS Service)**

### 🔹 **Overview**
- AWS Route 53 is a scalable Domain Name System (DNS) service.

### ✅ **Key Features**
- Supports **public and private DNS zones**.
- Provides **routing policies** like Simple, Weighted, Latency-based, and Geolocation.
- Offers **Health Checks** for failover.

### 🔄 **How It Works**
- Register a domain or create a hosted zone.
- Define DNS records like A, CNAME, MX, and TXT.
- Configure routing policies for high availability.

### 💡 **Real-World Use Cases**
- Managing domain names and DNS records.
- Implementing multi-region failover.

### ❓ **Common Interview Questions**
1. What are the different routing policies in Route 53?
2. How does Route 53 handle failover?
3. What is a hosted zone?

### 🏆 **Best Practices**
- Use **Alias records** for AWS services.
- Enable **health checks** for automatic failover.
- Implement **latency-based routing** for global applications.

---

## 1️⃣2️⃣ **AWS CloudFormation (CFN)**

### 🔹 **Overview**
- AWS CloudFormation provides **Infrastructure as Code (IaC)** capabilities.

### ✅ **Key Features**
- Automates infrastructure deployment.
- Uses **YAML/JSON templates**.
- Supports **parameterized templates**.

### 🔄 **How It Works**
- Define infrastructure in a CloudFormation template.
- Deploy the stack via AWS CLI, Console, or SDK.
- Manage and update resources through CloudFormation.

### 💡 **Real-World Use Cases**
- Automating AWS environment provisioning.
- Ensuring consistent infrastructure deployments.

### ❓ **Common Interview Questions**
1. What is AWS CloudFormation and why use it?
2. How does CloudFormation handle rollbacks?
3. What is the difference between a Stack and a StackSet?

### 🏆 **Best Practices**
- Use **nested stacks** for modular deployments.
- Store templates in **S3 for version control**.
- Enable **rollback protection** to prevent failures.

---

## 1️⃣3️⃣ **AWS ECR (Elastic Container Registry)**

### 🔹 **Overview**
- AWS ECR is a **private container registry** for storing Docker images.

### ✅ **Key Features**
- Fully managed **Docker image storage**.
- Integrated with **AWS IAM and ECS**.
- Supports **image vulnerability scanning**.

### 🔄 **How It Works**
- Push Docker images to ECR.
- Pull images from ECR to ECS or other AWS services.
- Manage images using lifecycle policies.

### 💡 **Real-World Use Cases**
- Storing container images securely.
- Integrating with Kubernetes and ECS.

### ❓ **Common Interview Questions**
1. How does AWS ECR compare to Docker Hub?
2. How do you authenticate Docker to AWS ECR?
3. What are lifecycle policies in ECR?

### 🏆 **Best Practices**
- Use **IAM roles** for secure access.
- Enable **image scanning** for security.
- Implement **lifecycle policies** to clean up unused images.

---

## 1️⃣4️⃣ **AWS ECS (Elastic Container Service)**

### 🔹 **Overview**
- AWS ECS provides **container orchestration** for Docker containers.

### ✅ **Key Features**
- Supports **Fargate (serverless) and EC2-based clusters**.
- Integrated with **IAM, CloudWatch, and ALB**.
- Auto Scales containers dynamically.

### 🔄 **How It Works**
- Deploy a containerized application in ECS.
- Configure ECS tasks and services.
- Scale containers based on demand.

### 💡 **Real-World Use Cases**
- Running microservices.
- Managing Kubernetes workloads.

### ❓ **Common Interview Questions**
1. What is the difference between ECS and Kubernetes?
2. How does ECS work with Fargate?
3. How do ECS tasks and services interact?

### 🏆 **Best Practices**
- Use **Fargate for serverless** workloads.
- Implement **load balancing** for container scaling.
- Monitor ECS tasks with **CloudWatch**.

---

## 1️⃣5️⃣ **AWS S3 (Simple Storage Service)**

### 🔹 **Overview**
- AWS S3 provides **scalable object storage** for any type of data.

### ✅ **Key Features**
- Multiple **storage classes** (Standard, IA, Glacier).
- Supports **versioning, encryption, and lifecycle policies**.
- **Server-side and client-side encryption** available.

### 🔄 **How It Works**
- Upload objects to S3 buckets.
- Define lifecycle policies for cost optimization.
- Secure access using IAM and bucket policies.

### 💡 **Real-World Use Cases**
- Hosting static websites.
- Storing logs and backups.

### ❓ **Common Interview Questions**
1. What are the different S3 storage classes?
2. How do S3 lifecycle policies work?
3. How do you secure an S3 bucket?

### 🏆 **Best Practices**
- Enable **encryption** for sensitive data.
- Use **lifecycle policies** for cost savings.
- Implement **S3 bucket policies** for security.

