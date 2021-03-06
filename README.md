statsd
=========

[![Build Status](https://travis-ci.org/jebovic/ansible-statsd.svg?branch=master)](https://travis-ci.org/jebovic/ansible-statsd) [![Ansible Galaxy](https://img.shields.io/badge/galaxy-jebovic.statsd-blue.svg?style=flat)](https://galaxy.ansible.com/jebovic/statsd)

Install and configure statsd (Work in progress)

This role is a part of my [OPS project](https://github.com/jebovic/ops), follow this link to see it in action. OPS provides a lot of stuff, like a vagrant file for development VMs, playbooks for roles orchestration, inventory files, examples for roles configuration, ansible configuration file, and many more.

Compatibility
-------------

Tested and approved on :

* Debian jessie (8+)
* Ubuntu Trusty (14.04 LTS)
* Ubuntu Xenial (16.04 LTS)

Dependencies
------------

This role depends on [jebovic.nodejs](https://github.com/jebovic/ansible-nodejs) and [jebovic.supervisor](https://github.com/jebovic/ansible-supervisor) roles to be fully functional

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

Example : config
----------------

```yaml
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
