borg-repo
=========

Borg Backup repository to store remote backups from other hosts.

Requirements
------------

None.

Role Variables
--------------

- `borg_user` & `borg_group` define which account will run `borg serve` and own the resulting files
- `borg_home` defines the homedir, and `borg_pool` defines the directory that will hold all backup repos 
- `borg_auth_users` is a list, where each item defines an authorized backup user. The default values are placeholders and should be replaced.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: backup-repo
      pre_tasks:
        - import_vars: borg_auth_users
      roles:
         - { role: thinkmassive.borg-repo }

License
-------

Apache

Author Information
------------------

Alexander Miller alex@thinkmassive.org
