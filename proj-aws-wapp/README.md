# aws-high-traffic-web-app
This repository contains Terraform configurations and scripts for deploying a scalable, high-traffic web application on AWS using EC2, ELB, ASG, API Gateway, Step Functions, Cognito, Lambda, and DynamoDB. The architecture ensures high availability, scalability, and security for handling up to 5000 concurrent requests.


### Repository Description for AWS High-Traffic Web Application

**Repository Name:** `aws-high-traffic-web-app`

**Description:** 

This repository contains the Terraform configuration files and necessary scripts to deploy a scalable, high-traffic web application on AWS. The architecture leverages various AWS services, including EC2, Elastic Load Balancer (ELB), Auto Scaling Group (ASG), API Gateway, Step Functions, Cognito, Lambda, and DynamoDB, to ensure high availability, scalability, and security. 

### Detailed Description
# AWS High-Traffic Web Application

This repository contains Terraform configurations for deploying a high-traffic web application on AWS. The architecture includes EC2 instances, ELB, ASG, API Gateway, Step Functions, Cognito, Lambda, and DynamoDB.

## Directory Structure

```plaintext
aws-high-traffic-web-app/
├── main.tf
├── variables.tf
├── outputs.tf
├── modules/
│   ├── vpc/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   ├── outputs.tf
│   ├── ec2/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   ├── outputs.tf
│   ├── elb/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   ├── outputs.tf
│   ├── asg/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   ├── outputs.tf
│   ├── cognito/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   ├── outputs.tf
│   ├── apigateway/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   ├── outputs.tf
│   ├── stepfunctions/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   ├── outputs.tf
│   ├── lambda/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   ├── outputs.tf
│   ├── dynamodb/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   ├── outputs.tf
├── scripts/
│   ├── initial_task.py
│   ├── manual_verification.py
├── README.md

**Features:**
- **EC2 Instances**: Hosts the web application to handle user requests.
- **Elastic Load Balancer (ELB)**: Distributes incoming traffic across multiple EC2 instances, ensuring load balancing and high availability.
- **Auto Scaling Group (ASG)**: Automatically scales the number of EC2 instances based on the traffic load to maintain performance.
- **Amazon API Gateway**: Exposes a RESTful API to interact with the booking system.
- **AWS Step Functions**: Manages complex, long-running booking workflows.
- **AWS Lambda**: Executes serverless functions to handle various stages of the booking process.
- **Amazon DynamoDB**: Provides a highly available NoSQL database to store booking details.
- **AWS Cognito**: Manages user authentication and authorization, securing the API endpoints.

**Directory Structure:**
- **main.tf**: The main Terraform configuration file that ties all modules together.
- **variables.tf**: Defines variables used across the Terraform configuration.
- **outputs.tf**: Specifies output values from the Terraform configuration.
- **modules/**: Contains individual Terraform modules for each component.
  - **vpc/**: Manages VPC, subnets, and security groups.
  - **ec2/**: Configures EC2 instances and launch configurations.
  - **elb/**: Sets up the Elastic Load Balancer and target groups.
  - **asg/**: Manages the Auto Scaling Group.
  - **cognito/**: Handles user authentication with AWS Cognito.
  - **apigateway/**: Exposes the booking workflow as a secure API.
  - **stepfunctions/**: Manages the booking workflow using Step Functions.
  - **lambda/**: Configures Lambda functions for handling booking processes.
  - **dynamodb/**: Sets up the DynamoDB table for storing booking details.
- **scripts/**: Contains the Python scripts for the Lambda functions.

**Setup Instructions:**
1. **Clone the Repository:**
   ```sh
   git clone https://github.com/your-username/aws-high-traffic-web-app.git
   cd aws-high-traffic-web-app
   ```

2. **Initialize Terraform:**
   ```sh
   terraform init
