mysqld_exporter
===============

This role is used to install mysqld exporter automatically.

Role Variables
--------------

```yaml
mysqld_exporter_version: MYSQLD_EXPORTER_VERSION
mysqld_exporter_db_account: MYSQLD_EXPORTER_DB_ACCOUNT
mysqld_exporter_db_password: MYSQLD_EXPORTER_DB_PASSWORD
mysqld_exporter_db_host: MYSQLD_EXPORTER_DB_HOST (default: localhost)
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
    mysqld_exporter_db_account: "prometheus"
    mysqld_exporter_db_password: "mypa$$word"
```

License
-------

MIT

Author Information
------------------

William Wu <william@pylabs.org>
