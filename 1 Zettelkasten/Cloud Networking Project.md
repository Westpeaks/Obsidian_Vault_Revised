
**1. Created a Small AWS VPC manually in the Console**

- Created a small VPC configuration
- Built a small deployment of 2 subnets with 32 available IPs (11 usable IPs each, Amazon uses the other 5)
- VPC CIDR: `10.0.0.0/27` with two `/28` subnets

**2. Set Up AWS Billing Protection**

- Configured a $20/month billing alarm using CloudWatch
- Set up SNS email notifications to alert you before overspending

**3. Deployed two EC2 Instances for Security Group Testing**

- Created a Terraform script that used my existing VPC, subnets, and security groups
- Launched 2 t2.micro instances:
    - One in the public subnet
    - One in the private subnet

**4. Worked with AWS Security Best Practices**

- The principle of least privilege
- Fixed security group rules
- Successfully SSH'd into the public EC2 instance
- From the public instance, successfully SSH'd into the private EC2 instance, Unable to reach the private EC2 unless directly in the public EC2. 

## Key Files Created

- `main.tf` - For the creation of the EC2 instances on the subnets
- `~/.ssh/aws-test-key` SSH keys needed to get into public and private subnet.

## Links:

[[]]

2025111206