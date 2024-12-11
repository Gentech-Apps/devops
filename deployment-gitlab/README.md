# 🚀 DevOps Samples with GitLab CI/CD

This repository showcases **CI/CD pipeline examples** utilizing **GitLab CI/CD** to automate building, testing, and deploying applications. These pipelines ensure **consistent deployments** and maintain high **code quality** throughout the software delivery lifecycle.

---

## 🌟 Overview

This repository demonstrates the following workflows:

### 1. **Continuous Integration (CI)**

- **Automates code builds** to verify compilation.
- **Runs unit tests** to validate functionality.

### 2. **Continuous Deployment (CD)**

- **Automates deployment** of applications to **staging** or **production** environments.

Each pipeline is defined using a `.gitlab-ci.yml` file, which outlines the necessary jobs, stages, and environment variables for the workflows.

---

## 🛠️ Pipeline Workflows

### 1. **Basic CI/CD Workflow**  
**File**: `.gitlab-ci.yml`  
**Stages**: `build`, `test`, `deploy`  
**Description**: A simple pipeline to **build**, **test**, and **deploy** an application. Suitable for basic projects.

### 2. **Deploy to Kubernetes**  
**File**: `.gitlab-ci-kubernetes.yml`  
**Stages**: `build`, `push`, `deploy`  
**Description**: Builds Docker images, pushes them to a container registry, and deploys the app to a Kubernetes cluster.  
**Required Variables**:
- `KUBERNETES_CLUSTER_NAME`
- `KUBECONFIG`
- `CONTAINER_REGISTRY_URL`

### 3. **Deploy Static Website to S3**  
**File**: `.gitlab-ci-s3.yml`  
**Stages**: `build`, `deploy`  
**Description**: Deploys static websites or assets (e.g., React or Angular apps) to AWS S3 and invalidates CloudFront cache.  
**Required Variables**:
- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `AWS_S3_BUCKET_NAME`
- `AWS_CLOUDFRONT_DISTRIBUTION_ID`

### 4. **Elastic Beanstalk Deployment**  
**File**: `.gitlab-ci-elasticbeanstalk.yml`  
**Stages**: `build`, `deploy`  
**Description**: Deploys an application to **AWS Elastic Beanstalk** using the AWS CLI.  
**Required Variables**:
- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `EB_APPLICATION_NAME`
- `EB_ENVIRONMENT_NAME`

### 5. **Tag-Based Deployment**  
**File**: `.gitlab-ci-tag-based.yml`  
**Description**: Automates deployments triggered by **Git tags**.  
**Required Variables**: Depends on the deployment target (e.g., Kubernetes, S3, Elastic Beanstalk).

---

## 📋 How to Use

1. **Clone the Repository**  
   ```bash
   git clone https://gitlab.com/your-repo-name/devops-samples.git
   cd devops-samples
