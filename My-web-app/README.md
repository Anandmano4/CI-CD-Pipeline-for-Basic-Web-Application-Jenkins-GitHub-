# Basic Web Application CI/CD Pipeline with Jenkins & GitHub

## Overview
This project demonstrates how to set up a Continuous Integration / Continuous Deployment (CI/CD) pipeline using **Jenkins** and **GitHub** for a basic web application.

The pipeline:
- Clones the GitHub repository.
- Installs dependencies.
- Runs tests.
- Builds the application.
- Deploys the application to a server.

## Prerequisites
- **Jenkins** running on a server (or locally).
- **Node.js** installed on Jenkins (via NodeJS Plugin).
- **GitHub** repository with the source code.
- Webhook configured in GitHub to trigger Jenkins on code pushes.

## Steps to Set Up

### 1. Install Jenkins
- [Install Jenkins](https://www.jenkins.io/doc/book/installing/) and configure necessary plugins.
- Install the following plugins:
  - GitHub Plugin
  - NodeJS Plugin
  - Pipeline Plugin

### 2. Create a GitHub Repository
- Create a repository on GitHub and push the source code of your basic web application.

### 3. Configure Jenkins Pipeline
- Create a `Jenkinsfile` in the root of the project directory.
- The `Jenkinsfile` contains the CI/CD pipeline logic for Jenkins.

### 4. Set Up Webhook
- Add a webhook in GitHub that triggers Jenkins on every push.
- URL for Jenkins webhook: `http://<your-jenkins-url>/github-webhook/`.

### 5. Run the Pipeline
- Trigger the pipeline by pushing code to GitHub.
- Jenkins will automatically start the pipeline, run tests, and deploy the application (if configured).

## Sample Commands
- To start Jenkins, use the following command (if running locally):
  ```bash
  java -jar jenkins.war
