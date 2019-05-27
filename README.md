apache_exporter
===============

Ansible role for install apache_exporter for Prometheus.

Requirements
------------

Ansible.

Role Variables
--------------

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `apache_exporter_version` | 0.6.0 | apache_exporter package version. |
| `apache_exporter_telemetry_address` | "0.0.0.0:9117" | Address on which apache_exporter will listen |
| `apache_exporter_telemetry_endpoint` | "/metrics" | Path under which to expose metrics |
| `apache_exporter_incecure` | "false" | Ignore server certificate if using HTTPS |
| `apache_exporter_scrape_uri` | "http://localhost/server-status/?auto" | URI to apache stub status page |

Dependencies
------------

None.

Example Playbook
----------------

Use it in a playbook as follows:

```yaml
- hosts: all
  become: yes
  roles:
    - apache_exporter
```

Configuration notes
-------------------

About usage of apache_exporter check:  
https://github.com/Lusitaniae/apache_exporter/blob/master/README.md

License
-------

BSD

Credits
-------

This role is inspired by https://github.com/cloudalchemy/ansible-mysqld-exporter  
apache_exporter is created by Lusitaniae (https://github.com/Lusitaniae/apache_exporter) and this is only wrap-up in Ansible role.
