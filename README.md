
![image](https://github.com/user-attachments/assets/64dbad01-fbc3-488a-b733-ad6365173823)


|**Author**        | **created on**       | **Version** |**Last edited on**| **Review Level**   | **Reviewer**      |
|---------------|------------|---------|--------|--------|----------------------|
| Anitha Annem  | May 16  | v1.0|  May 17    | Pre-Reviewer   | Priyanshu            |
| Anitha Annem  |  |  |   | L0             | Khushi Malhothra    |
| Anitha Annem  |     |      |         | L1             | Mukul Joshi       |
| Anitha Annem  |     |      |         | L2             | piyush Upadhyay      |

For more detailed infromation related refer this link [Ansible Role Documentation](https://github.com/Cloud-NInja-snaatak/Documentation/blob/kanika_scrum44/commonstack/ansible/role/intro.md)

# Directory Structure
```bash
jenkins-role/
├── defaults/
│   └── main.yml
├── files/
│   └── jenkins.repo
├── handlers/
│   └── main.yml
├── tasks/
│   └── main.yml
├── templates/
│   └── jenkins.service.j2
├── vars/
│   └── main.yml
├── meta/
│   └── main.yml
└── README.md
```
## Role Components

defaults/main.yml
Contains default variables (can be overridden):

```yaml
jenkins_port: 8080
jenkins_home: /var/lib/jenkins
jenkins_version: "2.426.1"
```
vars/main.yml
Contains version-pinned or OS-specific variables:
```yaml
jenkins_repo_url: "http://pkg.jenkins.io/redhat-stable/jenkins.repo"
jenkins_gpg_key_url: "https://pkg.jenkins.io/redhat-stable/jenkins.io.key"
java_package: "java-11-openjdk"
```

tasks/main.yml
Defines the main playbook steps:
```yaml
- name: Install Java
  package:
    name: "{{ java_package }}"
    state: present

- name: Add Jenkins repo
  get_url:
    url: "{{ jenkins_repo_url }}"
    dest: /etc/yum.repos.d/jenkins.repo

- name: Import GPG key
  rpm_key:
    state: present
    key: "{{ jenkins_gpg_key_url }}"

- name: Install Jenkins
  package:
    name: jenkins
    state: present

- name: Enable and start Jenkins
  service:
    name: jenkins
    enabled: yes
    state: started
```
handlers/main.yml
```yaml
- name: restart jenkins
  service:
    name: jenkins
    state: restarted
```


# Contact Information 
| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|

# References
| **Link** | **Description** |
|------------------------------------------------------|------------------|
| [Attendance](https://github.com/Cloud-NInja-snaatak/Documentation/blob/Shubham_SCRUM-72/ot_ms_understanding/application/attendance/documentation/README.md)| Attendance Documentations      |
