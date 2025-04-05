# 🚀 E-Commerce Web Application on AWS

## 📌 Project Overview

This is a production-ready **e-commerce web application** deployed on **AWS Cloud** using **Terraform** as the Infrastructure as Code (IaC) tool. The architecture is designed to be **highly available**, **secure**, **scalable**, and **cost-efficient** – aligning with modern industry practices.

---

## 🎯 Business Use Case

This platform enables customers to:

- ✅ Browse and search for products
- ✅ Add products to cart and place orders
- ✅ Make secure payments
- ✅ Track order status and history

---

## 🧱 Architecture Summary

### ✅ Core Components

| Layer         | AWS Services Used                                      |
|---------------|--------------------------------------------------------|
| Frontend      | S3 (static files), CloudFront (CDN), Route 53          |
| Backend APIs  | ECS Fargate (containerized APIs), API Gateway          |
| Database      | RDS (PostgreSQL/MySQL), DynamoDB (for sessions/events)|
| Auth          | AWS Cognito                                            |
| Caching       | ElastiCache (Redis)                                    |
| Messaging     | SQS, SNS                                               |
| File Storage  | Amazon S3                                              |
| Security      | IAM, WAF, GuardDuty, Security Groups, KMS             |
| CI/CD         | GitHub Actions, AWS CodePipeline, Terraform            |
| Monitoring    | CloudWatch, X-Ray, Prometheus, Datadog                 |

---

## 🛠️ Features

- 🌐 Multi-AZ High Availability
- 🔐 End-to-End Security with IAM, WAF, Cognito
- ⚙️ Auto Scaling for ECS Services
- 🚀 Continuous Integration & Delivery
- 📦 Event-driven order processing with SQS + Lambda
- 💸 Cost Optimization with Spot Instances and Serverless tools

---

## 🔄 User Flow

1. User accesses the web app via CloudFront (static files from S3)
2. Authenticates using AWS Cognito
3. Browses products (via ECS API Gateway → Backend containers → RDS)
4. Adds products to cart and places order
5. Order status is processed via SQS/Lambda and stored in DynamoDB
6. Notifications are sent using SNS
7. Payments are handled via 3rd-party gateway (Stripe/PayPal)

---

## 🧾 Deployment Stack

- **Terraform** – IaC to provision AWS resources
- **Docker + ECS Fargate** – Containerized deployment
- **GitHub Actions** – CI/CD pipelines
- **AWS CodePipeline + CodeBuild** – Automated infra + app deployments

---

## 📁 Folder Structure

```bash
aws-ecommerce/
├── terraform/
│   ├── vpc/
│   ├── ecs/
│   ├── rds/
│   └── cloudfront/
├── docker/
│   ├── backend/
│   └── frontend/
├── ci-cd/
│   └── github-actions/
└── README.md
