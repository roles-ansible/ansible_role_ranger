 role-ranger
==============
[![MIT License](https://github.com/chaos-bodensee/role-ranger/blob/master/.github/license.svg)](https://github.com/chaos-bodensee/role-ranger/blob/master/LICENSE)


Ansible role to install the ranger file manager on linux. ranger is a console file manager with VI key bindings. More info about ranger is available at [github.com/ranger/ranger](https://github.com/ranger/ranger.git).


 What does this role do?
-------------
First we try to install ``ranger`` with the default package manager.
If this fails, we download the ranger git and compile it by ourself *(with python 3)*.<br/>
We also perform a versioncheck that will check if a newer version of this role has been executed on this host before. You can disable it by setting ``ansible_versionscheck`` to `` false``

 How to use this role
-------------
You can either use this role via ansible galaxy or use it directly from [this](https://github.com/chaos-bodensee/role-ansible_version.git) git repository.

### ansible galaxy

Ansible-Rolle Instalieren:
```bash
ansible-galaxy install do1jlr.ranger
```

Example Ansible-Playbook:
```yml
---
- hosts: localhost
  roles:
  - do1jlr.ranger
```

### direkt anbinden

Ansible-Rolle clonen:
```bash
git clone https://github.com/chaos-bodensee/role-ranger.git
```

Example Playbook:
```yaml
---
- hosts: localhost
  roles:
    - role-ranger
  tags:
   - ranger
```


```
[WORK-IN-PROGRESS]

done:
- support for archlinux, centos + debian
- ansible galaxy support
- better readme


missing:
- travis && docker / actions checks
```
