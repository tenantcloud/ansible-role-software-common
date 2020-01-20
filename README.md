tenantcloud.ansible_role_software_common
=========

Ansible role for install common software. This role include install:

  - iterm2
  - slack
  - google-chrome
  - firefox
  - tunnelblick
  - authy

Requirements
------------

Role Variables
--------------

work_user: "user" os username

Dependencies
------------

  - homebrew
  - python@3
  - ansible

Example Playbook
----------------

    - hosts: localhost
      become: no
      roles:
        - tenantcloud.ansible_role_software_common

License
-------

BSD

Author Information
------------------

TenantCloud DevOps Team
