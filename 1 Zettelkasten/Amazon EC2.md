- Amazon EC2 instances are essentially cloud servers. They are VMs that can run Linux or Windows distros. 
	- With traditional on-premises resources, you must purchase hardware upfront, wait for delivery, and handle installation and configuration.
	- In contrast, with Amazon EC2, you can quickly launch, scale, and stop instances based on your needs without delays.

- Amazon handles the server segmentation at the hypervisor level.

## Launching an EC2 Instance

1. Start by selecting an Amazon machine image (**Ex.** Windows, t2micro). 
2. Then choose and image type. This will determine the provisioned hardware restraints (**Ex.** CPU, Memory, Network performance etc.).

## Connecting to the EC2 Instance

- Once the instance is launched you can use various methods of traditional connectivity (**Ex.** SSH, RDP etc.)
- In addition, AWS offers a secure and simplified method of connecting to and accessing instances. This is done through **AWS Systems Manager**.
- Once connected, the instance functions like a traditional server, you can install programs and packages accordingly.

## Scaling EC2 Instances

- **Elasticity** - elasticity is the ability to dynamically add resources in real-time based on demand. A system can rapidly scale up or scale down its resources based on the processing required for demand and decrease them when demand goes down. 
- With EC2 auto scaling you can create auto scaling groups. These groups are collections of EC2 instances that scale up or decrease based on your application's needs. This is defined by:
	- Minimum capacity
	- Desired capacity
	- Maximum capacity

## Links:

[[EC2 Instance Types]]

[[What is Needed for an EC2 Instance]]

2025111240