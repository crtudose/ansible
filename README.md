/etc/ansible/ansible.cfg is the default config file location
but we can create multiple playbook configuration directories such as /opt/web-playbooks, /opt/network-playbooks, /opt/db-playbooks and store ansible.cfg files there

**Configuration variables:**
$ ANSIBLE_GATHERING = explicit ansible-playbook playbook.yml    (we can specify the variable key/value before executing playbook but this is not persistent)
as alternative we can consider using export to make this change applicable shell wide, until you exit shell
$ export ANSIBLE_GATHERING=explicit
$ ansible-playbook playbook.yml
