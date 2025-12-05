---
title: "Strangers_Proposal"
date: 2024-01-01T00:00:00Z
draft: false
---


## 🐦 Proposal: Flyora – E-commerce Platform for Bird Lovers

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
![System Architecture Diagram](https://phucqb.sirv.com/Images/SystemArch.drawio.png)

#### 🧩 Frontend (Web Tier)
- **Amazon S3**: Static web hosting for frontend assets
- **CloudFront**: CDN for global content delivery
- **Responsive design**: Mobile-friendly interface



#### 🔐 Authentication & Security
- **Amazon Cognito**: User authentication and authorization
- **IAM**: Identity and access management
- **CloudWatch**: Monitoring and security layer

#### 🔄 Backend Services (App Tier)
- **Amazon API Gateway**: HTTP API management
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
- **Week 3**: Advanced services (Cognito, Bedrock, OpenSearch)
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

| Item                        | Monthly Cost | Annual Cost |Detail Calculation|
|-----------------------------|--------------|-------------|------------------|
| Amazon S3       | $0.13        | $1.56       |- Storage: 5GB <br>|
| AWS Lambda                  | $0.00        | $0.00       |- 10.000 request<br> - 512 MB Ephemeral storage <br> - 256 MB Memory <br>- Duration: 150ms|
| Amazon API Gateway(REST API)          | $0.04        | $0.48       |10.000 request|
| DynamoDB(DynamoDB on-demand capacity)                    | $0.01        | $0.12       |- Data storage size: 0.01 GB <br>- Number of writes: 0.01 million<br>- Number of reads 0.02 million |
| X-ray              | $0.01        | $0.96       |- 10.000 request <br>0- Sampling rate: 10% <br> - Traces retrieved per query: 20|
| CloudWatch & Logs           | $0.00        | $0.00       ||
| Amazon Bedrock (Embedding/LLM)| $0.13      | $1.56       |- Cohere Embed Multilingual (83%), Claude 3 Haiku (17%)<br> - 3000 request|
| Amazon RDS for PostgreSQL   | $21.01        | $252.12       | - db.t4g.micro<br> - Storage: 20GB|
| Data transfer               | $0.00        | $0.00       | - Free tier: 1 GB|
| CloudFront      | $0.11        | $1.32       |- 10000 requests<br> -Data Transfer Out: Free tier: 1 GB (global) |
| CodePipeline      | $0.00        | $0.00       |- 1 pipeline|
| CodeBuild      | $1.26        | $15.12       |- arm1.2xlarge <br> - 7 builds in a month <br> - Average build duration: 2 minutes|
| VPC      | $32.85        | $394.2       |Hourly Charge: 24h <br> Data Processing: 3000 request|
| **Total Estimate**          | **$54.34**    | **$652.92**  ||

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
- Secure user authentication and role management (Cognito, IAM)
- Scalable backend with Lambda/API Gateway
- Real-time product filtering and chatbot support
- AI-powered features via Bedrock (Embedding/LLM)
- Robust data storage with RDS, DynamoDB, and S3

#### Business Value:
- Centralized platform for bird lovers in Vietnam
- Reduced reliance on generic pet stores
- Foundation for future AI features and community expansion
- Potential for mobile app and chatbot integration

