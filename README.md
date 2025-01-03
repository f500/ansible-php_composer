php_composer
============

Install [Composer](https://getcomposer.org/), the dependency manager for PHP.

Requirements
------------

This role is tailored towards Debian Bullseye / Bookworm.

The packages `python-apt` (or `python3-apt`) must be installed.

In addition, it is assumed that the PHP CLI is already installed.

Role Variables
--------------

Specify the path where Composer will be installed:

    php_composer_install_path: /usr/local/bin/composer.phar

Specify a fixed version of composer that you want to install (defaults to `~`, which means the latest stable)

    php_composer_version: 1.10.17

Composer relies on the INI directive `allow_url_fopen` turned on, and uses the `proc_open()` function.
This goes against configuration best practices, so chances are Composer won't work in all circumstances.

Another common issue is a memory limit, which is hit when computing a dependency graph.

In order to have Composer function in all (or at least most) cases, a wrapper-script is installed.
The following variables control how this wrapper functions:

    php_composer_wrapper_enabled: yes
    php_composer_wrapper_path: /usr/local/bin/composer
    php_composer_wrapper_ini_directives:
      allow_url_fopen: yes
      disable_functions: ""
      memory_limit: -1

Dependencies
------------

None.

Example Playbook
-------------------------

    - hosts: servers
      roles:
        - { role: f500.php_composer, php_composer_install_path: /usr/local/bin/composer, php_composer_wrapper_enabled: no }

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

Copyright (C) 2017 Future500 B.V.

[LGPL-3.0](https://github.com/f500/ansible-php_composer/blob/master/COPYING.LESSER)

Author Information
------------------

Jasper N. Brouwer, jasper@future500.nl

Ramon de la Fuente, ramon@future500.nl
