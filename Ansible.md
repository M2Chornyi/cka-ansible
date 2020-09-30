# Ansible

To run Ansible with variable:
```bash
ansible-playbook k8s.yml -e target=k8s
```

Using password hash instead of plain password through [crypt](https://docs.python.org/3.4/library/crypt.html) module
```shell script
python3 -c 'import crypt,getpass;pw=getpass.getpass();print(crypt.crypt(pw) if (pw==getpass.getpass("Confirm: ")) else exit())'
```
