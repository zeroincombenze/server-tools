[![Build Status](https://travis-ci.org/zeroincombenze/server-tools.svg?branch=9.0)](https://travis-ci.org/zeroincombenze/server-tools)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/server-tools/badge.svg?branch=9.0)](https://coveralls.io/github/zeroincombenze/server-tools?branch=9.0)
[![codecov](https://codecov.io/gh/zeroincombenze/server-tools/branch/9.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/server-tools/branch/9.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-9.svg)](https://github.com/OCA/server-tools/tree/9.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-9.svg)](http://wiki.zeroincombenze.org/en/Odoo/9.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-9.svg)](http://wiki.zeroincombenze.org/en/Odoo/9.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-9.svg)](http://erp9.zeroincombenze.it)


































[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

.. image:: https://img.shields.io/badge/license-LGPL--3-blue.svg
   :target: http://www.gnu.org/licenses/lgpl-3.0-standalone.html
   :alt: License: LGPL-3

Password Security
=================

This module allows admin to set company-level password security requirements
and enforces them on the user.

It contains features such as

* Password expiration days
* Password length requirement
* Password minimum number of lowercase letters
* Password minimum number of uppercase letters
* Password minimum number of numbers
* Password minimum number of special characters

Installation
------------





Configuration
-------------






# Navigate to company you would like to set requirements on
# Click the ``Password Policy`` page
# Set the policies to your liking.

Password complexity requirements will be enforced upon next password change for
any user in that company.


Settings & Defaults

These are defined at the company level:

 Name                  Default   Description                             
 password_expiration   60        Days until passwords expire
 password_length       12        Minimum number of characters in password
 password_lower        True      Require lowercase letter in password
 password_upper        True      Require uppercase letters in password
 password_numeric      True      Require number in password
 password_special      True      Require special character in password
 password_history      30        Disallow reuse of this many previous passwords
 password_minimum      24        Amount of hours that must pass until another reset

Known Issues / Roadmap


Usage
-----






Known issues / Roadmap
----------------------





Bug Tracker
-----------






Bugs are tracked on `GitHub Issues
<https://github.com/LasLabs/odoo-base/issues>`_. In case of trouble, please
check there if your issue has already been reported. If you spotted it first,
help us to smash it by providing detailed and welcomed feedback.


Credits
-------






Images

* Odoo Community Association: `Icon <https://github.com/OCA/maintainer-tools/blob/master/template/module/static/description/icon.svg>`_.






### Contributors






* James Foster <jfoster@laslabs.com>
* Dave Lasley <dave@laslabs.com>

### Funders

### Maintainer










.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

This module is maintained by the OCA.

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

To contribute to this module, please visit https://odoo-community.org.

[//]: # (copyright)

----

**Odoo** is a trademark of [Odoo S.A.](https://www.odoo.com/) (formerly OpenERP, formerly TinyERP)

**OCA**, or the [Odoo Community Association](http://odoo-community.org/), is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

**zeroincombenze®** is a trademark of [SHS-AV s.r.l.](http://www.shs-av.com/)
which distributes and promotes **Odoo** ready-to-use on its own cloud infrastructure.
[Zeroincombenze® distribution](http://wiki.zeroincombenze.org/en/Odoo)
is mainly designed for Italian law and markeplace.
Everytime, every Odoo DB and customized code can be deployed on local server too.

[//]: # (end copyright)

[//]: # (addons)

[//]: # (end addons)

[![chat with us](https://www.shs-av.com/wp-content/chat_with_us.gif)](https://tawk.to/85d4f6e06e68dd4e358797643fe5ee67540e408b)
