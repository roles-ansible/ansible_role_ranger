[![Ansible Galaxy](https://raw.githubusercontent.com/chaos-bodensee/role-ranger/master/.github/galaxy.svg?sanitize=true)](https://galaxy.ansible.com/do1jlr/ranger)
[![Build Status](https://travis-ci.org/chaos-bodensee/role-ranger.svg?branch=master)](https://travis-ci.org/chaos-bodensee/role-ranger)
[![Ansible Lint check](https://github.com/chaos-bodensee/role-ranger/workflows/Ansible%20Lint%20check/badge.svg)](https://github.com/chaos-bodensee/role-ranger/actions?query=workflow%3A%22Ansible+Lint+check%22)
[![Ansible check debian:stable](https://github.com/chaos-bodensee/role-ranger/workflows/Ansible%20check%20debian:stable/badge.svg)](https://github.com/chaos-bodensee/role-ranger/actions?query=workflow%3A%22Ansible+check+debian%3Astable%22)
[![Ansible check debian:buster](https://github.com/chaos-bodensee/role-ranger/workflows/Ansible%20check%20debian:buster/badge.svg)](https://github.com/chaos-bodensee/role-ranger/actions?query=workflow%3A%22Ansible+check+debian%3Abuster%22)
[![Ansible check debian:sid](https://github.com/chaos-bodensee/role-ranger/workflows/Ansible%20check%20debian:sid/badge.svg)](https://github.com/chaos-bodensee/role-ranger/actions?query=workflow%3A%22Ansible+check+debian%3Asid%22)
[![MIT License](https://raw.githubusercontent.com/chaos-bodensee/role-ranger/master/.github/license.svg?sanitize=true)](https://github.com/chaos-bodensee/role-ranger/blob/master/LICENSE)

 role-ranger
==============

Ansible role to install the ranger file manager on linux. ranger is a console file manager with VI key bindings. More info about ranger is available at [github.com/ranger/ranger](https://github.com/ranger/ranger.git).


 What does this role do?
-------------
First we try to install ``ranger`` with the default package manager.
If this fails, we download the ranger git and compile it by ourself *(with python 3)*.<br/>
We also could perform a simple versioncheck that will check if a newer version of this role has been executed on this host before. You can enable it by setting ``submodules_versioncheck`` to ``true``

 How to use this role
-------------
You can either use this role via ansible galaxy or use it directly from [this](https://github.com/chaos-bodensee/role-ansible_version.git) git repository.

### ansible galaxy

Ansible-Rolle Installieren:
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
  vars:
    submodules_versioncheck: true
```


```
[WORK-IN-PROGRESS]

done:
- support for archlinux, centos + debian
- ansible galaxy support

started:
- travis && docker / actions checks
```
