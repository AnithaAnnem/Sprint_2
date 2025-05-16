
![image](https://github.com/user-attachments/assets/4e795c3d-64b8-433d-9c4c-906ef7249876)


# DevOps Repositories Setup Guide


|**Author**        | **created on**       | **Version** |**Last edited on**| **Review Level**   | **Reviewer**      |
|---------------|------------|---------|--------|--------|----------------------|
| Anitha Annem  | May 15  | v1.0|  May 16    | Pre-Reviewer   | Priyanshu            |
| Anitha Annem  |  |  |   | L0             | Khushi Malhothra    |
| Anitha Annem  |      |      |         | L1             | Mukul Joshi       |
| Anitha Annem  |      |      |         | L2             | piyush Upadhyay      |



# Table of Contents

1. [Introduction](#introduction)
2. [Pre-requisites](#pre-requisites)
3. [Step-by-Step Setup Guide](#step-by-step-setup-guide)
   - [1. Create DevOps Repositories](#1-create-devops-repositories)
   - [2. View Created Repositories](#2-view-created-repositories)
4. [Conclusion](#conclusion)
5. [Contact Information](#contact-information)
6. [References](#references)




# Introduction
This document provides a comprehensive guide to setting up DevOps repositories from scratch and preparing a demonstration for reviewers. The objective is to establish source control, continuous integration, and continuous deployment pipelines using a standard DevOps repository structure.

# Pre-requisites

Before starting, ensure:

- Git is installed (`git --version`)
- Access to GitHub or an equivalent VCS platform
- You have the necessary permissions to create repositories

# Step-by-Step Setup Guide

##   1. Create DevOps Repositories

Create the following repositories in your GitHub organization:

| Repository Name       | Purpose                                           |
|-----------------------|---------------------------------------------------|
| `ci-cd-pipeline`      | Stores Jenkins/GitHub Actions pipelines           |
| `terraform-repo`      | Infrastructure-as-Code using Terraform            |
| `monitoring-repo`     | Configuration for Prometheus, Grafana, and logs   |
| `ansible`             | Configuration management using Ansible            |

**Screenshot: Creating `ci-cd-pipeline` Repository**  

![image](https://github.com/user-attachments/assets/623af62b-8324-4ede-9458-8ab0a253e3a6)

##    2. View Created Repositories

Once all repositories are created, verify them in the GitHub organization dashboard.

  **Screenshot: Repositories in Organization**  

![image](https://github.com/user-attachments/assets/3048d2ac-3698-44c9-8e67-3cf879345804)



# Conclusion
This document outlined the structured setup of DevOps repositories within a GitHub organization, ensuring a modular and scalable approach to CI/CD, infrastructure automation, configuration management, and monitoring. By organizing your DevOps assets into dedicated repositories—such as ci-cd-pipeline, terraform-repo, monitoring-repo, and ansible—you enable better collaboration, maintainability, and security.

# Contact Information 
| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|


# References
| **Link** | **Description**            |
|----------|-------------------------------|
|[GitHub Documentation](https://docs.github.com/)| Comprehensive guide on repository creation and management.|
|[Terraform Documentation](https://developer.hashicorp.com/terraform/docs) | Detailed reference for infrastructure as code setup using Terraform.|
|[Ansible Documentation](https://docs.ansible.com/)| Official guide for configuration management with Ansible.|
| [Prometheus Documentation](https://prometheus.io/docs/) | Resources for monitoring system setup and rules. |
| [Grafana Documentation](https://grafana.com/docs/) | Insights on creating dashboards and integrating with Prometheus.|

