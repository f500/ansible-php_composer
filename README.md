php_composer
========

Install ComposerPHP

Requirements
------------

Debian Wheezy with the package python-pycurl and python-software-properties installed.

Dependencies
------------

Depends on f500.php, f500.php_cli.

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - { role: f500.php_composer }

License
-------

LGPL

Author Information
------------------

Jasper N. Brouwer, jasper@nerdsweide.nl

Ramon de la Fuente, ramon@delafuente.nl
