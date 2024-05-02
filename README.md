
# AWS EC2 Instance Creation with Terraform and Infracost Demo

## Overview

This repository contains the necessary Terraform scripts to provision an AWS EC2 Instance. The process is augmented with cost analysis using Infracost, which provides a detailed breakdown of potential costs associated with the resources managed by Terraform. The workflow is triggered by a pull request to the `main` branch, ensuring that cost evaluations are automatically commented on each pull request, facilitating informed decision-making and transparency in infrastructure changes.

## Prerequisites

- AWS Account with configured access rights.
- Terraform installed on your local machine or CI/CD environment.
- An Infracost API Key, which can be generated as per the Infracost documentation.

## Secrets

Ensure the following secrets are configured in your repository or CI/CD environment:

- `AWS_ACCESS_KEY_ID`: Your AWS access key.
- `AWS_SECRET_ACCESS_KEY`: Your AWS secret key.
- `INFRACOST_API_KEY`: The API key for Infracost.

## Workflow Steps

1. **Check out the repository**: Clone the latest version of the repository to work with Terraform scripts.
2. **Install Terraform**: Ensure Terraform is installed in your environment.
3. **Initialize the Terraform directory**: Prepare your Terraform working directory for other commands.
4. **Terraform Plan**: Execute `terraform plan` to see the execution plan and ensure everything is set up correctly.
5. **Terraform Show**: Save the Terraform plan's output to a file for detailed review and debugging.
6. **Initialize the Infracost API**: Set up your environment to use the Infracost API with the provided API key.
7. **Generate Infracost JSON**: Run Infracost to generate a JSON file containing detailed cost information.
8. **Analyze Cost and Comment on PR**: Automatically comment the cost analysis results on the pull request to provide visibility into cost implications of the proposed changes.

## See Infracost in Action

With the provided Terraform script, you can see Infracost in action, providing a clear and concise breakdown of costs associated with the creation of an EC2 instance. This integration helps in managing cloud costs more effectively by providing cost insights before resources are actually deployed.



