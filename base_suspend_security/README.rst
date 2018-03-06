[![Build Status](https://travis-ci.org/zeroincombenze/server-tools.svg?branch=9.0)](https://travis-ci.org/zeroincombenze/server-tools)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/server-tools/badge.svg?branch=9.0)](https://coveralls.io/github/zeroincombenze/server-tools?branch=9.0)
[![codecov](https://codecov.io/gh/zeroincombenze/server-tools/branch/9.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/server-tools/branch/9.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-9.svg)](https://github.com/OCA/server-tools/tree/9.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-9.svg)](http://wiki.zeroincombenze.org/en/Odoo/9.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-9.svg)](http://wiki.zeroincombenze.org/en/Odoo/9.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-9.svg)](http://erp9.zeroincombenze.it)




































[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

    :alt: License: AGPL-3
Suspend security
================

This module was written to  allow you to call code with some `uid` while being sure no security checks (`ir.model.access` and `ir.rule`) are done. In this way, it's the same as `sudo()`, but the crucial difference is that the code still runs with the original user id. This can be important for inherited code that calls workflow functions, subscribes the current user to some object, etc.

Usually, you'll be in in the situation to want something like this if you inherit from a module you can't or don't want to change, and call `super()`.

Installation
------------





Configuration
-------------





Usage
-----






=====

To use this module, you need to:

* depend on this module
* call `yourmodel.suspend_security().function_to_run()`, just the same as you would use `sudo()`

For further information, please visit:

* https://www.odoo.com/forum/help-1

Known issues / Roadmap
----------------------






* the magic works by wrapping uid in a marker class, so if some code unwraps this in the calling tree, security checks will be reenabled

Bug Tracker
-----------






Bugs are tracked on `GitHub Issues <https://github.com/OCA/server-tools/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smashing it by providing a detailed and welcomed feedback
`here <https://github.com/OCA/server-tools/issues/new?body=module:%20base_suspend_security%0Aversion:%208.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Credits
-------











### Contributors






* Holger Brunn <hbrunn@therp.nl>
* Laurent Mignon <laurent.mignon@acsone.eu>

### Funders

### Maintainer










.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

This module is maintained by the OCA.

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

To contribute to this module, please visit http://odoo-community.org.

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
