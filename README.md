php_composer
============

Install [Composer](https://getcomposer.org/), the dependency manager for PHP.

Requirements
------------

This role is tailored towards Debian Wheezy / Jessie.

The packages `python-apt` (or `python3-apt`) must be installed.

In addition, it is assumed that the PHP CLI is already installed.

Role Variables
--------------

Specify the path where Composer will be installed:

    php_composer_install_path: /usr/local/bin/composer

Dependencies
------------

None.

Example Playbook
-------------------------

    - hosts: servers
      roles:
        - { role: f500.php_composer, php_composer_install_path: /bin/composer }

License
-------

Copyright (C) 2017 Future500 B.V.

[LGPL-3.0](https://github.com/f500/ansible-php_composer/blob/master/COPYING.LESSER)

Author Information
------------------

Jasper N. Brouwer, jasper@future500.nl

Ramon de la Fuente, ramon@future500.nl
