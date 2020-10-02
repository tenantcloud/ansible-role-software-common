
<img src="https://github.com/tenantcloud/ansible-role-software-common/workflows/Ansible Lint/badge.svg?branch-master" alt="">
<img src="https://github.com/tenantcloud/ansible-role-software-common/workflows/Yaml Lint/badge.svg?branch-master" alt="">

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
  - wireguard

Requirements
------------

ansible-galaxy install geerlingguy.homebrew geerlingguy.mas

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
          - { id: 1451685025, name: "WireGuard" }
      roles:
        - geerlingguy.homebrew
        - geerlingguy.mas
        - tenantcloud.software_common
       environment:
         PATH: "/usr/local/bin:{{ ansible_env.PATH }}"
       
License
-------

BSD

Author Information
------------------

TenantCloud DevOps Team
