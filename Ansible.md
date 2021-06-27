# Ansible
Set `ANSIBLE_CONFIG` variable:
```shell
export ANSIBLE_CONFIG=./ansible.cfg
```

To run Ansible with variable:
```bash
ansible-playbook centos7.yml -e target=centos7
```

Using password hash instead of plain password through [crypt](https://docs.python.org/3.4/library/crypt.html) module
```shell script
python3 -c 'import crypt,getpass;pw=getpass.getpass();print(crypt.crypt(pw) if (pw==getpass.getpass("Confirm: ")) else exit())'
```
