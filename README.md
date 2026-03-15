# Packer AMI Build and Deployment with GitHub Actions 
This repository demonstrates how to build Amazon Machine Images (AMIs) using Packer and deploy them across multiple AWS accounts and regions using GitHUb Actions. We utilized **IAM access keys** from the main AWS account for authentication.

## Step 1: Create Main Administrator Access Keys

1. Log in to your **AWS Control Tower** management account.
2. Navigate to **IAM (Identity & Access Management)**.
3. Create a new IAM user with administrator access.
4. Generate and download the **Access Key ID** and **Secret Access Key**.

## Step 2: Add AWS Credentials to GitHub Secrets

1. Go to your GitHub repository settings.
2. Navigate to **Settings > Secrets and variables > Actions.**
3. Click on **New repository secret** and add the following secrets: ( AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY_ID)
4. Ensure these secrets are available in your GitHub Actions workflow.

## Step 3: Configure Accounts and Regions

1. Update your configuration files to include the AWS accounts and regions where you want to deploy the AMIs.
2. Customize the AWS regions and accounts according to your requirements.

## Step 4: Run the GitHub Actions Workflow

1. Push changes to the repository or manually trigger the workflow.
2. The workflow will build the AMIs using Packer and distribute them across the specified regions and accounts.
3. Note that the workflow may take up to 15 minutes to complete the distribution process.

## Additional Information

- Ensure that your GitHUb Actions runners have the necessary permissions to access AWS resources.
- Review Packer and GitHub Actions documentation for more details on configuration and usage.
