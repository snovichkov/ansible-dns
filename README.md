# ansible-dns

![Build Status](https://travis-ci.org/snovichkov/ansible-dns.svg?branch=master)

Ansible role for configure DNS

Role Variables
--------------

* **dns_domain**: An Local domain name.
* **dns_options**: An list of certain internal resolver variables.
* **dns_sortlist**: The list of addresses sorting.
* **dns_searches**: An search list for host-name lookup.
* **dns_nameservers**: An list of name server IP address.

Dependencies
------------

None

Example Playbook
----------------

```
- hosts: "servers"
  roles:
    - role: "snovichkov.dns"
      dns_domain: "example.com"
      dns_nameservers:
        - "8.8.8.8"
        - "8.8.4.4"
        - "2001:4860:4860::8888"
        - "2001:4860:4860::8844"  
```

License
-------

[BSD](https://raw.githubusercontent.com/snovichkov/ansible-dns/master/LICENSE)
