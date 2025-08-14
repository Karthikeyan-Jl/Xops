# Terraform Xops Webserver

This project provisions an AWS VPC, public subnet, internet gateway, route table, security group, and an EC2 instance running a simple web server using Terraform.

## Steps
1. Initialize Terraform: `terraform init`
2. Apply the configuration: `terraform apply`
3. Access the web server at the public IP output.
4. Take a screenshot of the web page and save it in the `screenshots/` folder.
5. Destroy resources: `terraform destroy`

## Clean Up
Run `terraform destroy` to remove all resources.
