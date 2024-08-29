===========================================
|icon| Let's Encrypt/letsencrypt 10.0.2.0.1
===========================================

**Request SSL certificates from letsencrypt.org**

.. |icon| image:: https://raw.githubusercontent.com/zeroincombenze/server-tools/10.0/letsencrypt/static/description/icon.png


.. contents::



Overview | Panoramica
=====================

|en| This module was written to have your Odoo installation request SSL certificates
from https://letsencrypt.org automatically.


|it| Nessuna informazione disponibile

|thumbnail|

.. |thumbnail| image:: https://raw.githubusercontent.com/zeroincombenze/server-tools/10.0/letsencrypt/static/description/


Configuration | Configurazione
------------------------------

This addons requests a certificate for the domain named in the configuration
parameter ``web.base.url`` - if this comes back as ``localhost`` or the like,
the module doesn't request anything.

Futher self-explanatory settings are in Settings -> General Settings. There you
can add further domains to the CSR, add a custom script that updates your DNS
and add a script that will be used to reload your web server (if needed).
The number of domains that can be added to a certificate is
`capped at 100 <https://letsencrypt.org/docs/rate-limits/>`_. A wildcard
certificate can be used to avoid that limit.

Note that all those domains must be publicly reachable on port 80 via HTTP, and
they must have an entry for ``.well-known/acme-challenge`` pointing to
``$datadir/letsencrypt/acme-challenge`` of your odoo instance.

Since DNS changes can take some time to propagate, when we respond to a DNS challenge
and the server tries to check our response, it might fail (and probably will).
The solution to this is documented in https://tools.ietf.org/html/rfc8555#section-8.2
and basically is a ``Retry-After`` header under which we can instruct the server to
retry the challenge.
At the time these lines were written, Boulder had not implemented this functionality.
This prompted us to use ``letsencrypt.backoff`` configuration parameter, which is the
amount of minutes this module will try poll the server to retry validating the answer
to our challenge, specifically it is the ``deadline`` parameter of ``poll_and_finalize``.



Usage | Utilizzo
----------------

The module sets up a cronjob that requests and renews certificates automatically.

Certificates are renewed a month before they expire. Renewal is then attempted
every day until it succeeds.

After the first run, you'll find a file called ``domain.crt`` in
``$datadir/letsencrypt``, configure your SSL proxy to use this file as certificate.

In depth configuration
~~~~~~~~~~~~~~~~~~~~~~

If you want to use multiple domains on your CSR then you have to configure them
from Settings -> General Settings. If you use a wildcard in any of those domains
then letsencrypt will return a DNS challenge. In order for that challenge to be
answered you will need to **either** provide a script (as seen in General Settings)
or install a module that provides support for your DNS provider. In that module
you will need to create a function in the letsencrypt model with the name
``_respond_challenge_dns_$DNS_PROVIDER`` where ``$DNS_PROVIDER`` is the name of your
provider and can be any string with length greater than zero, and add the name
of your DNS provider in the settings dns_provider selection field.

In any case if a script path is inserted in the settings page, it will be run
in case you want to update multiple DNS servers.

A reload command can be set in the Settings as well in case you need to reload
your web server. This by default is ``sudo /usr/sbin/service nginx reload``


You'll also need a matching sudo configuration, like::

    your_odoo_user ALL = NOPASSWD: /usr/sbin/service nginx reload

Further, if you force users to https, you'll need something like for nginx::

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
you need to add ``letsencrypt`` addon to wide load addons list
(by default, only ``web`` addon), setting ``--load`` option.
For example, ``--load=web,letsencrypt``



Getting started | Primi passi
=============================

|Try Me|


Prerequisites | Prerequisiti
----------------------------

* python 2.7+ (best 2.7.5+)
* postgresql 9.2+ (best 9.5)

::

    cd $HOME
    # Follow statements activate deployment, installation and upgrade tools
    cd $HOME
    [[ ! -d ./tools ]] && git clone https://github.com/zeroincombenze/tools.git
    cd ./tools
    ./install_tools.sh -pUT
    source $HOME/devel/activate_tools



Installation | Installazione
----------------------------

+---------------------------------+------------------------------------------+
| |en|                            | |it|                                     |
+---------------------------------+------------------------------------------+
| These instructions are just an  | Istruzioni di esempio valide solo per    |
| example; use on Linux CentOS 7+ | distribuzioni Linux CentOS 7+,           |
| Ubuntu 14+ and Debian 8+        | Ubuntu 14+ e Debian 8+                   |
|                                 |                                          |
| Installation is built with:     | L'installazione è costruita con:         |
+---------------------------------+------------------------------------------+
| `Zeroincombenze Tools <https://zeroincombenze-tools.readthedocs.io/>`__ |
+---------------------------------+------------------------------------------+
| Suggested deployment is:        | Posizione suggerita per l'installazione: |
+---------------------------------+------------------------------------------+
| $HOME/10.0 |
+----------------------------------------------------------------------------+

::

    # Odoo repository installation; OCB repository must be installed
    deploy_odoo clone -r server-tools -b 10.0 -G zero -p $HOME/10.0
    # Upgrade virtual environment
    vem amend $HOME/10.0/venv_odoo



Upgrade | Aggiornamento
-----------------------

::

    deploy_odoo update -r server-tools -b 10.0 -G zero -p $HOME/10.0
    vem amend $HOME/10.0/venv_odoo
    # Adjust following statements as per your system
    sudo systemctl restart odoo



Support | Supporto
------------------

|Zeroincombenze| This module is supported by the `SHS-AV s.r.l. <https://www.zeroincombenze.it/>`__



Get involved | Ci mettiamo in gioco
===================================

Bug reports are welcome! You can use the issue tracker to report bugs,
and/or submit pull requests on `GitHub Issues
<https://github.com/zeroincombenze/server-tools/issues>`_.

In case of trouble, please check there if your issue has already been reported.



Proposals for enhancement
-------------------------

|en| If you have a proposal to change this module, you may want to send an email to <cc@shs-av.com> for initial feedback.
An Enhancement Proposal may be submitted if your idea gains ground.

|it| Se hai proposte per migliorare questo modulo, puoi inviare una mail a <cc@shs-av.com> per un iniziale contatto.



Credits | Ringraziamenti
========================

Copyright
---------

Odoo is a trademark of `Odoo S.A. <https://www.odoo.com/>`__ (formerly OpenERP)


Authors | Autori
----------------

* Therp BV <False>
* Tecnativa <False>
* `Odoo Community Association (OCA) <https://odoo-community.org>`__
* `SHS-AV s.r.l. <https://www.zeroincombenze.it>`__



Contributors | Partecipanti
---------------------------

* `Holger Brunn <mail@hunki-enterprises.nl>`__
* `Antonio Espinosa <antonio.espinosa@tecnativa.com>`__
* `Dave Lasley <dave@laslabs.com>`__
* `Ronald Portier <ronald@therp.nl>`__
* `George Daramouskas <gdaramouskas@therp.nl>`__
* `Jan Verbeek <jverbeek@therp.nl>`__
* Other credits <False>
* ~~~~~~~~~~~~~ <False>
* ACME implementation <False>
* ~~~~~~~~~~~~~~~~~~~ <False>
* https://github.com/certbot/certbot/tree/0.22.x/acme <False>
* Icon <False>
* ~~~~ <False>
* https://helloworld.letsencrypt.org <False>
* Maintainers <False>
* ~~~~~~~~~~~ <False>
* This module is maintained by the OCA. <False>
* .. image:: https://odoo-community.org/logo.png <False>
* :alt: Odoo Community Association <False>
* :target: https://odoo-community.org <False>
* OCA, or the Odoo Community Association, is a nonprofit organization whose <False>
* mission is to support the collaborative development of Odoo features and <False>
* promote its widespread use. <False>
* `This module is part of the OCA/server-tools <https://github.com/OCA/server-tools/tree/10.0/letsencrypt>`__
* You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute. <False>



Acknowledges | Riconoscimenti
-----------------------------

ACME implementation
~~~~~~~~~~~~~~~~~~~

* https://github.com/certbot/certbot/tree/0.22.x/acme

Icon
~~~~

* https://helloworld.letsencrypt.org



Sponsor
-------

ACME implementation
~~~~~~~~~~~~~~~~~~~

* https://github.com/certbot/certbot/tree/0.22.x/acme

Icon
~~~~

* https://helloworld.letsencrypt.org



Maintainer | Manutenzione
-------------------------

* `Antonio M. Vigliotti <antoniomaria.vigliotti@gmail.com>`__



----------------

|en| **zeroincombenze®** is a trademark of `SHS-AV s.r.l. <https://www.shs-av.com/>`__
which distributes and promotes ready-to-use **Odoo** on own cloud infrastructure.
`Zeroincombenze® distribution of Odoo <https://www.zeroincombenze.it/>`__
is mainly designed to cover Italian law and markeplace.

|it| **zeroincombenze®** è un marchio registrato da `SHS-AV s.r.l. <https://www.shs-av.com/>`__
che distribuisce e promuove **Odoo** pronto all'uso sulla propria infrastuttura.
La distribuzione `Zeroincombenze® <https://www.zeroincombenze.it/>`__ è progettata per le esigenze del mercato italiano.


|
|

This module is part of server-tools project.

Last Update / Ultimo aggiornamento: 2024-08-29

.. |Maturity| image:: https://img.shields.io/badge/maturity-Alfa-black.png
    :target: https://odoo-community.org/page/development-status
    :alt: 
.. |license gpl| image:: https://img.shields.io/badge/licence-LGPL--3-7379c3.svg
    :target: http://www.gnu.org/licenses/lgpl-3.0-standalone.html
    :alt: License: LGPL-3
.. |license opl| image:: https://img.shields.io/badge/licence-OPL-7379c3.svg
    :target: https://www.odoo.com/documentation/user/14.0/legal/licenses/licenses.html
    :alt: License: OPL
.. |Try Me| image:: https://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-10.svg
    :target: https://erp10.zeroincombenze.it
    :alt: Try Me
.. |Zeroincombenze| image:: https://avatars0.githubusercontent.com/u/6972555?s=460&v=4
   :target: https://www.zeroincombenze.it/
   :alt: Zeroincombenze
.. |en| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/flags/en_US.png
   :target: https://www.facebook.com/Zeroincombenze-Software-gestionale-online-249494305219415/
.. |it| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/flags/it_IT.png
   :target: https://www.facebook.com/Zeroincombenze-Software-gestionale-online-249494305219415/
.. |check| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/check.png
.. |no_check| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/no_check.png
.. |menu| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/menu.png
.. |right_do| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/right_do.png
.. |exclamation| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/exclamation.png
.. |warning| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/warning.png
.. |same| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/same.png
.. |late| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/late.png
.. |halt| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/halt.png
.. |info| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/info.png
.. |xml_schema| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/certificates/iso/icons/xml-schema.png
   :target: https://github.com/zeroincombenze/grymb/blob/master/certificates/iso/scope/xml-schema.md
.. |DesktopTelematico| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/certificates/ade/icons/DesktopTelematico.png
   :target: https://github.com/zeroincombenze/grymb/blob/master/certificates/ade/scope/Desktoptelematico.md
.. |FatturaPA| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/certificates/ade/icons/fatturapa.png
   :target: https://github.com/zeroincombenze/grymb/blob/master/certificates/ade/scope/fatturapa.md
