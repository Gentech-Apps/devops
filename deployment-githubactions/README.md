# DevOps CI/CD Pipelines with GitHub Actions

This repository provides sample CI/CD pipelines using **GitHub Actions** for deploying applications to various **AWS services**. Each workflow automates building, testing, and deploying applications following best practices.

---

## Overview

### Included Pipelines

1. **Elastic Beanstalk Deployment**  
   Deploys web applications to AWS Elastic Beanstalk.  
   - **Workflow File**: `cicd-githubactions-aws-elasticbeanstalk.yml`  
   - **Secrets Required**:  
     - `AWS_ACCESS_KEY_ID`  
     - `AWS_SECRET_ACCESS_KEY`  
     - `EB_APPLICATION_NAME`  
     - `EB_ENVIRONMENT_NAME`  

2. **Kubernetes Deployment on EKS**  
   Deploys containerized applications to an Amazon EKS cluster.  
   - **Workflow File**: `cicd-githubactions-aws-k8s.yml`  
   - **Secrets Required**:  
     - `AWS_ACCESS_KEY_ID`  
     - `AWS_SECRET_ACCESS_KEY`  
     - `EKS_CLUSTER_NAME`  
     - `ECR_REPOSITORY`  

3. **ReactJS Deployment to S3 and CloudFront**  
   Deploys a ReactJS application to S3 with CloudFront for CDN.  
   - **Workflow File**: `cicd-githubactions-aws-reactjs.yml`  
   - **Secrets Required**:  
     - `AWS_ACCESS_KEY_ID`  
     - `AWS_SECRET_ACCESS_KEY`  
     - `AWS_S3_BUCKET_NAME`  
     - `AWS_CLOUDFRONT_DISTRIBUTION_ID`  

4. **Static File Hosting on S3**  
   Deploys static files or websites to an S3 bucket.  
   - **Workflow File**: `cicd-githubactions-aws-s3.yml`  
   - **Secrets Required**:  
     - `AWS_ACCESS_KEY_ID`  
     - `AWS_SECRET_ACCESS_KEY`  
     - `AWS_S3_BUCKET_NAME`  

5. **Tag-Based Deployment**  
   Automates deployments triggered by Git tags.  
   - **Workflow File**: `cicd-githubactions-aws-tagdeployment.yml`  
   - **Secrets Required**: Varies by deployment target.

---

## How to Use

### 1. Clone the Repository
```bash
git clone https://github.com/your-repo-name/devops-samples.git
cd devops-samples
