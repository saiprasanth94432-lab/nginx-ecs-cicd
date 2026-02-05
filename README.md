# Nginx ECS CI/CD Pipeline

This project demonstrates an end-to-end CI/CD pipeline for a Dockerized Nginx application deployed on AWS ECS (Fargate) behind an Application Load Balancer.

## Architecture
- GitHub as source repository
- AWS CodePipeline for orchestration
- AWS CodeBuild for Docker image build
- Amazon ECR for container image storage
- Amazon ECS (Fargate) for container orchestration
- Application Load Balancer for traffic routing
- Rolling update deployment strategy

## Deployment Flow
1. Code is pushed to GitHub
2. CodePipeline triggers automatically
3. CodeBuild builds Docker image and pushes it to ECR
4. ECS service pulls the new image
5. Rolling update replaces running tasks without downtime

## Outcome
- Zero-downtime deployments
- Automated container build and deployment
- Scalable and production-style ECS setup

## Future Enhancements
- Blue/Green deployments using CodeDeploy
- GitHub Actions as alternative CI/CD
- HTTPS with ACM and Route 53
