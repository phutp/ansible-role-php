# ansible-role-php

Role for install & config specific version of php from the remi repository (CentOS 7)

## Example Playbook
```
---
- name: install php
  hosts:
    - vagrant-be
  become: true
  vars:
    php_version: "php72"
    php_fpm_pool_name: "ocean"
    pm_mode: "static"
    pm_max_children: "150"
    pm_max_requests: "3000"
    pm_process_idle_timeout: "30"
    pm_request_slowlog_timeout: "1"
    php_fpm_user: "nginx"
    php_fpm_group: "nginx"
    php_fpm_listen: "127.0.0.1:9001"
    php_fpm_listen_owner: "nginx"
    php_fpm_listen_group: "nginx"
    php_fpm_listen_allowed_clients: "127.0.0.1"
  roles:
    - role: php
```
