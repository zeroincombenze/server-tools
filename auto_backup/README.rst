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

Database Auto-Backup
====================

A tool for all your back-ups, internal and external!

Installation
------------






Before installing this module, you need to execute::

    pip install pysftp

Configuration
-------------






Go to *Settings -> Configuration -> Configure Backup* to
create your configurations for each database that you needed
to backups.

Usage
-----






=====

Keep your Odoo data safe with this module. Take automated back-ups,
remove them automatically and even write them to an external server
through an encrypted tunnel. You can even specify how long local backups
and external backups should be kept, automatically!

Connect with an FTP Server

Keep your data safe, through an SSH tunnel!
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Want to go even further and write your backups to an external server?
You can with this module! Specify the credentials to the server, specify
a path and everything will be backed up automatically. This is done
through an SSH (encrypted) tunnel, thanks to pysftp, so your data is
safe!

Test connection

Checks your credentials in one click
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Want to make sure if the connection details are correct and if Odoo can
automatically write them to the remote server? Simply click on the ‘Test
SFTP Connection’ button and you will get message telling you if
everything is OK, or what is wrong!

E-mail on backup failure

Stay informed of problems, automatically!
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Do you want to know if the database backup succeeded or failed? Subscribe to
the corresponding backup setting notification type.

Run backups when you want

From the backups configuration list, press *More > Execute backup(s)* to
manually execute the selected processes.

.. image:: https://odoo-community.org/website/image/ir.attachment/5784_f2813bd/datas
   :alt: Try me on Runbot
   :target: https://runbot.odoo-community.org/runbot/149/9.0

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






* Yenthe Van Ginneken <yenthe.vanginneken@vanroey.be>
* Alessio Gerace <alessio.gerace@agilebg.com>
* Jairo Llopis <yajo.sk8@gmail.com>
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
