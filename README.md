[![Build Status](https://travis-ci.org/alesium/ansible-net-haproxy.svg?branch=master)](https://travis-ci.org/alesium/ansible-net-haproxy)

net-haproxy
=========

Ansible Role to configure haproxy from pkgsrc

Requirements
------------

- Hosts requires pkgsrc's pkgin
- Hosts should be bootstrapped for ansible usage (have python,...)
- Root privileges, eg `become: yes`

Role Variables
--------------

| Variable | Description | Default value |
|----------|-------------|---------------|
| `net_haproxy_service_name` | Service name for handler | `"pkgsrc/haproxy"` | 
| `net_haproxy_config_file_src` | haproxy.cfg.j2 source file location | `"haproxy.cfg.j2"` | 
| `net_haproxy_config_file_dest` | haproxy.cfg.j2 remote location | `"/opt/local/etc/haproxy.cfg"` | 

Dependencies
------------

None

Example Playbook
----------------


    - hosts: servers
      roles:
         - { role: alesium.net-haproxy }

License
-------

BSD

Author Information
------------------

Sebastien Perreault <sperreault@alesium.net>
