tenantcloud.software_common
=========

Ansible role for install common software. This role include install:

  - python@3
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

ansible_user: "user" os username

Dependencies
------------

  - homebrew
  - python@3
  - ansible

Example Playbook
----------------

    - hosts: localhost
      become: no
      vars:
        ansible_user: "user"
        mas_installed_apps:
          - { id: 497799835, name: "Xcode" }
      roles:
        - tenantcloud.software_common

License
-------

BSD

Author Information
------------------

TenantCloud DevOps Team
