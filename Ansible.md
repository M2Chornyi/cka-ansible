# Ansible

Initial files can be copied to directory:
```bash
cd /conmykc/IdeaProjects/devops-repo/
cp /etc/ansible/ansible.cfg ansible.cfg
cp /etc/ansible/hosts .
```
Base command to test data:
```bash
ansible all -m ping
ansible <group_win> -m win_ping
```
To get details about defined **facts**:
```bash
ansible -m setup <hostname>
ansible -m setup <hostname> -a 'filter=ansible_*_mb'
```

Run Ad-hoc command
```bash
ansible prs_temp --forks 1 -K -b --become-method=dzdo -m shell -a ""
ansible capc_unix -m shell -a "/sbin/chkconfig --list CGdsme | grep on"
ansible prs_unix -m shell -a "/sbin/chkconfig --list CGdsme | grep on" --forks 1
```


To run Ansible with variable:
```bash
ansible-playbook game.yml --extra-vars "target=local"
ansible-playbook game.yml -e target=local
```


