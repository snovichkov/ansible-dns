# ansible-dns

![Build Status](https://travis-ci.org/snovichkov/ansible-dns.svg?branch=master)

Ansible role for configure DNS

Role Variables
--------------

* **dns_domain**: The Local domain name.
* **dns_options**: A list of certain internal resolver options
* **dns_sortlist**: The list of addresses sorting.
* **dns_searches**: A search list for host-name lookup.
* **dns_nameservers**: A list of name server IP address.

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
      dns_options: ['single-request-reopen']
```

License
-------

[BSD](https://raw.githubusercontent.com/snovichkov/ansible-dns/master/LICENSE)
