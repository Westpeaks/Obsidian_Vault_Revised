12-31-2024 23:02

Tags: [[GitLab]] [[CI CD]] [[DevOps]] [[Cloud]] [[Fundamentals]]

# GitLab CI CD

## Pipelines, CI/CD and DevOps for Beginners

![[GLMM1.svg]]


## Pipelines

### What is a pipeline?

A series of steps that builds tests and deploys software. 

An analogy from car manufacturing:

![[carassembly.png]]


## Architecture

![[CICDbreakdown.svg]]

### What happens to artifacts after the jobs run?

- The crux of this issue comes from the fact that as each job executes (with its containers), it is destroyed as the job completes it run cycle. 
- To retain elements after the a job or jobs run, we must create artifacts. Gitlab will extract these artifacts and make them available under the **Job artifacts** in the **Build>Jobs** section. 

### Why do jobs and pipelines fail? 

![[Gitlab Exit Code.png]]
![[GitLab Exit Code 2.png]]

- Only an exit code of 0 marks a successful job. Exit codes 1-255 will indicate different types of errors. 
- An exit code will issue immediately after an error occurs. So, the last command that was executed in a job is where the error occurred. 

## What is DevOps?

DevOps is a software development methodology that integrates **software development (Dev)** and **IT operations (Ops)** to enhance collaboration, efficiency, and speed in delivering applications and services. It emphasizes breaking down silos between traditionally separate teams—such as development, operations, quality assurance, and security—by fostering a culture of shared responsibility, collaboration, and continuous improvement.

## Key Features of DevOps

1. **Cultural Philosophy**:
    
    - Promotes teamwork and shared accountability across all stages of the application lifecycle, from development to deployment and operations.
        
    - Encourages practices like "shift-left" testing and early issue detection to improve quality.
        
2. **Processes and Practices**:
    
    - Continuous Integration (CI) and Continuous Delivery (CD) enable frequent, reliable software releases.
        
    - Automation of repetitive tasks, such as testing, deployment, and infrastructure provisioning, to improve efficiency.
        
    - Use of fast feedback loops to refine processes iteratively.
        
3. **Tools and Technologies**:
    
    - DevOps relies on tools for automation (e.g., CI/CD pipelines), infrastructure as code (IaC), monitoring, and collaboration.
        
    - Popular tools include Jenkins, Docker, Kubernetes, Ansible, and Git.
        
4. **Benefits**:
    
    - Accelerates software delivery cycles.
        
    - Improves product quality by integrating testing and monitoring throughout the lifecycle.
        
    - Enhances organizational agility to respond quickly to customer needs or market changes.
        

## DevOps in Practice

Under a DevOps model, teams work across the entire application lifecycle rather than being confined to specific roles. This approach often extends to include security practices (DevSecOps) to ensure secure software delivery without compromising speed. By adopting DevOps principles, organizations can reduce time-to-market, improve reliability, and maintain a competitive edge in fast-paced industries.

![[DevOps.webp]]
## References

[GitLab CI/CD: Pipelines, CI/CD and DevOps](https://www.udemy.com/course/gitlab-ci-pipelines-ci-cd-and-devops-for-beginners/?couponCode=JUST4U02223)
