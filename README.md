php_composer
========

Install ComposerPHP

Requirements
------------

Debian Wheezy/Jessie with the package python-pycurl and python-software-properties installed.
In addition, it is assumed that the PHP-cli is already installed.

Dependencies
------------

None.

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
