systl
=====

A quick ansible role to persist sysctls on Linux in memory and on disk.

Role Variables
--------------

Takes a list of dictionaries of key-value pairs called _sysctls_:

```
sysctls:
    - key: net.ipv4.ip_forward
      value: 1
```

It also supports specifying the sysctl file using a variable called sysctl_file, which overrides the default sysctl.conf/sysctl.d filename (_/etc/sysctl.d/99-custom-sysctls.conf_).

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: mattgeddes.sysctl, sysctls: [ { "key": "net.ipv4.ip_forward", "value": "1" } ] }

License
-------

Apache-2.0

