[![Ansible Galaxy](https://raw.githubusercontent.com/roles-ansible/role_ranger/master/.github/galaxy.svg?sanitize=true)](https://galaxy.ansible.com/do1jlr/ranger) [![Build Status](https://travis-ci.org/roles-ansible/role_ranger.svg?branch=master)](https://travis-ci.org/roles-ansible/role_ranger) [![MIT License](https://raw.githubusercontent.com/roles-ansible/role_ranger/master/.github/license.svg?sanitize=true)](https://github.com/roles-ansible/role_ranger/blob/master/LICENSE)


 role_ranger
==============

Ansible role to install the ranger file manager on linux. ranger is a console file manager with VI key bindings. More info about ranger is available at [github.com/ranger/ranger](https://github.com/ranger/ranger.git).


 What does this role do?
-------------
First we try to install ``ranger`` with the default package manager.
If this fails, we download the ranger git and compile it by ourself *(with python 3)*.<br/>
We also could perform a simple versioncheck that will check if a newer version of this role has been executed on this host before. You can enable it by setting ``submodules_versioncheck`` to ``true``

 How to use this role
-------------
You can either use this role via ansible galaxy or use it directly from [this](https://github.com/roles-ansible/role_ranger.git) git repository.

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
git clone https://github.com/roles-ansible/role_ranger.git
```

Example Playbook:
```yaml
---
- hosts: localhost
  roles:
    - role_ranger
  tags:
   - ranger
  vars:
    submodules_versioncheck: true
```

 Testing
----------
This role is tested with [these github-action](https://github.com/search?q=topic%3Acheck-ansible+topic%3Agithub-actions+org%3Aroles-ansible&type=Repositories) tests for different versions of differen linux systems. Linting is tested via travis-ci.
If you want to find out more about our tests, please have a look at the github marketplace.

| test status | Github Marketplace |
| :---------  | :----------------  |
| [![Travis Build Status](https://travis-ci.org/roles-ansible/role_ranger.svg?branch=master)](https://travis-ci.org/roles-ansible/role_ranger) | [.travis.yml](https://github.com/roles-ansible/role_ranger/blob/master/.travis.yml) |
| [![Ansible Lint check](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20Lint%20check/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+Lint+check%22) | [ansible-lint action](https://github.com/marketplace/actions/ansible-lint)
| [![Ansible check debian:stable](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20debian:stable/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+debian%3Astable%22) | [ansible test with debian stable](https://github.com/marketplace/actions/check-ansible-debian-stable) |
| [![Ansible check debian:latest](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20debian:latest/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+debian%3Alatest%22) | [ansible test with debian latest](https://github.com/marketplace/actions/check-ansible-debian-latest) |
| [![Ansible check debian:sid](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20debian:sid/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+debian%3Asid%22) | [ansible test with debian sid](https://github.com/marketplace/actions/check-ansible-debian-sid) |
| [![Ansible check debian:buster](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20debian:buster/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+debian%3Abuster%22) | [ansible test with debian buster](https://github.com/marketplace/actions/check-ansible-debian-buster) |
| [![Ansible check debian:jessie](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20debian:jessie/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+debian%3Ajessie%22) | [ansible test with debian jessie](https://github.com/marketplace/actions/check-ansible-debian-jessie) |
| [![Ansible check debian:stretch](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20debian:stretch/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+debian%3Astretch%22) | [ansible test with debian stretch](https://github.com/marketplace/actions/check-ansible-debian-stretch) |
| | |
| [![Ansible check ubuntu:latest](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20ubuntu:latest/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+ubuntu%3Alatest%22) | [ansible test with ubuntu latest](https://github.com/marketplace/actions/check-ansible-ubuntu-latest) |
| [![Ansible check ubuntu:bionic](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20ubuntu:bionic/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+ubuntu%3Abionic%22) | [ansible test with ubuntu bionic](https://github.com/marketplace/actions/check-ansible-ubuntu-bionic) |
| [![Ansible check ubuntu:disco](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20ubuntu:disco/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+ubuntu%3Adisco%22) | [ansible test with ubuntu disco](https://github.com/marketplace/actions/check-ansible-ubuntu-disco) |
| [![Ansible check ubuntu:eoan](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20ubuntu:eoan/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+ubuntu%3Aeoan%22) | [ansible test with ubuntu eoan](https://github.com/marketplace/actions/check-ansible-ubuntu-eoan) |
| [![Ansible check ubuntu:focal](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20ubuntu:focal/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+ubuntu%3Afocal%22) | [ansible test with ubuntu focal](https://github.com/marketplace/actions/check-ansible-ubuntu-focal) |
| [![Ansible check ubuntu:trusty](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20ubuntu:trusty/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+ubuntu%3Atrusty%22) | [ansible test with ubuntu trusty](https://github.com/marketplace/actions/check-ansible-ubuntu-trusty) |
| [![Ansible check ubuntu:xenial](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20ubuntu:xenial/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+ubuntu%3Axenial%22) | [ansible test with ubuntu xenial](https://github.com/marketplace/actions/check-ansible-ubuntu-xenial) |
| | |
| [![Ansible check fedora:latest](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20fedora:latest/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+fedora%3Alatest%22) | [ansible test with fedora latest](https://github.com/marketplace/actions/check-ansible-fedora-latest) |
| [![Ansible check fedora:33](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20fedora:33/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+fedora%3A33%22) | [ansible test with fedora 33](https://github.com/marketplace/actions/check-ansible-fedora-33) |
| [![Ansible check fedora:32](https://github.com/roles-ansible/role_ranger/workflows/Ansible%20check%20fedora:32/badge.svg)](https://github.com/roles-ansible/role_ranger/actions?query=workflow%3A%22Ansible+check+fedora%3A32%22) | [ansible test with fedora 32](https://github.com/marketplace/actions/check-ansible-fedora-32) |


 variables
-------
```yaml
# perform simple versionscheck (true is recomended)
submodules_versioncheck: false

# infos for ranger installation
ranger:
  repo: 'https://github.com/ranger/ranger.git'
  branch: 'master'
  download_directory: "{{ x_ansible_download_dir | default(ansible_env.HOME + '/.ansible/tmp/downloads/ranger') }}"
```
