
![image](https://github.com/user-attachments/assets/6db3620c-79d6-41c4-8fde-e4f5090bf36b)


|**Author**        | **created on**       | **Version** |**Last edited on**| **Review Level**   | **Reviewer**      |
|---------------|------------|---------|--------|--------|----------------------|
| Anitha Annem  | May 08  | v1.0|  May 08    | Pre-Reviewer   | Priyanshu            |
| Anitha Annem  | May 08 |  |   | L0             | Khushi Malhothra    |
| Anitha Annem  |  May 08    |      |         | L1             | Mukul Joshi       |
| Anitha Annem  | May 08     |      |         | L2             | piyush Upadhyay      |

# Table of Contents

- [Introduction](#introduction)
- [What are AWS Service Control Policies (SCPs)?](#what-are-aws-service-control-policies-scps)
- [Why Use SCPs for Cost Optimization?](#why-use-scps-for-cost-optimization)
- [Workflow Diagram](#workflow-diagram)
- [Advantages of Using SCPs for Cost Optimization](#advantages-of-using-scps-for-cost-optimization)
- [Best Practices](#best-practices)
- [Conclusion](#conclusion)
- [Contact Information](#contact-information)
- [References](#references)

  

# Introduction

This document provides a comprehensive overview of how to use AWS Service Control Policies (SCPs) as an effective tool for cloud cost governance. It covers key concepts, benefits, best practices, and a clear step-by-step explanation of how SCPs work in conjunction with IAM policies to enforce cost controls across AWS Organizations.

# What are AWS Service Control Policies (SCPs)?
Service Control Policies (SCPs) are a feature of AWS Organizations that enable central control over the maximum available permissions for all accounts in your organization. SCPs do not grant permissions themselves but define boundaries for what services and actions IAM users and roles can perform.

# Why Use SCPs for Cost Optimization?

**Service Control Policies (SCPs)** are a powerful feature of AWS Organizations that help enforce governance and control across multiple AWS accounts. When used effectively, SCPs can play a key role in **cost optimization** by:

- **Restricting high-cost services** that are not necessary for your workloads.
- **Enforcing consistent usage policies** across accounts to maintain control over cloud resource consumption.
- **Preventing the launch of expensive instance types or services**, reducing the risk of unexpected charges.
- **Allowing only approved regions or services**, avoiding usage in regions with higher costs or compliance risks.

Implementing SCPs early in your cloud strategy helps **prevent runaway costs**, **accidental resource creation**, and **misuse of AWS services**, providing both financial and operational benefits.

# Workflow Diagram

![image](https://github.com/user-attachments/assets/43a5f789-c0e7-4135-99da-47dc9bb6c0d6)
Note: SCPs apply before IAM permissions are considered valid. If SCP denies a service/action, it cannot be used even if IAM allows it.

## Explanation:

**User/Developer Request**  
A user or developer attempts to perform an action in AWS (e.g., launching an EC2 instance, creating a resource, etc.).

**IAM Permissions Check**  
AWS evaluates the IAM policies attached to the user, group, or role to determine whether the requested action is allowed.

**SCPs at Org/OU Level Evaluated**  
In parallel, Service Control Policies (SCPs) defined at the organization or organizational unit (OU) level are evaluated. SCPs act as *guardrails*, setting boundaries on what actions are permitted across all accounts in that scope.

**Request Approved or Denied**  
For an action to be allowed, it must pass **both** the IAM policy check and the SCP evaluation. If either denies the action, it is blocked.

**Only Approved Actions Executed**  
If the action is permitted by both IAM and SCPs, it is executed. Otherwise, it is rejected before any resources are created or changed.

**Cost Control Enforced at Policy Level**  
By using SCPs to restrict access to costly services, expensive instance types, or non-approved regions, organizations can prevent unintentional or unauthorized spending—ensuring cost control is baked into the governance model.


# Advantages of Using SCPs for Cost Optimization

- **Centralized Governance**: Apply policies across multiple AWS accounts in your organization.
- **Prevent Misuse**: Block non-essential or high-cost services proactively.
- **Granular Control**: Apply policies to individual OUs or accounts for tailored optimization.
- **Audit & Compliance**: Support compliance by disallowing unapproved services.
- **Risk Reduction**: Avoid cost surprises from unmonitored or unauthorized services.

# Best Practices

- **Start with Deny Lists**  
  Deny expensive services or actions unless specifically required (e.g., allow EC2 Spot instances but restrict On-Demand unless justified).

- **Use Whitelisting Where Necessary**  
  In high-governance environments, restrict usage to a known set of approved services.

- **Limit Region Usage**  
  Allow only specific AWS regions where your business operates to avoid cross-region data transfer and rogue deployments.

- **Tag Enforcement**  
  Pair SCPs with tag policies to mandate cost allocation tagging (e.g., `Environment`, `CostCenter`) for better cost tracking and accountability.


# Conclusion 
Conclusion
AWS Service Control Policies are powerful tools for proactive cloud cost management. By controlling which services and actions are allowed across your organization, SCPs help prevent overspending and enforce a disciplined approach to cloud resource utilization. While SCPs are not a standalone solution, they form a key part of a broader cost optimization and governance strategy.

# Contact Information 
| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|

# References

| [SCP](https://www.stormit.cloud/blog/aws-scp-service-control-policy/)| Documentation followed from this link|

