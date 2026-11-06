# AWS Infrastructure Examples with Terraform

This repository contains small Terraform examples for provisioning AWS resources. Each file demonstrates a different resource; these are learning examples, not a complete production-ready infrastructure stack.

## Examples in this repository

| File | What it demonstrates | AWS region in the configuration |
| --- | --- | --- |
| `aws-ec2-instance` | An EC2 `t2.micro` instance using a specified Ubuntu AMI and an existing subnet ID | `ap-south-1` |
| `aws-iam-user` | Creating an IAM user named `username` | `us-east-1` |
| `aws-s3-bucket` | Creating an S3 bucket named `osho-rajnish` with Development tags | `us-east-1` |
| `aws-vpc` | Creating a VPC with CIDR `10.0.0.0/16` and DNS support enabled | `us-east-1` |

## Important: prepare an example before running it

The files currently do not have the `.tf` extension, which Terraform requires when loading configuration. Run one example at a time: copy the desired file into a separate working directory and rename it with a `.tf` extension (for example, `main.tf`). Do not combine these examples as-is: they use different AWS regions and are intended to be independent.

Before applying an example:

- Configure AWS credentials using your preferred secure method; do not commit credentials to this repository.
- For the EC2 example, confirm that the AMI and subnet ID exist in your AWS account and in `ap-south-1`.
- For the S3 example, replace `osho-rajnish` with a globally unique bucket name that you are authorized to use.
- Review the IAM user and VPC settings, then check the plan before creating resources.

## Run an example

From the working directory containing the renamed `.tf` file:

```bash
terraform init
terraform validate
terraform plan
terraform apply
```

When you no longer need the resources, review the proposed changes and run `terraform destroy` from that same directory. AWS resources may incur charges; check the plan and your AWS billing before applying.

## Key learning outcomes

- Define AWS resources as infrastructure-as-code using Terraform and the AWS provider.
- Configure provider regions and understand that resource identifiers, such as AMI and subnet IDs, are region- and account-specific.
- Use `terraform init`, `validate`, and `plan` to prepare and inspect changes before applying them.
- Recognize practical resource constraints, including globally unique S3 bucket names and the need to manage AWS credentials securely.
- Understand that these examples are independent starting points and need review and configuration for a particular AWS account before use.
