[![Ansible Galaxy](https://raw.githubusercontent.com/roles-ansible/ansible_role_ranger/master/.github/galaxy.svg?sanitize=true)](https://galaxy.ansible.com/do1jlr/ranger) [![MIT License](https://raw.githubusercontent.com/roles-ansible/ansible_role_ranger/master/.github/license.svg?sanitize=true)](https://github.com/roles-ansible/ansible_role_ranger/blob/master/LICENSE)

 ansible_role_ranger
==============

Ansible role to install the ranger file manager on linux. ranger is a console file manager with VI key bindings. More info about ranger is available at [github.com/ranger/ranger](https://github.com/ranger/ranger.git).


 What does this role do?
-------------
+ This role try to install ``ranger`` with the default package manager.
+ If this fails, this role will download the ranger git and compile it by ourself *(with python 3)*.
+ We also could perform a simple versioncheck that will check if a newer version of this role has been executed on this host before.
  - You can enable it by setting ``submodules_versioncheck`` to ``true``

 How to use this role
-------------
You can either use this role via ansible galaxy or use it directly from [this](https://github.com/roles-ansible/ansible_role_ranger.git) git repository.

### ansible galaxy
install role:
```bash
ansible-galaxy install do1jlr.ranger
```

You can execute the role **directly via ansible ad-hoc command**, but it is highly recomended to create a ansible playbook
```bash
# example ad-hoc command
ansible -m include_role -a "name=do1jlr.ranger" localhost
```

Example Ansible-Playbook:
```yml
---
- hosts: localhost
  roles:
  - do1jlr.ranger
```

### use via git command
clone github repo:
```bash
git clone https://github.com/roles-ansible/ansible_role_ranger.git
```

example Playbook:
```yaml
---
- hosts: localhost
  roles:
    - ansible_role_ranger
  tags:
   - ranger
  vars:
    submodules_versioncheck: true
```

## Requirements
The ``community.general`` collection is required for some parts of this ansible role.
You can install it with this command:
```bash
ansible-galaxy collection install -r requirements.yml --upgrade
```

 variables
-------
```yaml
# perform simple versionscheck (true is recomended)
submodules_versioncheck: false

# parameter for ranger installation
ranger:
  repo: 'https://github.com/ranger/ranger.git'
  branch: 'master'
  download_directory: "{{ x_ansible_download_dir | default(ansible_env.HOME + '/.ansible/tmp/downloads/ranger') }}"
```
