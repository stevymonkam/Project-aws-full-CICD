# AWS-Full-CICD-Pipeline Project

## Lab 3: Implementing CI/CD in AWS with AWS CodeCommit, CodeDeploy, and CodePipeline

![](AWS%20CICD.drawio.png)

### Scenario
A company specializing in online sales wants to automate the deployment of its web application to improve efficiency and reduce human errors. Currently, the deployment process is manual, leading to delays, frequent errors, and a lack of visibility into production versions. To address these issues, the company hires an AWS Cloud Engineer to design and implement a complete CI/CD pipeline on AWS.

### Objectives
- Automate Continuous Integration (CI) to ensure that each code modification is automatically tested and validated.
- Automate Continuous Deployment (CD) to allow smooth and uninterrupted application deployment in the production environment.
- Ensure the security, scalability, and resilience of the CI/CD pipeline.

**Project proposed by Lahda Biassou Alphonsine**  
**Costs:** Free tier  
**Estimated completion time:** 45 minutes  

## Solution Architecture

## Implementation Steps

### Step 1: Download HTTPS Git Credentials for AWS CodeCommit via the IAM console
1. Click on "Users" in the left menu, then select your user and go to "Security credentials."
2. Scroll down to "HTTPS Git credentials for AWS CodeCommit" and click on "Generate Credential."

### Step 2: Create a CodeCommit Repository
1. Open the Amazon CodeCommit console and choose to create a repository.
2. On the "Create Repository" page, enter a name for your repository (e.g., `EAZYrepo`) and select "Create."
3. On the next screen, click "Copy" next to "Step 3: Clone the Repository."

### Step 3: Add Sample Code to Your CodeCommit Repository
1. Run the following command to clone the repository, replacing `<GIT Clone Address>` with the copied address:
   ```bash
   git clone <GIT Clone Address>
   ```
2. Enter the IAM HTTPS Git Credentials username and password that were downloaded earlier.

### Step 4: Create an EC2 Deployment Server
1. Open the Amazon EC2 console.
2. Choose "Instances" > "Launch Instances."
3. Name the instance `MyCodePipelineDemo`.
4. Select "Amazon Linux 2 (HVM)" AMI.
5. Choose instance type `t2.micro`.
6. Configure security groups and IAM roles as needed.
7. Launch the instance.

### Step 5: Create a Deployment in CodeDeploy
- Create an Application
- Create a Deployment
- Create an IAM Role for CodeDeploy
- Create a Deployment Group

### Step 6: Create and Configure the Pipeline with CodePipeline

## Cleanup
To avoid unnecessary costs, delete all created AWS resources after completing the lab.

**Congratulations! You have successfully implemented a CI/CD pipeline in AWS.**
