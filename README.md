statsd
=========

[![Build Status](https://travis-ci.org/jebovic/ansible-statsd.svg?branch=master)](https://travis-ci.org/jebovic/ansible-statsd) [![Ansible Galaxy](https://img.shields.io/badge/galaxy-jebovic.statsd-blue.svg?style=flat)](https://galaxy.ansible.com/jebovic/statsd)

Install and configure statsd

Role Variables
--------------

```yaml
# statsd install configuration
statsd_dep_packages:
  - git
statsd_github_repo: https://github.com/etsy/statsd
statsd_version: HEAD

# statsd basic configuration
statsd_user: statsd
statsd_user_group: statsd
statsd_install_path: /opt/statsd
statsd_config_path: /etc/statsd
```

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - { role: jebovic.statsd }
```

Tags
----

* statsd_config : only update config and restart service

License
-------

MIT

Author Information
------------------

Jérémy Baumgarth https://github.com/jebovic