---
title: Enterprise Cloud Migration
date: 2025-01-15 10:00:00 -0600
categories: [Portfolio, Work]
tags: [work project, cloud, aws, architecture]
---

## Overview

This project involved migrating a legacy monolithic application to a microservices architecture hosted on AWS. The primary goal was to improve scalability, reduce operational costs, and enhance deployment velocity.

## Key Responsibilities

*   **Architecture Design**: Designed a serverless architecture using AWS Lambda, API Gateway, and DynamoDB.
*   **CI/CD Pipeline**: Implemented a robust CI/CD pipeline using GitHub Actions and AWS CodePipeline to automate testing and deployment.
*   **Database Migration**: Led the migration of 5TB of data from an on-premise Oracle database to Amazon Aurora PostgreSQL with minimal downtime.

## Challenges & Solutions

One of the significant challenges was handling the complex dependencies between legacy modules. We adopted the "Strangler Fig" pattern to gradually replace functionality, ensuring the system remained operational throughout the transition.

## Outcome

*   **Cost Reduction**: Reduced infrastructure costs by 40% through the use of serverless components.
*   **Performance**: Improved API response times by 60% using CloudFront caching and optimized database queries.
*   **Reliability**: Achieved 99.99% uptime post-migration.

## Technologies Used

*   AWS (Lambda, API Gateway, DynamoDB, Aurora)
*   Terraform
*   Docker
*   Python / Node.js
