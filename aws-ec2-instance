terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 5.0"
    }
  }
}

# 1. Configure the AWS Provider
provider "aws" {
  region = "ap-south-1" # Mumbai Region
}

# 2. Create the EC2 Instance
resource "aws_instance" "my_first_ec2" {
  ami           = "ami-0a03139288d18e3c4" # Ubuntu 24.04 ID for Mumbai
  instance_type = "t2.micro"

  # ADDED THIS LINE: Using the Subnet ID you created in the console
  subnet_id     = "subnet-0b2dc1f1dae4e45cd"

  tags = {
    Name      = "terrafrom-with-amazonec2-instance"
    ManagedBy = "Terraform"
  }
}
