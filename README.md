/etc/ansible/ansible.cfg is the default config file location
but we can create multiple playbook configuration directories such as /opt/web-playbooks, /opt/network-playbooks, /opt/db-playbooks and store ansible.cfg files there

**Configuration variables:**
$ ANSIBLE_GATHERING = explicit ansible-playbook playbook.yml    (we can specify the variable key/value before executing playbook but this is not persistent)
As alternative we can consider using export to make this change applicable shell wide, until you exit shell
$ export ANSIBLE_GATHERING=explicit
$ ansible-playbook playbook.yml
To make this change persistent, we can use configuration file such as /opt/web-playbooks/ansible.cfg

**View Configuration**
$ ansible-config list #lists all configurations
$ ansible-config view # shows the current config file
$ ansible-config dump # shows the current settings

Lab1:
[bob@student-node playbooks]$ cat practice.yaml 
employee:  # dictionary
  name: john  # key/value separated by a colon

[bob@student-node playbooks]$ cat practice.yaml # array with line at beginning of each dataset
- name: apple
  color: red
  weight: 100g
- name: orange
  color: orange
  weight: 90g
- name: mango
  color: yellow
  weight: 150g
