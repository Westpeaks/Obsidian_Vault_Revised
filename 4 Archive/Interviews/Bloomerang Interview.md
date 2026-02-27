# Overview

- Bloomerang helps small and medium sized nonprofits find donors and streamline giving through their platform. 

- The platform is a management CRM and tool suite used to acquire and manage donors effectively.

- They provide:
	- **Donor CRM** - 360-degree view of supporters
	- **Fundraising Tools** - Online giving, donation forms, peer-to-peer fundraising
	- **Volunteer Management** - Recently integrated
	- **Email Marketing & Communications**
	- **Analytics & Reporting**
	- **Payment Processing** (Bloomerang Payments)

## **Tech Stack & Infrastructure**

Based on the job postings and documentation, here's what you should know:

**Cloud & Infrastructure:**

- AWS cloud infrastructure with ECS and Fargate, potentially Kubernetes within EKS or GKE 
- Modern web technologies including .NET Framework, Node.js, and React 

**DevOps Tools They Use:**

- Configuration management tools like Ansible, Chef, or Puppet, and Infrastructure as Code expertise with Terraform or CloudFormation 
- Production-level containerization and orchestration experience required 
- REST API and Bloomerang.js for integrations 
- Zapier integrations connecting to 7,000+ other apps 

**Integrations:**

- Mailchimp, PayPal, Gmail, Google Forms, and various nonprofit tools

# Experience

**What I have had experience in:**

- Linux
- Containerization (Docker, Podman)
- Terraform - 3 projects including recent AWS project
- Bash
- AWS - 2 projects
- React - 2 projects
- Rest APIs - years of experience
- Zapier
- Kubernetes - building homelab now. Going to run K8s with two worker nodes. Currently working on configuring it with FluxCD and GitOps.  
- CI/CD Pipelines via GitLab

**What I need experience in:**
## Ansible

 - **Core Definition:** Ansible is an open-source IT automation tool used for configuration management, application deployment, and orchestration. It allows you to automate repetitive tasks like software installation, system configuration, and infrastructure provisioning across multiple servers simultaneously.

- **How It Works:** Ansible uses a simple, agentless architecture - meaning you don't need to install any software on the machines you're managing. It connects to your servers via **SSH** (Linux) or WinRM (Windows) and executes tasks using "playbooks" written in **YAML**, which is a human-readable data format. This makes it easy to read, write, and understand automation scripts even if you're not a programmer.

**I have had experience with deployment via YAML using GitLab for deployments. This will translate to YAML** 

## Amazon ECS (Elastic Container Service)

**What It Is:** ECS is AWS's native container orchestration service that allows you to run and manage Docker containers at scale. Think of it as AWS's proprietary solution for deploying, managing, and scaling containerized applications without having to manage the underlying orchestration infrastructure yourself.

**How It Works:** You define your application as a "task definition" (which containers to run, CPU/memory requirements, networking, etc.), and ECS handles the scheduling and placement of those containers across a cluster of EC2 instances or Fargate. It integrates deeply with other AWS services like load balancers, IAM for security, CloudWatch for monitoring, and ECR (Elastic Container Registry) for storing your container images.

## AWS Fargate

**What It Is:** Fargate is a serverless compute engine for containers that works with both ECS and EKS. The key concept is that you don't manage any servers at all - you just define your container requirements (CPU, memory) and AWS handles everything else behind the scenes.

**How It Works:** Instead of provisioning and managing EC2 instances to run your containers, Fargate automatically provisions the right amount of compute resources. You pay only for the resources your containers actually use (per-second billing based on vCPU and memory). AWS handles patching, scaling, and server management completely, so you can focus purely on your application.

## Amazon EKS (Elastic Kubernetes Service)

**What It Is:** EKS is AWS's managed Kubernetes service. Kubernetes is the industry-standard, open-source container orchestration platform originally developed by Google. EKS runs Kubernetes in the AWS cloud while AWS manages the Kubernetes control plane (master nodes) for you.

**How It Works:** EKS provides a fully managed Kubernetes control plane that's highly available across multiple AWS availability zones. You can run your worker nodes (where containers actually run) on EC2 instances or on Fargate. Since it's standard Kubernetes, you can use all the same tools, APIs, and workflows you'd use with Kubernetes anywhere else, making it portable and avoiding vendor lock-in.

**I do not have cloud experience with containerization and Kubernetes and wouls be excited for the opportunity to learn professionally.**

## Questions

 1. What is the team size?
2. What are the core values of the DevOps team at Bloomerang? 
3. How does the team support each other? How is communication valued?  
4. What would you want to see from someone coming onto this team in the first 30 days? 
5. How do you measure performance for the team?
6. What are the most common challenges the team is facing at the moment?

## Notes

- Bloomerang is in the process of moving their windows on-prem solution to the cloud using AWS ECS, EKS, and Fargate. 

# Questions for Interview

- _Give me an example of working with a team in charge of creating a new vision and strategy.
  
  **Ex.** Starting the support department a Illuminate. Support KB at Zoom. 
  
- _Tell me about a time you took a job or assignment that required new or different skills_
  
  **Ex.** Starting a Zoom. Building a support department and what support would look like at Softek Illuminate.

- _Describe a time when a mistake or failure directly led to a successful solution_ 
  
  **Ex:** homelab nextcloud storage. Tweaking and monitoring in Grafana to maintain site health. Project included scraping new data and implementing new feeds, developing for an on rotation first responder, displaying sites in a feed and having them rotate on a queue.   

## Links:

2025111835