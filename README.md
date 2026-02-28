
**Production-Ready CI/CD Pipeline on AWS with Auto Scaling & Lambda**

*📌 Project Overview*

This project implements a fully automated, production-ready CI/CD pipeline on AWS to deploy a web application securely and reliably. 
The architecture integrates GitHub for version control and uses AWS DevOps services to automate building, testing, and deployment to EC2 instances running inside a secure VPC environment.

**🏗️ Architecture Overview**



🔁 CI/CD Flow

Developer pushes code to GitHub


    .AWS CodePipeline detects changes

    .AWS CodeBuild builds the application

    .Build artifacts are stored in Amazon S3

    .AWS CodeDeploy deploys to EC2 instances

    .EC2 instances run inside an Auto Scaling Group

    .Traffic is routed via an Application Load Balancer (ALB)

    .A Lambda function performs post-deployment validation

    .CloudWatch monitors the system

    .SNS sends alerts via email


**PHASE 1 — NETWORK FOUNDATION (VPC)**

*Step 1: Create VPC*



**PHASE 2 — SECURITY SETUP**

*Step 2: Create Security Groups*


**PHASE 3 — IAM ROLES**

*Step 3: Create EC2 IAM Role*


*Step 4: Create CodeDeploy Service Role*


*Step 5: Create CodeBuild Role*


*Step 6: Create Lambda Execution Role*


**PHASE 4 — EC2 + APPLICATION SETUP**

*Step 7: Launch EC2 Instance*


*Step 8: Install CodeDeploy Agent*


** PHASE 5 — LOAD BALANCER & AUTO SCALING**

*Step 9: Create Target Group*

*Step 10: Create Application Load Balancer*


*Step 11: Create Launch Template*


*Step 12: Create Auto Scaling Group*


**PHASE 6 — S3 ARTIFACT BUCKET**

*Step 13: Create S3 Bucket*


** PHASE 7 — CODEBUILD (CI)**

*Step 14: Add buildspec.yml to GitHub repo*


*Step 15: Create CodeBuild Project*


**PHASE 8 — CODEDEPLOY**

*Step 16: Add appspec.yml to GitHub*

*Step 17: Create CodeDeploy Application*

*Step 18: Create Deployment Group*


**PHASE 9 — CODEPIPELINE**

*Step 19: Create CodePipeline*


**PHASE 10 — ADD LAMBDA**

Now we integrate Lambda for automation.

*Step 20: Create Lambda Function*


*Step 21: Add Lambda as Pipeline Stage*


**PHASE 11 — MONITORING & ALERTS**

*Step 22: Enable CloudWatch Logs*


*Step 23: Create SNS Topic*


*Step 24: Create CloudWatch Alarm*



Send notification to SNS
