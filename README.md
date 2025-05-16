
![image](https://github.com/user-attachments/assets/1eb0574d-e894-4c8b-94e1-4ab2d878ba45)


|**Author**        | **created on**       | **Version** |**Last edited on**| **Review Level**   | **Reviewer**      |
|---------------|------------|---------|--------|--------|----------------------|
| Anitha Annem  | May 16  | v1.0|  May 16    | Pre-Reviewer   | Priyanshu            |
| Anitha Annem  |  |  |   | L0             | Khushi Malhothra    |
| Anitha Annem  |      |      |         | L1             | Mukul Joshi       |
| Anitha Annem  |      |      |         | L2             | piyush Upadhyay      |


# Introduction
In modern software development, ensuring code quality and security is crucial. Continuous Integration (CI) systems play a pivotal role in automating code validation, while dependency scanning safeguards projects from vulnerabilities in third-party libraries. This documentation focuses on implementing Java CI checks and dependency scanning within a DevOps pipeline.

# What is Dependency Scanning?
Dependency scanning is an automated process that analyzes a software project’s dependencies, including direct and transitive (nested) libraries, to detect known security vulnerabilities, license compliance issues, or outdated packages. It typically involves comparing dependency versions against vulnerability databases such as the National Vulnerability Database (NVD) or vendor-specific security advisories.


# Why is Dependency Scanning Important?

- **Security:** Third-party dependencies can have unpatched vulnerabilities that attackers exploit.
- **Compliance:** Ensures that licenses of dependencies comply with organizational policies.
- **Quality Assurance:** Detects deprecated or unsupported libraries which may cause reliability issues.
- **Risk Mitigation:** Proactively identifies risky dependencies to reduce technical debt and security incidents.

# Workflow

![image](https://github.com/user-attachments/assets/aad370b9-2f96-4f84-8cc7-e1af7d30ceed)

## Dependency Scanning Workflow

### Step 1: Source Code Repository
The starting point is the application's source code, stored in a repository (e.g., GitHub, GitLab, Bitbucket).  
This code typically includes a manifest file (e.g., `package.json`, `pom.xml`, `requirements.txt`) that lists the project dependencies.

### Step 2: Dependency Scan Tool Integration
A dependency scanning tool (e.g., Snyk, OWASP Dependency-Check, Dependabot) is integrated into the CI/CD pipeline.  
It parses the manifest files to identify all direct and transitive (indirect) dependencies.

### Step 3: Vulnerability Database Check
The tool compares the discovered dependencies (and their versions) against a vulnerability database, such as:
- NVD (National Vulnerability Database)
- GitHub Advisory Database
- Snyk Vulnerability DB

It checks whether any of the dependencies are known to have security vulnerabilities (typically identified by CVEs).

### Step 4: Scan Results Generated
The scan outputs a report listing:
- Vulnerable dependencies
- CVE IDs
- Severity scores (e.g., CVSS score)
- Remediation advice (e.g., update to version X)

### Step 5: Developer Review & Fix
Developers are notified (via the pipeline, a dashboard, or automated pull requests).  
They review the scan results and take corrective actions:
- Upgrade the vulnerable dependency
- Replace or remove insecure libraries
- Apply security patches if available




# Different Dependency Scanning Tools

| Tool Name             | Supported Languages                 | Features                                         | License             |
|-----------------------|-----------------------------------|-------------------------------------------------|---------------------|
| OWASP Dependency-Check| Java, .NET, Node.js, Python, Ruby | Open-source, integrates with CI, reports CVEs   | Apache 2.0          |
| Snyk                  | Multiple                          | Real-time monitoring, automated fixes, container scanning | Commercial + Free tier |
| GitHub Dependabot     | Multiple                          | Automated pull requests for updates, vulnerability alerts | Built-in GitHub     |
| WhiteSource           | Multiple                          | License compliance, policy enforcement, comprehensive vulnerability database | Commercial          |
| Sonatype Nexus IQ     | Multiple                          | Advanced policy engine, governance, detailed analytics | Commercial          |

# Comparison of Tools

| Feature               | OWASP Dependency-Check | Snyk  | GitHub Dependabot | WhiteSource | Sonatype Nexus IQ |
|-----------------------|------------------------|-------|-------------------|-------------|-------------------|
| Open Source           | Yes                    | No    | Yes               | No          | No                |
| Languages Supported   | Broad                  | Broad | Broad             | Broad       | Broad             |
| Integration with CI/CD| Yes                    | Yes   | Yes               | Yes         | Yes               |
| Automated Fixes       | No                     | Yes   | Yes               | No          | No                |
| License Compliance    | Basic                  | Advanced | Basic           | Advanced    | Advanced          |
| Container Scanning    | No                     | Yes   | No                | Yes         | Yes               |
| Pricing               | Free                   | Freemium | Free             | Commercial  | Commercial        |


# Advantages of Dependency Scanning

- **Early Detection:** Finds vulnerabilities before deployment.
- **Automated:** Integrates into CI/CD, reducing manual effort.
- **Comprehensive:** Scans both direct and transitive dependencies.
- **Regulatory Compliance:** Helps meet security standards and audits.
- **Improves Code Quality:** Encourages use of secure and updated dependencies.
  
# Best Practices

- Integrate dependency scanning early in the development lifecycle (Shift Left).
- Regularly update scanning tools and vulnerability databases.
- Set severity thresholds to fail builds based on risk tolerance.
- Combine dependency scanning with static code analysis for holistic security.
- Educate developers on interpreting scan results and remediation.
- Track and manage dependencies continuously, not just at release.

# Conclusion
Dependency scanning is an essential component of modern secure software development. Organizations should adopt automated dependency scanning integrated into their CI/CD pipelines to ensure continuous security monitoring. Selection of tools depends on the project language, ecosystem, budget, and desired features such as automated fixes or license compliance. Combining multiple tools can also provide enhanced coverage.


# Contact Information 
| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|


# References
| **Link** | **Description**            |
|----------|-------------------------------|
|[OWSAP](https://owasp.org/www-project-dependency-check/)|For OWSAP.|
|[Dependency scanning](https://github.com/diffblue/gitlab/blob/master/doc/user/application_security/dependency_scanning/index.md) | Documentation followed from this link .|
