---
title: "Proposal"
date: 2024-01-01T00:00:00Z
draft: false
---


## 🐦 Proposal: Flyora – E-commerce Platform for Bird Lovers

📄 **[Download Full Proposal PDF](/files/Proposal%20FLYORA.pdf)**

### 1. Executive Summary
Flyora is a specialized web application designed to serve bird enthusiasts across Vietnam. It offers curated products such as bird food, toys, cages, and decorative accessories tailored to species like Chào Mào, Vẹt, Yến Phụng, and Chích Chòe. Built with modern web technologies and hosted on AWS, Flyora ensures scalability, performance, and secure access. The platform aims to become the go-to destination for bird care and ornamentation, combining e-commerce with personalization and community engagement.

---

### 2. Problem Statement
**Current Challenges**:
- No centralized platform for bird-specific products
- Generic pet stores lack species-specific recommendations
- Poor mobile responsiveness and outdated UI in existing platforms
- Limited backend scalability and search capabilities

**Proposed Solution**:
Flyora delivers a responsive, category-driven shopping experience with secure user authentication, real-time product filtering, and a scalable backend. It supports both desktop and mobile users, with future plans for AI-powered recommendations and chatbot support.

---

### 3. Solution Architecture
#### 📄 System Architecture Diagram
![System Architecture Diagram](https://phucqb.sirv.com/Images/4a27331b2b7fa421fd6e.jpg)

#### 🧩 Frontend (Web Tier)
- **Amazon S3**: Static web hosting for frontend assets
- **CloudFront**: CDN for global content delivery
- **Responsive design**: Mobile-friendly interface

#### 🔐 Authentication & Security
- **IAM**: Identity and access management
- **CloudWatch & AWS X-Ray**: Monitoring and distributed tracing

#### 🔄 Backend Services (App Tier)
#### Technical Improvements:
- Responsive, mobile-friendly UI
- Secure user authentication and role management (IAM)
- Scalable backend with Lambda/API Gateway
- **AWS Lambda Functions**: 
  - Chatbot handler
  - Import automation
  - API handler
- **Amazon Bedrock**: Embedding Model and LLM Model for AI-powered features

#### 📦 Data & Storage (Data Tier)
- **Amazon RDS for PostgreSQL**: Relational database
- **DynamoDB**: NoSQL database
- **Amazon S3**: Data storage

#### 🔧 CI/CD & Development
- **GitLab**:  Version control and CI/CD pipeline triggers
- **AWS CodeBuild**: Automated build process
- **AWS CodePipeline**: Continuous integration and deployment

---

### 4. Technical Implementation

#### Phases:
1. **AWS Learning & Setup** – Master AWS services and architecture design
2. **Development & Integration** – Build frontend and connect AWS backend
3. **Testing & Deployment** – Complete testing and production release

#### Month 1 - AWS Learning Focus:
- **Week 1-2**: AWS fundamentals (S3, Lambda, API Gateway, DynamoDB)
- **Week 3**: Advanced services (Bedrock, OpenSearch)
- **Week 4**: Architecture design and database modeling with MySQL Workbench

#### Technical Requirements:
- AWS services proficiency for serverless architecture
- Frontend development with S3 static hosting
- DynamoDB for NoSQL data management
- GitHub for version control and CI/CD integration

---

### 5. Timeline & Milestones

| Phase                    | Duration   | Key Milestones                           |
|--------------------------|------------|------------------------------------------|
| **Month 1: AWS Learning**| 4 weeks    | • AWS fundamentals mastered<br>• Architecture designed<br>• Database schema created |
| **Month 2: Development** | 4 weeks    | • Frontend UI completed<br>• Lambda functions built<br>• API Gateway configured |
| **Month 3: Integration** | 4 weeks    | • Full system integration<br>• Testing completed<br>• Production deployment |

---

### 6. Budget Estimation

| Item                                     | Monthly Cost | Annual Cost |
|------------------------------------------|--------------|-------------|
| Amazon S3 (Simple Storage Service)       | $0.15        | $1.80       |
| AWS Lambda (Serverless Compute)          | $0.00        | $0.00       |
| Amazon API Gateway (REST API Endpoints)  | $0.04        | $0.48       |
| DynamoDB (On-demand NoSQL Database)      | $0.00        | $0.00       |
| AWS X-Ray (Application Monitoring)        | $0.01        | $0.12       |
| Amazon CloudWatch (Monitoring & Logs)    | $0.00        | $0.00       |
| Amazon Bedrock (AI/LLM Services)          | $3.49        | $41.88      |
| Amazon RDS for PostgreSQL (Relational DB) | $21.01       | $252.12     |
| AWS Data Transfer (Network Traffic)       | $0.00        | $0.00       |
| Amazon CloudFront (CDN Service)          | $0.10        | $1.20       |
| AWS CodePipeline (CI/CD Automation)      | $0.00        | $0.00       |
| AWS CodeBuild (Build Service)             | $2.52        | $30.24      |
| Amazon VPC (Virtual Private Cloud)        | $43.07       | $516.84     |
| **Total Estimate**                        | **$70.39**   | **$844.68** |
| Item                        | Monthly Cost | Annual Cost |Detail Calculation|
|-----------------------------|--------------|-------------|------------------|
| Amazon S3                         | $0.15             | $1.8            | - Storage: 1GB                |
| AWS Lambda                        | $0.00             | $0.00            | - 10.000 request<br>- 512 MB Ephemeral storage<br>- 256 MB Memory<br>- Duration: 150ms |
| Amazon API Gateway (REST API)     | $0.04             | $0.48            | - 10.000 request              |
| DynamoDB (on-demand capacity)     | $0.00             | $0.00            | - Data storage size: 0.01 GB<br>- Number of writes: 0.01 million<br>- Number of reads: 0.02 million |
| X-ray                             | $0.01             | $0.12            | - 10.000 request<br>- Sampling rate: 10%<br>- Traces retrieved per query: 20 |
| CloudWatch & Logs                 | $0.00             | $0.00            |                             |
| Amazon Bedrock (Embedding/LLM)    | $3.49             | $41.88            | - Cohere Embed Multilingual (83%), Claude 3 Haiku (17%)<br>- 3.000 request |
| Amazon RDS for PostgreSQL         | $21.01            | $252.12          | - db.t4g.micro<br>- Storage: 20GB |
| Data transfer                     | $0.00             | $0.00            | - Free tier: 1 GB              |
| CloudFront                        | $0.10             | $1.2            | - 10.000 request<br>- Data Transfer Out: Free tier 1 GB (global) |
| CodePipeline      | $0.00        | $0.00       |- 1 pipeline|
| CodeBuild      | $2.52        | $30.24       |- arm1.2xlarge <br> - 14 builds in a month <br> - Average build duration: 2 minutes|
| VPC                               | $43.07            | $516.84          | - Hourly Charge: 24h<br>- Data Processing: 3.000 request <br> - 1 Nat gateway |
| **Total Estimate**          | **$70.39**    | **$844.68**  ||

Hardware costs are not applicable as Flyora is a web-only platform.

---

### 7. Risk Assessment

| Risk                   | Impact   | Probability | Mitigation Strategy                          |
|------------------------|----------|-------------|-----------------------------------------------|
| Lambda cold starts     | Medium   | Medium      | Provisioned concurrency for critical functions|
| DynamoDB throttling    | Medium   | Low         | Auto-scaling and proper partition key design  |
| RDS downtime           | Medium   | Low         | Multi-AZ deployment, automated backups        |
| Cost overruns          | Low      | Low         | Monitor with AWS Budgets and CloudWatch alerts|
| Bedrock API limits     | Medium   | Low         | Monitor usage, fallback to cached results     |

---

### 8. Expected Outcomes

#### Technical Improvements:
- Responsive, mobile-friendly, UI/UX
- Secure user authentication and role management (IAM)
- Scalable backend with Lambda/API Gateway
- Real-time product filtering and chatbot support
- AI-powered features via Bedrock (Embedding/LLM)
- Robust data storage with RDS, DynamoDB, and S3

#### Business Value:
- Centralized platform for bird lovers in Vietnam
- Reduced reliance on generic pet stores
- Foundation for future AI features and community expansion
- Potential for mobile app and chatbot integration

