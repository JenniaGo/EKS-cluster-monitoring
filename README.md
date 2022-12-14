# EKS-Cluster-Monitoring

### Summary:
Create EKS cluster using Terraform and monitor kubernetes status (version, states, endpoint) using AWS SDK for Python (boto3)

===================

### Step one
clone repo and enter credentials in terraform/vpc.tf (can use file config or hardcoded keys adn token) and chose region
  
      provider "aws" {
      region = "eu-west-2"
      access_key = ""
      secret_key = ""
      token= ""
      }

### Step two
Check syntax and init terraform

      terraform plan
      terraform init
      
If all good and no errors - apply

     terraform apply -auto-approve

### Step three
Check your new eks cluster with the script

      python3 eks-get-status.py
      
done, now you can customize and schedule it for your use
