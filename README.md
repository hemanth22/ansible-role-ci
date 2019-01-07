Role Name
=========

Ansible Role: CI

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

    - hosts: localhost
      roles:
        - role: hemanth22.ci
          tags: ['ci']

License
-------

GNU General Public License v3.0

Author Information
------------------

This role was created in 2019 by Hemanth BITRA.
