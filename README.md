# Simple Web Application Deployment with Helm

This project demonstrates deploying a basic web application using Helm on Kubernetes. Helm is used for package management and deployment automation, making it easy to manage Kubernetes applications.

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Project Structure](#project-structure)
- [Setup Instructions](#setup-instructions)
- [Deployment Steps](#deployment-steps)
- [Accessing the Application](#accessing-the-application)
- [Cleaning Up](#cleaning-up)
- [Additional Notes](#additional-notes)

## Overview

This project showcases how to deploy a simple Python Flask web application on Kubernetes using Helm. The web application serves a basic "Hello, World!" message and is containerized using Docker. Helm charts are used to define and manage the Kubernetes resources required for deployment.

## Prerequisites

Before you begin, ensure you have the following installed:

- Docker
- Kubernetes cluster (e.g., Minikube, GKE, EKS)
- Helm

## Project Structure

The project has the following structure:


├── Dockerfile

├── app.py

├── requirements.txt

└── mywebapp/

├── Chart.yaml

├── charts/

├── templates/

│ ├── deployment.yaml

│ └── service.yaml

├── values.yaml

└── 
...


- **Dockerfile**: Defines how to build the Docker image for the Flask application.
- **app.py**: Python script for the Flask web application.
- **requirements.txt**: Python dependencies for the Flask application.
- **mywebapp/**: Helm chart directory containing Kubernetes manifests and configuration files.

## Setup Instructions

1. **Clone the Repository**:

   ```bash
   $ git clone <repository_url>
   $ cd simple-webapp-helm

2. **Build Docker Image**:
    
    Build the Docker image for the web application.
  
  ```
     docker build -t mywebapp .

3. **Deploy with Helm**:

    Deploy the application on Kubernetes using Helm:

   ```
     $ helm install mywebapp ./mywebapp


## Deployment steps:

### Helm Chart Configuration

- values.yaml: Edit this file to configure your application deployment settings.
- templates/deployment.yaml: Kubernetes Deployment configuration for the web application
- templates/service.yaml: Kubernetes Service configuration to expose the application.

## Verify Deployment

## Check the service to get the external IP or Port
      


