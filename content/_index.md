---
title: "Strangers_Proposal"
date: 2024-01-01T00:00:00Z
draft: false
---

<div style="text-align: center; margin-bottom: 2rem;">
  <img src="/images/flyora-logo.svg" alt="Flyora Logo" style="max-width: 200px; height: auto;" />
</div>

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

#### 🧩 Frontend (Web Tier)
- **Amazon S3**: Static web hosting for frontend assets
- **CloudFront**: CDN for global content delivery
- **Responsive design**: Mobile-friendly interface

#### 🔐 Authentication & Security
- **Amazon Cognito**: User authentication and authorization
- **IAM**: Identity and access management
- **CloudWatch**: Monitoring and security layer

#### 🔄 Backend Services (App Tier)
- **Amazon API Gateway**: RESTful API management
- **AWS Lambda Functions**: 
  - Chatbot handler
  - Import automation
  - API handler
- **Amazon Nova Lite (Bedrock)**: AI-powered recommendations
- **Amazon OpenSearch**: Advanced search capabilities

#### 📦 Data & Storage (Data Tier)
- **Amazon S3**: Product images and static assets
- **DynamoDB**: NoSQL database for product catalog
- **MySQL Workbench**: Database design and management

#### 🔧 CI/CD & Development
- **GitHub**: Version control and collaboration
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

| Item                  | Monthly Cost | Annual Cost |
|-----------------------|--------------|-------------|
| Amazon S3 + CloudFront| $0.20        | $2.40       |
| AWS Lambda            | $0.00        | $0.00       |
| Amazon API Gateway    | $0.01        | $0.12       |
| DynamoDB              | $0.25        | $3.00       |
| Amazon Cognito        | $0.08        | $0.96       |
| CloudWatch & Logs     | $0.05        | $0.60       |
| Amazon Bedrock (Nova) | $0.10        | $1.20       |
| OpenSearch Service    | $0.15        | $1.80       |
| CodePipeline/CodeBuild| $0.05        | $0.60       |
| **Total Estimate**    | **$0.89**    | **$10.68**  |

Hardware costs are not applicable as Flyora is a web-only platform.

---

### 7. Risk Assessment

| Risk               | Impact   | Probability | Mitigation Strategy                          |
|--------------------|----------|-------------|-----------------------------------------------|
| Lambda cold starts | Medium   | Medium      | Provisioned concurrency for critical functions|
| DynamoDB throttling| Medium   | Low         | Auto-scaling and proper partition key design  |
| Cost overruns      | Low      | Low         | Monitor with AWS Budgets and CloudWatch alerts|
| OpenSearch downtime| Medium   | Low         | Implement fallback search with DynamoDB       |

---

### 8. Expected Outcomes

#### Technical Improvements:
- Responsive, mobile-friendly UI
- Secure user authentication and role management
- Scalable backend with real-time product filtering
- Fast search and personalized recommendations (future)

#### Business Value:
- Centralized platform for bird lovers in Vietnam
- Reduced reliance on generic pet stores
- Foundation for future AI features and community expansion
- Potential for mobile app and chatbot integration

