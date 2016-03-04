Debian
========

Some base-tasks (for debian)

Requirements
------------

Debian Wheezy/Jessie with the package python-pycurl and python-software-properties installed.

Role Variables
--------------

    debian_cache_valid_time: 14400
    debian_codename: "wheezy" (default) or "jessie" or '{{ ansible_distribution_release }}'

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - { role: f500.debian }

License
-------

LGPL

Author Information
------------------

Jasper N. Brouwer, jasper@nerdsweide.nl

Ramon de la Fuente, ramon@delafuente.nl
