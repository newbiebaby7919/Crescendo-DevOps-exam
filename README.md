
# Crescendo-DevOps-Exam

## Overview
This Terraform setup provisions an AWS VPC, EC2 instance, subnets, NAT gateway, and Internet gateway. Nginx and Tomcat are installed on the EC2 instance during provisioning.

## Prerequisites
1. AWS account with necessary IAM permissions
2. Terraform installed (v1.6.0 or higher)
3. AWS CLI configured with valid credentials
4. GitHub repository named "Crescendo-DevOps-exam"

## Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/newbiebaby7919/Crescendo-DevOps-exam.git
   cd Crescendo-DevOps-exam
   ```

2. Initialize Terraform:
   ```bash
   terraform init
   ```

3. Validate the configuration:
   ```bash
   terraform validate
   ```

4. Plan the infrastructure:
   ```bash
   terraform plan
   ```

5. Deploy the infrastructure:
   ```bash
   terraform apply -auto-approve
   ```

6. Check Outputs:
   After a successful deployment, you will see the VPC ID, Subnet IDs, and EC2 Public IP.

7. Verify EC2 Setup:
   - SSH into EC2 using the public IP and your key pair:
     ```bash
     ssh -i /path/to/key.pem ec2-user@<EC2-PUBLIC-IP>
     ```
   - Check Nginx and Tomcat services:
     ```bash
     sudo systemctl status nginx
     sudo systemctl status tomcat
     ```

## Cleanup Instructions
To remove the infrastructure, run:
```bash
terraform destroy -auto-approve
```

## GitHub Actions
1. Commit and push your Terraform files to GitHub.
2. Ensure the repository has GitHub Actions configured for deployment and destruction.
3. Share the repository with GitHub users "bobcres" and "R3ymark".

## Done!
