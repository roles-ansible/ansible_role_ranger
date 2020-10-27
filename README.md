[![Ansible Galaxy](https://raw.githubusercontent.com/roles-ansible/ansible_role_ranger/master/.github/galaxy.svg?sanitize=true)](https://galaxy.ansible.com/do1jlr/ranger) [![Build Status](https://travis-ci.com/roles-ansible/ansible_role_ranger.svg?branch=master)](https://travis-ci.com/roles-ansible/ansible_role_ranger) [![MIT License](https://raw.githubusercontent.com/roles-ansible/ansible_role_ranger/master/.github/license.svg?sanitize=true)](https://github.com/roles-ansible/ansible_role_ranger/blob/master/LICENSE)


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

 Testing
----------
This role is tested with [these github-action](https://github.com/search?q=topic%3Acheck-ansible+topic%3Agithub-actions+org%3Aroles-ansible&type=Repositories) tests for different versions of differen linux systems. Linting is tested via travis-ci and the  [ansible-lint action](https://github.com/marketplace/actions/ansible-lint).
If you want to find out more about our tests, please have a look at the github marketplace.

| test status | Github Marketplace |
| :---------  | :----------------  |
| [![Travis Build Status](https://travis-ci.com/roles-ansible/ansible_role_ranger.svg?branch=master)](https://travis-ci.com/roles-ansible/ansible_role_ranger) | [.travis.yml](https://github.com/roles-ansible/ansible_role_ranger/blob/master/.travis.yml) |
|||
| [![Ansible Lint check](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20Lint%20check/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+Lint+check%22) | [ansible-lint action](https://github.com/marketplace/actions/ansible-lint)
| [![Ansible check debian:stable](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20debian:stable/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+debian%3Astable%22) | [ansible test with debian stable](https://github.com/marketplace/actions/check-ansible-debian-stable) |
| [![Ansible check debian:latest](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20debian:latest/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+debian%3Alatest%22) | [ansible test with debian latest](https://github.com/marketplace/actions/check-ansible-debian-latest) |
| [![Ansible check debian:sid](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20debian:sid/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+debian%3Asid%22) | [ansible test with debian sid](https://github.com/marketplace/actions/check-ansible-debian-sid) |
| [![Ansible check debian:buster](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20debian:buster/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+debian%3Abuster%22) | [ansible test with debian buster](https://github.com/marketplace/actions/check-ansible-debian-buster) |
| [![Ansible check debian:stretch](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20debian:stretch/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+debian%3Astretch%22) | [ansible test with debian stretch](https://github.com/marketplace/actions/check-ansible-debian-stretch) |
| | |
| [![Ansible check archlinux:latest](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20archlinux:latest/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+archlinux%3Alatest%22) | [ansible test with archlinux latest](https://github.com/marketplace/actions/check-ansible-archlinux-latest) |
| | |
| [![Ansible check ubuntu:latest](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20ubuntu:latest/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+ubuntu%3Alatest%22) | [ansible test with ubuntu latest](https://github.com/marketplace/actions/check-ansible-ubuntu-latest) |
| [![Ansible check ubuntu:bionic](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20ubuntu:bionic/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+ubuntu%3Abionic%22) | [ansible test with ubuntu bionic](https://github.com/marketplace/actions/check-ansible-ubuntu-bionic) |
| [![Ansible check ubuntu:eoan](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20ubuntu:eoan/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+ubuntu%3Aeoan%22) | [ansible test with ubuntu eoan](https://github.com/marketplace/actions/check-ansible-ubuntu-eoan) |
| [![Ansible check ubuntu:trusty](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20ubuntu:trusty/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+ubuntu%3Atrusty%22) | [ansible test with ubuntu trusty](https://github.com/marketplace/actions/check-ansible-ubuntu-trusty) |
| [![Ansible check ubuntu:xenial](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20ubuntu:xenial/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+ubuntu%3Axenial%22) | [ansible test with ubuntu xenial](https://github.com/marketplace/actions/check-ansible-ubuntu-xenial) |
| | |
| [![Ansible check fedora:latest](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20fedora:latest/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+fedora%3Alatest%22) | [ansible test with fedora latest](https://github.com/marketplace/actions/check-ansible-fedora-latest) |
| [![Ansible check fedora:33](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20fedora:33/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+fedora%3A33%22) | [ansible test with fedora 33](https://github.com/marketplace/actions/check-ansible-fedora-33) |
| [![Ansible check fedora:32](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20fedora:32/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+fedora%3A32%22) | [ansible test with fedora 32](https://github.com/marketplace/actions/check-ansible-fedora-32) |
| [![Ansible check fedora:31](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20fedora:31/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+fedora%3A31%22) | [ansible test with fedora 31](https://github.com/marketplace/actions/check-ansible-fedora-31) |
| | |
| [![Ansible check centos:latest](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20centos:latest/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+centos%3Alatest%22) | [ansible test with centos latest](https://github.com/marketplace/actions/check-ansible-centos-latest) |
| [![Ansible check centos:centos8](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20centos:centos8/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+centos%3Acentos8%22) | [ansible test with centos centos8](https://github.com/marketplace/actions/check-ansible-centos-centos8) |
| [![Ansible check centos:centos7](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20centos:centos7/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+centos%3Acentos7%22) | [ansible test with centos centos7](https://github.com/marketplace/actions/check-ansible-centos-centos7) |
| | |
| [![Ansible check alpine:latest](https://github.com/roles-ansible/ansible_role_ranger/workflows/Ansible%20check%20alpine:latest/badge.svg)](https://github.com/roles-ansible/ansible_role_ranger/actions?query=workflow%3A%22Ansible+check+alpine%3Alatest%22) | [ansible test with alpine latest](https://github.com/marketplace/actions/check-ansible-alpine-latest) |


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
