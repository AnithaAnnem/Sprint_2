
![image](https://github.com/user-attachments/assets/8b124c81-1267-4acd-9d24-58d08bfba2ef)


|**Author**        | **created on**       | **Version** |**Last edited on**| **Review Level**   | **Reviewer**      |
|---------------|------------|---------|--------|--------|----------------------|
| Anitha Annem  | May 17  | v1.0|  May 17    | Pre-Reviewer   | Priyanshu            |
| Anitha Annem  |  |  |   | L0             | Khushi Malhothra    |
| Anitha Annem  |   |      |         | L1             | Mukul Joshi       |
| Anitha Annem  |     |      |         | L2             | piyush Upadhyay      |

# Table of Contents

- [Introduction](#introduction)  
- [What is React CI & Bug Analysis?](#what-is-react-ci--bug-analysis)  
- [Why is it Important?](#why-is-it-important)  
- [Workflow](#workflow)  
- [Tools Used in CI Checks & Bug Analysis](#tools-used-in-ci-checks--bug-analysis)  
- [Tool Comparison](#tool-comparison)  
- [Advantages](#advantages)  
- [Best Practices](#best-practices)  
- [Conclusion](#conclusion)  
- [Contact Information](#contact-information)  
- [References](#references)

  

# Introduction
Continuous Integration (CI) has become a fundamental part of modern web development, especially in React applications. CI checks help maintain code quality, prevent regressions, and ensure fast feedback during development. This document focuses on React-specific CI checks and bug analysis tools, presenting their workflows, tools, and best practices.

# What is React CI & Bug Analysis?
CI in React Development
React Continuous Integration (CI) refers to the automated process of integrating code changes frequently, automatically testing and deploying them, ensuring that every change is verified.

Bug Analysis
Bug analysis includes automated and manual processes to detect, report, and track defects in code during the CI pipeline.

# Why is it Important?

- **Prevents defective code from being merged:** Automated checks catch issues before they reach production.
- **Detects regressions early in the cycle:** Continuous integration ensures new changes don’t break existing functionality.
- **Reduces manual testing overhead:** Automated pipelines handle repetitive validation tasks, saving time.
- **Improves team collaboration and deployment speed:** Developers receive quick feedback, enabling faster, safer releases.
- **Enhances code quality and user experience:** Reliable automation promotes cleaner code and a more stable product.

# Workflow
![image](https://github.com/user-attachments/assets/40a6ac96-9426-480d-b420-68a8b4ff3e6e)

### Step-by-step Explanation

**Developer Pushes Code (A)**  
The process begins when a developer pushes new code or opens a pull request to the version control system (e.g., GitHub).

**CI Tool Triggers Workflow (B)**  
The Continuous Integration (CI) tool (like GitHub Actions, CircleCI) detects the new code and automatically triggers the CI workflow to start.

**Install Dependencies (C)**  
The environment prepares itself by installing necessary dependencies (npm packages, libraries) required for the React app to build and run tests.

**Run Linting, Type Checks (D)**  
The code is analyzed for stylistic errors and potential bugs through linters (like ESLint) and type checking (like TypeScript checks). This ensures code quality and consistency.

**Run Unit & Integration Tests (E)**  
Automated tests, including unit tests (testing individual components/functions) and integration tests (testing combined parts), are executed to validate the correctness of the code.

**Build Application (F)**  
Once the code passes tests, the React application is built/compiled into a production-ready bundle.

**Deploy to Staging/Production (G)**  
The built application is deployed to a staging environment for further testing or directly to production, depending on the workflow.

**Bug Monitoring Tool Watches Runtime (H)**  
After deployment, a bug monitoring tool (like Sentry or Bugsnag) actively monitors the application in real-time, tracking runtime errors and user-impacting bugs.

**Alert + Report if Bugs Found (I)**  
If any bugs or errors occur, the monitoring tool alerts developers via email, Slack, or dashboards and provides detailed reports to facilitate quick fixes.

# Tools Used in CI Checks & Bug Analysis

| Category                    | Tools                                                 |
|-----------------------------|--------------------------------------------------------|
| **CI/CD Tools**             | GitHub Actions, CircleCI, Travis CI, GitLab CI/CD, Jenkins |
| **Bug Tracking & Analysis** | Sentry, Bugsnag, LogRocket, New Relic, Datadog         |


# Tool Comparison

| Feature               | GitHub Actions | CircleCI | Jenkins | Sentry | Bugsnag |
|-----------------------|----------------|----------|---------|--------|---------|
| **Ease of Setup**     | High           | Medium   | Low     | High   | High    |
| **Native GitHub Support** | ✅          | ❌       | ❌     | ✅     | ✅      |
| **Custom Workflows**  | ✅             | ✅       | ✅     | ✅     | ✅      |
| **Real-time Monitoring** | ❌          | ❌       | ❌     | ✅     | ✅      |
| **Free Tier Availability** | ✅         | ✅       | ✅     | ✅     | ✅      |
| **Community Support** | High           | Medium   | High   | High   | Medium  |



# Advantages

| Advantage             | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| **Automation**         | Reduces manual work, saving time and minimizing human errors.              |
| **Scalability**        | CI/CD tools grow with your codebase, supporting large teams and projects.  |
| **Early Detection**    | Bugs are caught early using tools like Sentry and Bugsnag.                 |
| **Improved Collaboration** | Promotes consistent coding practices across the team.                   |
| **Deployment Confidence** | Ensures only stable, tested code reaches production.                     |


# Best Practices

| Practice                                             | Description                                                                 |
|------------------------------------------------------|-----------------------------------------------------------------------------|
| Use code owners and required checks in PRs           | Enforces accountability and ensures all changes meet quality gates.        |
| Run linting and tests locally before pushing         | Reduces CI failures and speeds up feedback loops.                          |
| Fail fast: lint & test early in the workflow         | Detects issues early, minimizing wasted compute time.                      |
| Maintain high test coverage (80%+ recommended)       | Improves reliability and catches regressions before production.            |
| Use branch protection rules                          | Prevents unauthorized or untested code from being merged.                  |
| Integrate real-time notifications for pipeline status| Keeps the team informed of build failures or successes immediately.        |
| Include error tracking tools like Sentry post-deploy | Monitors application health and alerts teams to runtime issues.            |

# Conclusion

Based on the evaluation of features, ease of use, community support, and integration with React projects:

- **CI Checks:**  
  We recommend using **GitHub Actions** for CI checks due to its native integration with GitHub, ease of configuration, and strong community support.

- **Bug Analysis:**  
  For bug analysis, **Sentry** is recommended for its comprehensive real-time monitoring, seamless integration with React, and robust alerting system.

This combination offers a modern, scalable, and developer-friendly solution for managing React CI checks and bug analysis efficiently.



# Contact Information 
| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|

# References
| **Link** | **Description** |
|------------------------------------------------------|------------------|
| [React CI/CD](https://legacy.reactjs.org/docs/optimizing-performance.html)| For React CI/CD      |
| [Sentry for React](https://legacy.reactjs.org/docs/optimizing-performance.html)| For setting React      |




#  POC for React CI Design Bugs Analysis
##  Author Information
| Version | Last Modified | Author              | Level           | Reviewer |
|---------|----------------|---------------------|------------------|----------|
| V1      | 22-05-2025     | Harsh Wardhan Singh | Internal review | Pritam   |
| V1.1      | 23-05-2025     | Harsh Wardhan Singh | L0 | Akshit Kapil   |
- [Introduction](#-introduction)
- [Setup Instructions](#-setup-instructions)
  - [Install SonarQube Locally](#install-sonarqube-locally)
  - [Configure SonarQube Project](#configure-sonarqube-project)
  - [Install SonarScanner](#install-sonarscanner)
  - [Create `sonar-project.properties`](#create-sonar-projectproperties)
  - [Run the Analysis](#run-the-analysis)
  - [Conclusion](#conclusion)
- [Contacts](#contacts)
- [References](#references)
---
##  Introduction
This Proof of Concept (POC) demonstrates how to analyze a **React codebase using SonarQube** for detecting bugs, vulnerabilities, and code smells — **without CI tools like Jenkins, GitHub Actions, Docker, or YAML pipelines**.
---
##   Setup Instructions
###  Install SonarQube Locally
```bash
docker run -d --name sonarqube -p 9000:9000 sonarqube:lts
```
![Screenshot from 2025-05-23 20-02-59](https://github.com/user-attachments/assets/be09baef-011a-4bec-8872-9cbc472490f7)
Access the dashboard at:
`http://localhost:9000`
(Default login: `admin` / `admin`)
---
###  Configure SonarQube Project
1. Log in to the SonarQube dashboard.
2. Create a **new project**.
3. Note the **Project Key** and generate a **token** for authentication.
---
###  Install SonarScanner
```bash
# Download and extract
wget https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-5.0.1.3006-linux.zip
unzip sonar-scanner-cli-5.0.1.3006-linux.zip
sudo mv sonar-scanner-*/ /opt/sonar-scanner
# Add to PATH
export PATH=$PATH:/opt/sonar-scanner/bin
```
![Screenshot from 2025-05-23 20-03-25](https://github.com/user-attachments/assets/df1fd046-bf6f-42e0-92fd-adbaeeaa8394)
---
###  Create `sonar-project.properties`
In the root of your React project, create a file:
```properties
# sonar-project.properties
sonar.projectKey=react-ci-poc
sonar.projectName=React CI Bug Analysis
sonar.projectVersion=1.0
sonar.sources=src
sonar.language=js
sonar.sourceEncoding=UTF-8
sonar.host.url=http://localhost:9000
sonar.login=<YOUR_GENERATED_TOKEN>
```
Replace `<YOUR_GENERATED_TOKEN>` with the token you generated in the UI.
![Screenshot from 2025-05-23 20-05-08](https://github.com/user-attachments/assets/699f33db-f4e3-4463-9310-ee6951b6d1da)
---
###   Run the Analysis
```bash
sonar-scanner
```
![Screenshot from 2025-05-23 20-05-41](https://github.com/user-attachments/assets/429f750d-3365-4358-8324-3cd9e3a72f18)
This will analyze your React source files and upload the results to the SonarQube dashboard.
## You can see the bugs by the URL
```bash
http://35.173.216.15:9000/dashboard?id=react-app
```
![Screenshot from 2025-05-23 19-32-26](https://github.com/user-attachments/assets/dd78ee81-b823-447c-b379-feee64d4a6d7)
**Note**- Change here with your public IP
---
### Conclusion
This POC successfully demonstrates how to perform bug analysis and code quality checks on a React application using SonarQube without any CI/CD tools. By manually configuring and running the scanner, developers can identify bugs, vulnerabilities, and code smells early in the development cycle.
---
##  Contacts
| Name               | Email                                 |
|--------------------|----------------------------------------|
| Harsh Wardhan Singh | harsh.singh.snaatak@mygurukulam.co    |
---
##   References
| Title                   | Link                                                                 |
|-------------------------|----------------------------------------------------------------------|
| SonarQube Documentation | [https://docs.sonarsource.com/sonarqube/](https://docs.sonarsource.com/sonarqube/) |
| SonarScanner CLI        | [https://docs.sonarsource.com/latest/scanners/sonarscanner/](https://docs.sonarsource.com/latest/scanners/sonarscanner/) |
| ESLint Formatters       | [https://eslint.org/docs/latest/use/formatters/](https://eslint.org/docs/latest/use/formatters/) |
this CI checks REACT bugs analysis
