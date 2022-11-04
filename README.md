# Ansible AWS CLI Playbook
Ansible playbook to install AWS CLI on Ubuntu 14.04. Should work on most other versions of Ubuntu too.

## Setup
- Clone or download the repo to your Ansible machine
- Add your host information within `inventories/hosts`
- Add your AWS creditentials and bucket details within `vars/awscredentials.yml`

## Run Playbook
Below is how I prefer to run Ansible playbooks.
```
ansible-playbook -i inventories/hosts playbook.yml
```
You can also run Ansible playbooks using below command:
```
ansible-playbook -i inventories/hosts playbook.yml --extra-vars="hosts=sonarqube user=ubuntu" --ask-pass
```

The `--extra-vars` parameter sets the "host" and "user" variable in the `playbook` file. And `--ask-pass` will prompt you for a password.


