DevOps Bootstrap Stack - Version 1.0.1
Systems & Cybersecurity Engineer
Bilal - 23 years old - Master's degree in work-study program
GitHub : https://github.com/bilalgu/devops-bootstrap

***

This personal project aims to build a secure, automated, and realistic cloud infrastructure.
It serves as a technical portfolio and a learning environment to design and implement a complete DevOps workflow.

Version 1.0.1 deploys a basic service on AWS using infrastructure as code, configuration management, containerization, CI/CD and security hardening.

***

Technology Stack

| Area             | Technologies                    |
| ---------------- | ------------------------------- |
| IaaS             | AWS EC2                         |
| Provisioning     | Terraform                       |
| Configuration    | Ansible                         |
| Containerization | Docker                          |
| CI/CD            | GitHub Actions                  |
| Security         | SSH hardening + custom fail2ban |
| OS               | Ubuntu 22.04                    |

***

Steps Completed

**Step 1 - Infrastrucuture Provisioning (Terraform)**

- Automatically creates an EC2 instance with SSH key pair
- Deployed using `terraform init` and `terraform apply`

**Step 2 - Server Configuration (Ansible)**

- Installs Docker on the instance through Ansible role
- Deployment via `ansible-playbook -i inventory.ini playbook.yml`

**Step 3 - Application Deployment (Docker via Ansible)**

- Nginx container serving a static HTML page
- An Ansible role that copies Dockerfile & index.html, builds and runs the container
- Port 80 opened via Terraform aws security group

**Step 4 - Continuous Deployment (GitHub Actions)**

- Redeploys automatically (if the VM is up) and if any change is made to `configuration/ansible/**`
- Simulates a lightweight CI/CD pipeline

**Step 5 - SSH Hardening & Intrusion Protection**

- Disables root login and allows only key-based SSH authentication
- Custom fail2ban jail with EC2-specific log

***

What's Automated 

- Full provisioning with Terraform
- Server configuration with Ansible (Docker, Nginx, hardening)
- Application deployment via Docker and Ansible
- CI/CD with GitHub Actions

***

I've Learned 

- How to structure a full DevOps chain from zero to deployment
- Building reusable Ansible roles
- Writing EC2-compatible fail2ban filters
- Managing and deploying a CI/CD pipeline

***

Next Steps (V2.0)

- Increase the protection of the infrastructure and the web service
- Set up logging on infrastructure and services
- Deploy a second service and scale the infrastrucutre

***

GitHub Repository

--> Source code and full documentation :
https://github.com/bilalgu/devops-bootstrap/
