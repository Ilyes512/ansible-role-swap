Swap (Ansidev)
=========
[![Build Status](https://travis-ci.org/Ilyes512/ansible-role-swap.svg)](https://travis-ci.org/Ilyes512/ansible-role-swap)

This role configure's Swap for Ubuntu Trusty (14.04) and Xenial (16.04).

Requirements
------------

No requirements.

Role Variables
--------------

```
swap_use_dd: false # false = fallocate
swap_location: /swapfile
swap_size_mb: 1024 # Dont use any suffix like mb/MB/MiB
swap_swappiness: 10
swap_cache_pressure: 50
```

Dependencies
------------

No dependencies.

Example Playbook
----------------
```
- hosts: servers
  vars_files:
    - vars/main.yml
  roles:
    - { role: ilyes512.swap, tag: ansidev.swap }
```

Inside `vars/main.yml`:

```
swap_size_mb: 2048
```

*Note: A good guideline for determining the Swap size is by taking your machine's RAM size and multiplying it
by two. For example if you got a 512 MB VM you would set it to 1024 MB Swap.*

License
-------

MIT

Author Information
------------------

Ilyes Ahidar [@Ilyes512](https://twitter.com/ilyes512)
