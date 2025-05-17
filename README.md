
![image](https://github.com/user-attachments/assets/64dbad01-fbc3-488a-b733-ad6365173823)


|**Author**        | **created on**       | **Version** |**Last edited on**| **Review Level**   | **Reviewer**      |
|---------------|------------|---------|--------|--------|----------------------|
| Anitha Annem  | May 16  | v1.0|  May 17    | Pre-Reviewer   | Priyanshu            |
| Anitha Annem  |  |  |   | L0             | Khushi Malhothra    |
| Anitha Annem  |     |      |         | L1             | Mukul Joshi       |
| Anitha Annem  |     |      |         | L2             | piyush Upadhyay      |


# Table of Contents

- [Introduction](#introduction)
- [Jenkins POC Setup](#jenkins-poc-setup)
- [Contact Information](#contact-information)
- [References](#references)



For more detailed infromation related refer this link [Ansible Role Documentation](https://github.com/Cloud-NInja-snaatak/Documentation/blob/kanika_scrum44/commonstack/ansible/role/intro.md)


# Introduction 
This Proof of Concept (POC) demonstrates a basic setup of Jenkins, an open-source automation server widely used for continuous integration and continuous delivery (CI/CD). 

# Jenkins POC Setup

## Install Java
```bash
sudo apt update
sudo apt install openjdk-11-jdk -y
java -version
```
## Install Jenkins
```bash
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb https://pkg.jenkins.io/debian binary/ > /etc/apt/sources.list.d/jenkins.list'

sudo apt update
sudo apt install jenkins -y
```
##  Start & Enable Jenkins
```bash
sudo systemctl start jenkins
sudo systemctl enable jenkins
```
Check status:
```bash
sudo systemctl status jenkins
```
## Access Jenkins UI
Open a browser and visit:
```
http://<your-server-ip>:8080
```
## Unlock Jenkins
Get the initial admin password:
```
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
Paste it into the UI to continue.



# Contact Information 
| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|

# References
| **Link** | **Description** |
|------------------------------------------------------|------------------|
| [Jenkins Installation](https://www.jenkins.io/doc/book/installing/linux/)| Installation on Jenkins      |
