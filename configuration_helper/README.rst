[![Build Status](https://travis-ci.org/zeroincombenze/server-tools.svg?branch=9.0)](https://travis-ci.org/zeroincombenze/server-tools)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/server-tools/badge.svg?branch=9.0)](https://coveralls.io/github/zeroincombenze/server-tools?branch=9.0)
[![codecov](https://codecov.io/gh/zeroincombenze/server-tools/branch/9.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/server-tools/branch/9.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-9.svg)](https://github.com/OCA/server-tools/tree/9.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-9.svg)](http://wiki.zeroincombenze.org/en/Odoo/9.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-9.svg)](http://wiki.zeroincombenze.org/en/Odoo/9.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-9.svg)](http://erp9.zeroincombenze.it)




































[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

   :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
   :alt: License: AGPL-3

Installation
============






















Installation
------------

Configuration
-------------






*This module is intended for developer only. It does nothing used alone.*

It helps to create `config.settings` by providing an abstract Class.

This class:

  * creates automatically related fields in 'whatiwant.config.settings'
    using those defined in 'res.company': it avoids duplicated field definitions.
  * company_id field with default value is created
  * onchange_company_id is defined to update all related fields
  * supported fields: char, text, integer, float, datetime, date, boolean, m2o


How to use

.. code-block:: python

    from . company import ResCompany

    class WhatiwantClassSettings(orm.TransientModel):
        _inherit = ['res.config.settings', 'abstract.config.settings']
        _name = 'whatiwant.config.settings'
        # fields must be defined in ResCompany class
        # related fields are automatically generated from previous definitions
        _companyObject = ResCompany
        # all prefixed field with _prefix in res.company, will be available in 'whatiwant.config.settings' model
        _prefix = 'prefixyouchoose_'


Roadmap
  * support (or check support) for these field types : o2m, m2m, reference, property, selection
  * automatically generate a default view for 'whatiwant.config.settings' (in --debug ?)

Usage
-----






Known issues / Roadmap
----------------------





Bug Tracker
-----------






Bugs are tracked on `GitHub Issues
<https://github.com/OCA/server-tools/issues>`_. In case of trouble, please
check there if your issue has already been reported. If you spotted it first,
help us smashing it by providing a detailed and welcomed feedback.

Credits
-------










### Contributors






* Yannick Vaucher <yannick.vaucher@camptocamp.com>
* David BEAL <david.beal@akretion.com>
* Sébastien BEAU <sebastien.beau@akretion.com>

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
