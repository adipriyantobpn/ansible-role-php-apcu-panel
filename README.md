Ansible Role: APCu Panel
=========

An Ansible Role that to manage APCu Panel Yum repository

Requirements
------------

This role needs no special requirements, except sudo access

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):


```yaml
---
apcu_panel_enable_all: no
apcu_panel_enable_ips:
  - "192.168.83.0/24"
  - "172.20.0.0/16"
apcu_panel_username: admin
apcu_panel_password: superduperlongpassword
php_enable_webserver: yes
php_webserver_daemon: httpd
php_enable_php_fpm: no
php_fpm_daemon: php-fpm
```

Dependencies
------------

None

Example Playbook
----------------

```yaml
---
- name: Prepare CentOS 7 server
  hosts: centos7
  roles:
    - role: adipriyantobpn.php-apcu-panel
      apcu_panel_enable_all: no
      apcu_panel_enable_ips:
        - "192.168.83.0/24"
        - "172.20.0.0/16"
        - "172.16.0.0/24"
      apcu_panel_username: phpmaster
      apcu_panel_password: passwordfortesting
      php_enable_webserver: yes
      php_webserver_daemon: httpd
      php_enable_php_fpm: no
      php_fpm_daemon: php-fpm
```

License
-------

BSD

Author Information
------------------

This role was created in 2017 by [Adi Priyanto](https://github.com/adipriyantobpn) as a learning purpose for community.