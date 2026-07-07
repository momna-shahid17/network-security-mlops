# 🛡️ Network Security System using End-to-End MLOps

<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-orange?logo=scikitlearn)
![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-green?logo=mongodb)
![MLflow](https://img.shields.io/badge/MLflow-Experiment%20Tracking-blue)
![Docker](https://img.shields.io/badge/Docker-Containerization-2496ED?logo=docker)
![AWS](https://img.shields.io/badge/AWS-Cloud-FF9900?logo=amazonaws)
![GitHub Actions](https://img.shields.io/badge/GitHub-Actions-2088FF?logo=githubactions)

### End-to-End MLOps Pipeline for Network Security Threat Detection

A production-ready Machine Learning Operations (MLOps) project that automates data ingestion, model training, experiment tracking, containerization, CI/CD, and deployment on AWS.

</div>

---

# 📌 Project Overview

This project implements a production-ready Machine Learning pipeline for Network Security Threat Detection.

The complete workflow automates:

- Data Ingestion
- Data Validation
- Data Transformation
- Model Training
- Hyperparameter Tuning
- MLflow Experiment Tracking
- DagsHub Integration
- Model Evaluation
- Batch Prediction
- AWS S3 Artifact Storage
- Docker Containerization
- GitHub Actions CI/CD
- Amazon ECR Image Registry
- Automated Deployment on AWS EC2

---

# 🚀 Features

- End-to-End MLOps Pipeline
- ETL Pipeline
- MongoDB Atlas Integration
- Data Validation
- Data Transformation
- Model Training Pipeline
- Hyperparameter Tuning
- MLflow Experiment Tracking
- DagsHub Remote Tracking
- Batch Prediction Pipeline
- AWS S3 Model Artifact Storage
- Docker Containerization
- Automated GitHub Actions CI/CD
- Amazon ECR Integration
- Self-Hosted GitHub Runner Deployment

---

# 🏗️ Project Workflow

```
Network Dataset
        │
        ▼
MongoDB Atlas
        │
        ▼
Data Ingestion
        │
        ▼
Data Validation
        │
        ▼
Data Transformation
        │
        ▼
Model Training
        │
        ▼
Hyperparameter Tuning
        │
        ▼
MLflow + DagsHub
        │
        ▼
Model Evaluation
        │
        ▼
AWS S3
        │
        ▼
GitHub Repository
        │
        ▼
GitHub Actions (CI)
        │
        ▼
Docker Image Build
        │
        ▼
Amazon ECR
        │
        ▼
Self-Hosted GitHub Runner (EC2)
        │
        ▼
Pull Latest Docker Image
        │
        ▼
Run Updated Container
        │
        ▼
Prediction API
```

---

# 📂 Repository Structure

```
network-security-mlops/

│── .github/
│   └── workflows/

│── Network_data/
│── data_schema/

│── networksecurity/
│   ├── components/
│   ├── configuration/
│   ├── constant/
│   ├── entity/
│   ├── exception/
│   ├── logging/
│   ├── pipeline/
│   └── utils/

│── templates/

│── app.py
│── main.py
│── Dockerfile
│── requirements.txt
│── setup.py
│── README.md
```

---

# 🛠️ Tech Stack

### Programming

- Python

### Machine Learning

- Scikit-learn
- Pandas
- NumPy

### Database

- MongoDB Atlas

### Experiment Tracking

- MLflow
- DagsHub

### Cloud

- Amazon EC2
- Amazon ECR
- Amazon S3

### DevOps

- Docker
- GitHub Actions
- Self-Hosted GitHub Runner

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/momna-shahid17/network-security-mlops.git

cd network-security-mlops
```

---

## Create Virtual Environment

### Windows

```bash
python -m venv venv

venv\Scripts\activate
```

### Linux

```bash
python3 -m venv venv

source venv/bin/activate
```

---

## Install Dependencies

```bash
pip install --upgrade pip

pip install -r requirements.txt
```

---

# 🔐 Environment Variables

Create a `.env` file.

```env
MONGODB_URL=<your-mongodb-connection-string>

AWS_ACCESS_KEY_ID=<your-access-key>

AWS_SECRET_ACCESS_KEY=<your-secret-key>

AWS_REGION=<your-region>

AWS_BUCKET_NAME=<your-s3-bucket>
```

---

# 🔑 GitHub Secrets

Configure the following secrets inside your GitHub repository.

| Secret Name | Description |
|-------------|-------------|
| AWS_ACCESS_KEY_ID | AWS Access Key |
| AWS_SECRET_ACCESS_KEY | AWS Secret Access Key |
| AWS_REGION | AWS Region |
| AWS_ECR_LOGIN_URI | Amazon ECR Login URI |
| ECR_REPOSITORY_NAME | Amazon ECR Repository Name |

Navigate to:

```
Repository
    ↓
Settings
    ↓
Secrets and variables
    ↓
Actions
    ↓
New Repository Secret
```

---

# ☁️ AWS EC2 Setup

Run the following commands **once** on your Ubuntu EC2 instance.

## Update Packages

```bash
sudo apt update -y
sudo apt upgrade -y
```

## Install Docker

```bash
curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh
```

## Configure Docker Permission

```bash
sudo usermod -aG docker ubuntu

newgrp docker
```

## Verify Docker

```bash
docker --version

docker ps
```

---

# 📊 MLflow

Start MLflow UI

```bash
mlflow ui
```

Open:

```
http://127.0.0.1:5000
```

---

# 🚀 Train the Model

```bash
python main.py
```

---

# 🌐 Run the Application Locally

```bash
python app.py
```

---

# 🐳 Docker & Deployment

Docker is used for containerizing the application.

The Docker image is **not built manually** during deployment.

Instead, the complete build and deployment process is fully automated using GitHub Actions.

Deployment Flow:

- Push code to the `main` branch
- GitHub Actions starts automatically
- Docker image is built
- Docker image is pushed to Amazon ECR
- Self-Hosted GitHub Runner on EC2 pulls the latest image
- Existing container is replaced with the latest version
- Updated application is deployed automatically

No manual Docker build or push commands are required.

---

# 🔄 CI/CD Pipeline

The project uses GitHub Actions for Continuous Integration and Continuous Deployment.

### Continuous Integration

- Checkout Source Code
- Basic Validation
- Configure AWS Credentials
- Build Docker Image
- Push Docker Image to Amazon ECR

### Continuous Deployment

Using a Self-Hosted GitHub Runner on AWS EC2:

- Authenticate with Amazon ECR
- Pull Latest Docker Image
- Deploy Updated Container
- Clean Unused Docker Resources

Every push to the `main` branch automatically triggers the deployment pipeline.

---

# ☁️ AWS Services Used

- Amazon EC2
- Amazon ECR
- Amazon S3
- IAM

---

# 📈 Experiment Tracking

### MLflow

- Experiment Tracking
- Parameters Logging
- Metrics Logging
- Artifact Management

### DagsHub

- Remote Experiment Tracking
- Model Versioning
- Artifact Storage

---

# 🔮 Future Improvements

- Kubernetes Deployment
- Helm Charts
- ArgoCD GitOps
- Prometheus Monitoring
- Grafana Dashboard
- Model Drift Detection
- Feature Store
- Kafka Streaming

---

# 👩‍💻 Author

**Momna Shahid**

DevOps • Cloud • Kubernetes • MLOps Engineer

**GitHub**

https://github.com/momna-shahid17

**Project Repository**

https://github.com/momna-shahid17/network-security-mlops

**LinkedIn**

https://www.linkedin.com/in/momna-shahid/

---

# ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub.
