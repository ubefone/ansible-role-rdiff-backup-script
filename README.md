Rdiff-Backup Script Ansible Role
=========

Ansible Role configures an rdiff-backup script and list of servesr to backup up from ansible inventory.

Requirements
------------

rdiff-backup is included in the Ubuntu, Debian, and Fedora repos but CentOS 6 and 7 requires EPEL.

Role Variables
--------------

rdiff_backup_server: backupserver.example.com (required)
state: present (default) or absent
rdiff_backup_command: (optional, overrides default command)
rdiff_prune_command: (optional, overrides default command)

Dependencies
------------

none

Example Playbook
----------------

### Playbook

```
- hosts: servers
  roles:
    - { role: ahnooie.rdiff-backup-script }
```

### Inventory File

```
[servers]
servera.example.com rdiff_backup_server=backupserver.example.com state=present
serverb.example.com rdiff_backup_server=backupserver.example.com state=present
serverc.example.com rdiff_backup_server=backupserver.example.com state=present
```

License
-------

MIT

Author Information
------------------

Created by [Benjamin Bryan](http://b3n.org)
