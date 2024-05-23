# Node.js Application Deployment with AWS CodeBuild and Elastic Beanstalk

This project demonstrates how to deploy a Node.js application using AWS CodeBuild for building the code and AWS Elastic Beanstalk for deployment. The deployment process is automated using AWS CodePipeline.

## Overview

The project consists of the following components:

- **Node.js Application:** A sample Node.js application that you want to deploy.
  
- **AWS CodeBuild:** A fully managed build service that compiles source code, runs tests, and produces deployable artifacts. In this project, CodeBuild is used to build the Node.js application.

- **AWS Elastic Beanstalk:** An easy-to-use service for deploying and scaling web applications and services. Elastic Beanstalk manages the deployment, from capacity provisioning, load balancing, and auto-scaling to application health monitoring.

- **AWS CodePipeline:** A continuous integration and continuous delivery (CI/CD) service that automates the build, test, and deployment phases of your release process. CodePipeline orchestrates the deployment process, triggering CodeBuild to build the application and then deploying it to Elastic Beanstalk.

## Prerequisites

Before you begin, ensure you have the following:

- **Node.js Application:** Ensure your Node.js application is structured properly and has a `package.json` file defining dependencies.

- **AWS Account:** You need an AWS account to use AWS services. Make sure you have the necessary permissions to create and manage resources like CodeBuild, Elastic Beanstalk, and CodePipeline.

## Usage

1. **Set Up AWS Resources:**
   
   - Create an Elastic Beanstalk application and environment for deploying your Node.js application.
   - Set up CodeBuild project to build your Node.js application.
   - Create an IAM role for CodePipeline with permissions to access CodeBuild and Elastic Beanstalk.

2. **Configure CodePipeline:**
   
   - Create a CodePipeline pipeline that connects your CodeBuild project and Elastic Beanstalk environment.
   - Define the source stage to pull code from your version control system (e.g., GitHub, CodeCommit).
   - Add a build stage to invoke CodeBuild to build the Node.js application.
   - Configure the deploy stage to deploy the built artifact to Elastic Beanstalk.

3. **Test and Deploy:**
   
   - Make changes to your Node.js application code and push them to your version control system.
   - CodePipeline will automatically trigger the pipeline, which will initiate the build process using CodeBuild and then deploy the application to Elastic Beanstalk.

4. **Verify Deployment:**
   
   - Access your application via the Elastic Beanstalk URL to verify that the deployment was successful.

