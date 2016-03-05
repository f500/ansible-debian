Debian
========

This role installs these packages:

* curl
* python-pycurl
* python-configparser

It adds debian backports repos. 

It also runs apt-get update when it was run, last time, more than `{{ debian_cache_valid_time }}` seconds ago.

Requirements
------------

Debian Wheezy or Jessie.

Role Variables
--------------

    debian_cache_valid_time: 14400
    debian_codename: "wheezy" (default) or "jessie" or '{{ ansible_distribution_release }}'
    debian_repo_url: 'ftp.us.debian.org'

Be aware that `debian_codename` defaults on `{{ ansible_distribution_release }}` so, most of the chances, you don't need to specify it.


Dependencies
-------------------------

None

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
