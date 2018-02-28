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
    :alt: License: AGPL-3

Request SSL certificates from letsencrypt.org
=============================================

This module was written to have your Odoo installation request SSL certificates
from https://letsencrypt.org automatically.

Installation
------------





After installation, this module generates a private key for your account at
letsencrypt.org automatically in ``$data_dir/letsencrypt/account.key``. If you
want or need to use your own account key, replace the file.

For certificate requests to work, your site needs to be accessible via plain
HTTP, see below for configuration examples in case you force your clients to
the SSL version.

After installation, trigger the cronjob `Update letsencrypt certificates` and
watch your log for messages.

This addon depends on the ``openssl`` binary and the ``acme_tiny`` and ``IPy``
python modules. If you use https in your nginx or apache configuration,
openssl should already be installed.

If you still need to install the OpenSSL binary you can use your distro
package manager. For Debian and Ubuntu, that would be:

    sudo apt-get install openssl

For installing the ACME-Tiny python module, use the PIP package manager:

    sudo pip install acme-tiny

For installing the IPy python module, use the PIP package manager:

    sudo pip install IPy


Configuration
-------------





This addons requests a certificate for the domain named in the configuration
parameter ``web.base.url`` - if this comes back as ``localhost`` or the like,
the module doesn't request anything.

If you want your certificate to contain multiple alternative names, just add
them as configuration parameters ``letsencrypt.altname.N`` with ``N`` starting
from ``0``. The amount of domains that can be added are subject to `rate
limiting <https://community.letsencrypt.org/t/rate-limits-for-lets-encrypt/6769>`_.

Note that all those domains must be publicly reachable on port 80 via HTTP, and
they must have an entry for ``.well-known/acme-challenge`` pointing to your odoo
instance.

Usage
-----







=====

The module sets up a cronjob that requests and renews certificates automatically.

After the first run, you'll find a file called ``domain.crt`` in
``$datadir/letsencrypt``, configure your SSL proxy to use this file as certificate.

.. image:: https://odoo-community.org/website/image/ir.attachment/5784_f2813bd/datas
    :alt: Try me on Runbot
    :target: https://runbot.odoo-community.org/runbot/149/8.0

For further information, please visit:

* https://www.odoo.com/forum/help-1

In depth configuration

This module uses ``openssl`` to generate CSRs suitable to be submitted to
letsencrypt.org. In order to do this, it copies ``/etc/ssl/openssl.cnf`` to a
temporary and adapts it according to its needs (currently, that's just adding a
``[SAN]`` section if necessary). If you want the module to use another configuration
template, set config parameter ``letsencrypt.openssl.cnf``.

After refreshing the certificate, the module attempts to run the content of
``letsencrypt.reload_command``, which is by default ``sudo service nginx reload``.
Change this to match your server's configuration.

You'll also need a matching sudo configuration, like::

    your_odoo_user ALL = NOPASSWD: /usr/sbin/service nginx reload

The line above can be added to /etc/sudoers through the visudo command.

If your distribution supports it, like Debian does, you can create and edit
an automatically included file through
``visudo -f /etc/sudoers.d/letsencrypt``. This will also put the right
authorities on the file (-r--r-----).

The server that provides the certificates will try to check that you actually
control the host that you request a certificate for. It will do this by
requesting through http a file from an uri that contains
``/.well-known/acme-challenge/xxx``. The letsencrypt module provides a
controller that will provide this uri from the Odoo server, but we have to
configure the frontend nginx or apache server to accept http for these uri's.

Therefore, if you force users to https, you'll need something like this
for nginx::

    if ($scheme = "http") {
        set $redirect_https 1;
    }
    if ($request_uri ~ ^/.well-known/acme-challenge/) {
        set $redirect_https 0;
    }
    if ($redirect_https) {
        rewrite ^   https://$server_name$request_uri? permanent;
    }

and this for apache::

    RewriteEngine On
    RewriteCond %{HTTPS} !=on
    RewriteCond %{REQUEST_URI} "!^/.well-known/"
    RewriteRule ^/?(.*) https://%{SERVER_NAME}/$1 [R,L]

In case you need to redirect other nginx sites to your Odoo instance, declare
an upstream for your odoo instance and do something like::

    location /.well-known {
        proxy_pass    http://yourodooupstream;
    }

If you're using a multi-database installation (with or without dbfilter option)
where /web/databse/selector returns a list of more than one database, then
you need to add ``letsencrypt`` addon to serverwide load addons list
(by default, only ``web`` addon), setting ``--load`` option.
For example, ``--load=web,letsencrypt``


Known issues / Roadmap
----------------------




Bug Tracker
-----------





Bugs are tracked on `GitHub Issues <https://github.com/OCA/server-tools/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smashing it by providing a detailed and welcomed feedback
`here <https://github.com/OCA/server-tools/issues/new?body=module:%20letsencrypt%0Aversion:%208.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Credits
-------









### Contributors





* Holger Brunn <hbrunn@therp.nl>
* Antonio Espinosa <antonio.espinosa@tecnativa.com>

ACME implementation

* https://github.com/diafygi/acme-tiny/blob/master/acme_tiny.py

Icon
----

* https://helloworld.letsencrypt.org

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
