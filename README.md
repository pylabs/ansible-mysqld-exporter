mysqld_exporter
===============

This role is used to install mysqld exporter automatically.

Role Variables
--------------

```yaml
mysqld_exporter_version: MYSQLD_EXPORTER_VERSION
mysqld_exporter_base_dir: MYSQLD_EXPORTER_BASE_DIR (default: /opt/mysqld_exporter)
mysqld_exporter_listen_address: MYSQLD_EXPORTER_LISTEN_ADDRESS (default: 0.0.0.0)
mysqld_exporter_listen_port: MYSQLD_EXPORTER_LISTEN_PORT (default: 9104)
```

Dependencies
------------

- pylabs.sysbase

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: pylabs.mysqld_exporter
  vars:
    mysqld_exporter_version: "0.12.1"
```

License
-------

MIT

Author Information
------------------

William Wu <william@pylabs.org>
