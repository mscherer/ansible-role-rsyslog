Ansible module used by OSAS to manage rsyslog.

[![Build Status](https://travis-ci.org/OSAS/ansible-role-rsyslog.svg?branch=master)](https://travis-ci.org/OSAS/ansible-role-rsyslog)

This role requires a dogtag instance, like the one setup by IPA in order to 
manage the TLS certificates used to export the log over TLS.

# Example

This role can be used like this:

```
$ cat deploy_rsyslog.yml
- hosts: all
  roles:
  - role: rsyslog
    syslog_server: syslog.example.org
```

The role will detect it is running on the syslog server, and install 
all the configuration required for the master there.

# Location of the logs

The log by default are placed in /srv/logs/. The directory must be created manually
before use on the main server, and cannot be configured for now.
