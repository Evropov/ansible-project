# anisible-project
The "ansible-project" repository contains a set of Ansible playbooks, roles, and templates that are used for automating the setup and configuration of servers and deploying a simple WordPress-based web application. These playbooks and roles are designed to work on Ubuntu-based systems. This documentation will guide you through the repository and provide information on how to use the playbook to deploy the web application.

Getting Started:

Before you begin, ensure that you have installed the following prerequisites:

- Ansible
- Python
- Git

Clone the Repository: 

To get started, clone the 'ansible-project' repository by running the following command:
```
git clone https://github.com/Evropov/ansible-project.git
```
Once the repository has been cloned, navigate to the ansible-project directory and switch to the "master" branch:
```
cd ansible-project
```
```
git checkout master
```
The repository contains the following directories and files:

- hosts: Contains the inventory file that specifies the servers and variables that the playbooks will target.
- roles: Contains the Ansible roles that are used to configure the servers.
- playbook.yml: The main Ansible playbook that runs all the roles.

Ansible Playbook:

The Ansible playbook is located in the 'ansible-project' directory. The playbook is named playbook.yml and is used to install the whole LAMP stack and deploy the web application.

The playbook consists of the following tasks and their respective roles:

- Specify the Pythin interpreter that should be used
- Install required packages for a LAMP server(server)
- Install some additional PHP extensions(php)
- Create a database, database user and password(mysql)
- Download, unarchive and configure a WordPress instance to use the created database, database user and password(wordpress)

Variables:

The variables associated with the MySQL role are included in the roles/mysql/defaults/main.yml file:

- wp_mysql_db: the name of the database that will be created
- wp_mysql_user: the username of the database user that will be created
- wp_mysql_password: the password for the database user

Usage:

To use the playbook, run the following command:
```
ansible-playbook playbook.yml -i hosts
```
This will run all the roles specified in the playbook.yml playbook on the server/s specified in the inventory file.

Customization:

The playbooks and roles in this repository are designed to work with Ubuntu-based systems. If you are using a different operating system or have specific requirements for your server configuration, you may need to modify the playbooks and roles to meet your needs.

To modify the playbooks and roles, you can edit the YAML files in the roles/task directory. You can also create your own roles and add them to the repository if you need to customize the configuration further.

Conclusion:

The "ansible-project" repository is a useful tool for automating the setup and configuration of servers and deploy a simple web application using Ansible. It contains a set of playbooks and roles that are designed to work with Ubuntu-based systems, but can be customized to meet your specific requirements.
