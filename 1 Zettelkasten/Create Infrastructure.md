- The Terraform process follows the Infrastructure as Code model (**IaC**).
- Essentially it can be used to deploy and take down infrastructure in your cloud platform of choice as needed. 
- In the example below, the Configuration block is deploying an EC2 instance in AWS. 

```hcl
provider "aws" {
  region = "us-west-2"
}

data "aws_ami" "ubuntu" {
  most_recent = true

  filter {
    name = "name"
    values = ["ubuntu/images/hvm-ssd-gp3/ubuntu-noble-24.04-amd64-server-*"]
  }

  owners = ["099720109477"] # Canonical
}

resource "aws_instance" "app_server" {
  ami           = data.aws_ami.ubuntu.id
  instance_type = "t2.micro"

  tags = {
    Name = "learn-terraform"
  }
}
```
## Elements Needed

- Two main elements are needed to declare a Terraform project. These are expressed in **.tf** files.
	- **terraform.tf** - This will contain and control the version of Terraform used for deployment. 
	- **main.tf** - This will contain the main configuration block. This can be thought of a the main function in coding. other .tf files can also be used within a terraform project. 

## Links:

[Create Infrastructure](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/aws-create)

[[Terraform Basics]]

2025111236