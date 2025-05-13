# Introduction
This document provides a comprehensive guide to setting up DevOps repositories from scratch and preparing a demonstration for reviewers. The objective is to establish source control, continuous integration, and continuous deployment pipelines using a standard DevOps repository structure.

# Pre-requisites

| Category               | Requirement                                                                                          | Notes                                             |
|------------------------|------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| **Repository Access**  | [GitHub](https://github.com) / [Azure DevOps](https://dev.azure.com) / [GitLab](https://gitlab.com) / [Bitbucket](https://bitbucket.org) | Any Git-based platform account                   |
| **DevOps Tools**       | [Azure DevOps](https://azure.microsoft.com/services/devops/) / [Jenkins](https://www.jenkins.io/) / [GitHub Actions](https://github.com/features/actions) / [GitLab CI/CD](https://docs.gitlab.com/ee/ci/) | At least one CI/CD tool                          |
| **Permissions**        | Admin or contributor rights                                                                         | Required to create repos and pipelines           |
| **Git CLI**            | [Git CLI](https://git-scm.com/downloads)                                                            | Command-line Git version control                 |
| **Code Editor**        | [VS Code](https://code.visualstudio.com/) or any IDE                                                | For editing code and pipeline definitions        |
| **Docker**             | [Docker](https://www.docker.com/)                                                                   | Only if containerized workflows are needed       |
| **Terraform/Ansible**  | [Terraform](https://www.terraform.io/) / [Ansible](https://www.ansible.com/)                       | For infrastructure as code (IaC)                 |
| **Cloud Account**      | [Azure](https://portal.azure.com) / [AWS](https://aws.amazon.com/) / [GCP](https://cloud.google.com/) | Optional – for cloud-based deployments           |


