# Jenkins Pipeline for DevOps Lab

This repository contains a Jenkins pipeline script for automating the process of building, pushing, and deploying a Dockerized application to a Kubernetes cluster.

## Pipeline Overview

The Jenkins pipeline performs the following stages:

1. **SCM Checkout**: Clones the repository from GitHub.
2. **Build Docker Image**:  Builds a Docker image for the application.
3. **Push Docker Image**:  Pushes the built Docker image to a DockerHub registry.
4. **Run Container on Dev Server**: Runs the Docker container on a development server.
5. **Deploy to Kubernetes**: Deploys the application to a Kubernetes cluster using `kubectl`.

## Pipeline Code

You can find the Jenkins pipeline code in the `DeployKubernetes` file. Here’s a brief overview of the main steps:

## How to Use

1. Ensure Jenkins is properly set up with the following plugins:
   - Git Plugin
   - Docker Plugin
   - Kubernetes Plugin

2. Configure the following credentials in Jenkins:
   - **Git credentials**: For accessing the GitHub repository.
   - **DockerHub credentials**: For pushing images to the Docker registry.
   - **Kubernetes config**: For deploying to the Kubernetes cluster.

3. Trigger the pipeline through Jenkins to automate the deployment process.
