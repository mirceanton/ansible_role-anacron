Ansible Role: Anacron
=====================

An Ansible role that installs anacron and configures jobs.

Requirements
------------

N/A

Role Variables
--------------

- `anacron_jobs`: a list of jobs to be added to the anacrontab

To check the default variables, take a look at the [defaults](defaults/main.yml) file.

Dependencies
------------

N/A

Example Playbook
----------------

``` yml
---
- hosts: all
  remote_user: root

  roles:
    - role: mirceanton.anacron
      vars:
        anacron_jobs:
          - 1 1 backup /home/me/myscripts/backup.sh
```

License
-------

MIT

Author Information
------------------

A role developed by [Mircea-Pavel ANTON](https://www.mirceanton.com).
