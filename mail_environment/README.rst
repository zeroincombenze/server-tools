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

Mail configuration with server_environment
==========================================

This module allows to configure the incoming and outgoing mail servers
using the `server_environment` mechanism: you can then have different
mail servers for the production and the test environment.

Installation
------------






To install this module, you need to have the server_environment module
installed and properly configured.

Configuration
-------------






With this module installed, the incoming and outgoing mail servers are
configured in the `server_environment_files` module (which is a module
you should provide, see the documentation of `server_environment` for
more information).

In the configuration file of each environment, you may first use the
sections `[outgoing_mail]` and `[incoming_mail]` to configure the
default values respectively for SMTP servers and the IMAP/POP servers.

Then for each server, you can define additional values or override the
default values with a section named `[outgoing_mail.resource_name]` or
`[incoming_mail.resource_name]` where "resource_name" is the name of
the server.

Exemple of config file :

[outgoing_mail]
smtp_host = smtp.myserver.com
smtp_port = 587
smtp_user =
smtp_pass =
smtp_encryption = ssl

[outgoing_mail.odoo_smtp_server1]
smtp_user = odoo
smtp_pass = odoo

[incoming_mail.odoo_pop_mail1]
server = mail.myserver.com
port = 110
type = pop
is_ssl = 0
attach = 0
original = 0
user = odoo@myserver.com
password = uas1ohV0

You will need to create 2 records in the database, one outgoing mail
server with the field `name` set to "odoo_smtp_server1" and one
incoming mail server with the field `name` set to "odoo_pop_mail1".


Usage
-----






=====

Once configured, Odoo will read the mail servers values from the
configuration file related to each environment defined in the main
Odoo file.


Known issues / Roadmap
----------------------






* Due to the special nature of this addon, you cannot test it on the OCA
runbot.

Bug Tracker
-----------






Bugs are tracked on `GitHub Issues
<https://github.com/OCA/server-tools/issues>`_. In case of trouble, please
check there if your issue has already been reported. If you spotted it first,
help us smashing it by providing a detailed and welcomed `feedback
<https://github.com/OCA/
server-tools/issues/new?body=module:%20
mail_environment%0Aversion:%20
9.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Credits
-------






Images

* Odoo Community Association: `Icon <https://github.com/OCA/maintainer-tools/blob/master/template/module/static/description/icon.svg>`_.






### Contributors






* Nicolas Bessi <nicolas.bessi@camptocamp.com>
* Yannick Vaucher <yannick.vaucher@camptocamp.com>
* Guewen Baconnier <guewen.baconnier@camptocamp.com>
* Joël Grand-Guillaume <joel.grandguillaume@camptocamp.com>
* Holger Brunn <hbrunn@therp.nl>
* Alexandre Fayolle <alexandre.fayolle@camptocamp.com>

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
