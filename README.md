Ansible Role: CI
=========
[![CI](https://github.com/hemanth22/ansible-role-ci/actions/workflows/CI.yml/badge.svg)](https://github.com/hemanth22/ansible-role-ci/actions/workflows/CI.yml)

It is maven based simple ci, which will perform maven compile, maven test, maven package.

Requirements
------------

Pre-requisites are configured in the role itself no need of any extra roles.

Role Variables
--------------

In ci_path variable define path where git reportory to be placed and perform ci build and testing.
```
ci_path: test
```

In ci_repo variable define github repository link.
```
ci_repo: https://github.com/hemanth22/GroovyLearning.git
```
In ci_branch variable define git branch where you want to perform the ci build and test.

```
ci_branch: superpom
```

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
---
- hosts: localhost
  remote_user: vagrant
  vars:
    ci_repo: https://github.com/hemanth22/GroovyLearning.git
    ci_path: hemanthtest
    ci_branch: codecoverage
  roles:
    - role: hemanth22.ci
      become: true
      become_method: sudo
```

To create a directory and work as CI use below command.
```
ansible-playbook test.yml --tags ci
```
To destroy test directory created during CI.
```
ansible-playbook test.yml --tags destroy
```
License
-------

GNU General Public License v3.0

Author Information
------------------

This role was created in 2019 by Hemanth BITRA.
