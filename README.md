# CloudMart — Services

## Project Description

Parent repository grouping the three business microservices of the CloudMart capstone: product, order and user management. Each runs behind a regional Managed Instance Group with autoscaling and health-check-based autohealing, and is reached only through the API Gateway in [CloudMart-Platform](https://github.com/vihanapathum/CloudMart-Platform).

| Submodule | Role | Port | Database |
| --- | --- | --- | --- |
| [cloudmart-product-service](https://github.com/vihanapathum/cloudmart-product-service) | Product catalog + image upload | 8081 | Cloud SQL (MySQL) + Cloud Storage |
| [cloudmart-order-service](https://github.com/vihanapathum/cloudmart-order-service) | Order management | 8082 | MongoDB + Firestore (audit log) |
| [cloudmart-user-service](https://github.com/vihanapathum/cloudmart-user-service) | Customer records | 8083 | Cloud SQL (MySQL) |

## Technology Stack

- Java 25, Spring Boot 4.0.7, Spring Cloud 2025.1
- Managed Instance Groups with autoscaling on GCE, PM2 process management

## Setup / Getting Started

This repo uses git submodules:

```bash
git clone --recurse-submodules https://github.com/vihanapathum/CloudMart-Services.git
```

See each submodule's own README for build and run instructions.

## Student Information

- **Student Name:** A.G.Vihana Pathum Piyasiri
- **Student Number:** 2301692038
- **Slack Handle:** vihana_piyasiri
- **GCP Project ID:** project-1023ef7b-f75c-4e17-ab5

---

_Deployed and verified on GCP: 2026-09-30._
