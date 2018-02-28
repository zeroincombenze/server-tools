[![Build Status](https://travis-ci.org/zeroincombenze/server-tools.svg?branch=8.0)](https://travis-ci.org/zeroincombenze/server-tools)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/server-tools/badge.svg?branch=8.0)](https://coveralls.io/github/zeroincombenze/server-tools?branch=8.0)
[![codecov](https://codecov.io/gh/zeroincombenze/server-tools/branch/8.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/server-tools/branch/8.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-8.svg)](https://github.com/OCA/server-tools/tree/8.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-8.svg)](http://erp8.zeroincombenze.it)


































[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

.. image:: https://img.shields.io/badge/licence-AGPL--3-blue.svg
    :alt: License

Tracks Authentication Attempts and Prevents Brute-force Attacks
===============================================================

This module registers each request done by users trying to authenticate into
Odoo. If the authentication fails, a counter is increased for the given remote
IP. After a defined number of attempts, Odoo will ban the remote IP and
ignore new requests.
This module applies security through obscurity
(https://en.wikipedia.org/wiki/Security_through_obscurity),
When a user is banned, the request is now considered as an attack. So, the UI
will **not** indicate to the user that his IP is banned and the regular message
'Wrong login/password' is displayed.

This module realizes a call to a web API (http://ip-api.com) to try to have
extra information about remote IP.

Known issue / Roadmap
The ID used to identify a remote request is the IP provided in the request
(key 'REMOTE_ADDR').
Depending of server and / or user network configuration, the idenfication
of the user can be wrong, and mainly in the following cases:

* if the Odoo server is behind an Apache / NGinx proxy without redirection,
  all the request will be have the value '127.0.0.1' for the REMOTE_ADDR key;
* If some users are behind the same Internet Service Provider, if a user is
  banned, all the other users will be banned too;

Installation
------------




Configuration
-------------





Once installed, you can change the ir.config_parameter value for the key
'auth_brute_force.max_attempt_qty' (10 by default) that define the max number
of attempts allowed before the user was banned.

Usage
-----








Admin user have the possibility to unblock a banned IP.

Logging

This module generates some WARNING logs, in the three following cases:

* Authentication failed from remote '127.0.0.1'. Login tried : 'admin'.
  Attempt 1 / 10.

* Authentication failed from remote '127.0.0.1'. The remote has been banned.
  Login tried : 'admin'.

* Authentication tried from remote '127.0.0.1'. The request has been ignored
  because the remote has been banned after 10 attempts without success. Login
  tried : 'admin'.

Screenshot

**List of Attempts**

.. image:: /auth_brute_force/static/description/screenshot_attempts_list.png

**Detail of a banned IP**

.. image:: /auth_brute_force/static/description/screenshot_custom_ban.png


=====

* go to ...

.. image:: https://odoo-community.org/website/image/ir.attachment/5784_f2813bd/datas
   :alt: Try me on Runbot
   :target: https://runbot.odoo-community.org/runbot/149/8.0

For further information, please visit:

* https://www.odoo.com/forum/help-1

Known issues / Roadmap
----------------------




Bug Tracker
-----------





Bugs are tracked on `GitHub Issues <https://github.com/OCA/web/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smashing it by providing a detailed and welcomed feedback
`here <https://github.com/OCA/web/issues/new?body=module:%20auth_brute_force%0Aversion:%208.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Credits
-------









### Contributors





* Sylvain LE GAL (https://twitter.com/legalsylvain)

### Funders

### Maintainer








.. image:: http://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: http://odoo-community.org

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
