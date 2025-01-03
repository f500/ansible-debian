Debian
========

This role installs these packages:

* curl
* python-pycurl/python3-pycurl
* python-configparser/python3-configargparse

It adds debian backports repos. 

It also runs apt-get update when it was run, last time, more than `{{ debian_cache_valid_time }}` seconds ago.

Requirements
------------

Debian Bullseye/Bookworm.

Role Variables
--------------

    debian_cache_update: yes
    debian_cache_valid_time: 14400
    debian_codename: '{{ ansible_distribution_release }}' ('wheezy', 'jessie', 'stretch', 'buster', 'bullseye')
    debian_codename: '{{ ansible_distribution_release }}'

Be aware that `debian_codename` defaults on `{{ ansible_distribution_release }}` so, most of the chances, you don't need to specify it.


Dependencies
-------------------------

None

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - { role: f500.debian }

Linting
-------
Github actions will check this role with ansible-lint. To run this locally, you will need to follow the following steps:

```bash
brew install ansible-lint
brew install yamllint
ansible-lint
```

to fix the linting errors, run:

```bash
ansible-lint --fix
```

License
-------

LGPL-3.0

Author Information
------------------

Jasper N. Brouwer, jasper@nerdsweide.nl

Ramon de la Fuente, ramon@delafuente.nl
