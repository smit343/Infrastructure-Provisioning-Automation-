# Project 2 -  Infrastructure Provisioning Automation with Ansible and/or Terraform

This project deploys AWS infrastructure using infrastructure provisioning automation tools (Infrastructure as Code). There are three sets of infrastructure components that will be deployed on AWS:
- AWS VPC network.;
  
- Database server.
Create and launch an EC2 instance - e.g. Ubuntu 22.04 - into the private subnet created earlier.
Download and install a database server in the EC2 instance - e.g. MySQL, PostgreSQL or MongoDB.
Start and enable the database server service and ensure the database ports - e.g. 3306, 5432, etc. - are open and able to receive connections.;

- API server.
Create and launch an EC2 instance - e.g. Ubuntu 22.04 - into the public subnet created earlier.
Download and install packages for an API server.
For example for a Python FastAPI API server:
Python 3.10.
fastapi python library.


This repository is composed of the following files:
- infra.ansible.yaml, userdata.sh, userdata_app.sh.


URL for the public GitHub repository: https://github.com/smit343/Infrastructure-Provisioning-Automation-

## Table of contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Testing the Results](#testing-the-results)
- [Authors](#authors)

## Prerequisites

- AWS account;
- IAM user with sufficient rights;
- Access to a Linux terminal;
- Have AWS CLI, git, ansible installed on your Linux machine;
- Basic knowledge of Ansible, AWS, and Git. 

## Installation

To install the required tools, follow the steps in the links below:

- AWS CLI:
https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

- Git:
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

- Ansible:
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html

- Python3, pip:
```sh
#Python3
sudo apt update
sudo apt install python3

#pip
sudo apt install python3-pip


\## Getting Started

- To have access to your AWS account through your IAM user, execute the following command in your terminal
```sh
$ aws configure
AWS Access Key ID [None]: paste your access key id
AWS Secret Access Key [None]: paste your secret access key
Default region name [None]: us-east-1
Default output format [None]:
```

- In your terminal, clone this repository :
```
git clone https://github.com/smit343/Infrastructure-Provisioning-Automation-
cd Infrastructure-Provisioning-Automation-
```

## Usage

- Execute the Ansible playbooks in the following order :
```sh
ansible-playbook infra.ansible.yaml
```

## Testing the Results
- Copy the DNS of the load balancer created, and paste it on your web browser, editing the route according to the desired output:

Available routes:

- `/` - returns all documents in the database-players.csv collection.
- `/players/top/:number` - returns top players. For example, /players/top/10 will return the top 10 players leading in points scored.
- `/players/team/:teamname` - returns all players of a team. For example, /players/team/TOR will return all players of Toronto Maple Leafs.
- `/teams` - returns a list of the teams.

```

## Diagram

![AWS Diagram of Project 7, parts 1 and 2](./project7_part12.jpg)
![AWS Diagram of Project 7, part 3](./project7_part3.jpg)

## Authors

- Smit Patel - (https://github.com/smit343/Infrastructure-Provisioning-Automation-)
