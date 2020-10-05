
![Ansible Lint](https://github.com/tenantcloud/ansible-role-software-common/workflows/Ansible%20Lint/badge.svg?branch-master)
![Yaml Lint](https://github.com/tenantcloud/ansible-role-software-common/workflows/Yaml%20Lint/badge.svg?branch-master)

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

```yaml
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
```

License
-------

BSD

Author Information
------------------

TenantCloud DevOps Team
