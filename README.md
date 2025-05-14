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



