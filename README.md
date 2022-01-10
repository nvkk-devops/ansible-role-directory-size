# Ansible Role Windows / Linux
* Connect to Windows/Linux Machine
* List the directories along with sizes

## Windows
```
##### Pre-requisite
## on controller-node
$ ansible-galaxy collection install ansible.windows

## on managed-windows-host
$ curl -LO https://raw.githubusercontent.com/ansible/ansible/devel/examples/scripts/ConfigureRemotingForAnsible.ps1
$ ./ConfigureRemotingForAnsible.ps1

##### run playbook : on controller-node
$ export OBJC_DISABLE_INITIALIZE_FORK_SAFETY=YES
$ export domainpw=
$ ansible-playbook playbook.yml --extra-vars "ansible_password=${domainpw}" --extra-vars "domain_username=${domainUsername}" --tags windows -i hosts -v

```

## Linux
```
$ ansible-playbook playbook.yml --tags linux -i hosts --extra-vars "ansible_user=${domainUsername}" -k -v

```
