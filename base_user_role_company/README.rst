==============================================================
|icon| User roles by company/base_user_role_company 10.0.1.0.0
==============================================================

.. |icon| image:: https://raw.githubusercontent.com/zeroincombenze/server-tools/10.0/base_user_role_company/static/description/icon.png


.. contents::



Overview | Panoramica
=====================

|en| Enable User Roles depending on the Companies selected.

A company specific Role will only be enabled
if it is set for **all** the currently selected companies.

For example, if a user is "Sales Manager" only for Company A,
it will see that role enabled only if Company A is selected.
If the user selects Company A and Company B,
then the "Sales Manager" role won't be enabled.


|it| Nessuna informazione disponibile

|thumbnail|

.. |thumbnail| image:: https://raw.githubusercontent.com/zeroincombenze/server-tools/10.0/base_user_role_company/static/description/description.png


Configuration | Configurazione
------------------------------

Roles are set on the User form.

The "Company" additional column allows to set a Role as only valid for specific companies.

There is also a "Active Role" techincal field, only visible in developer mode.
It shows what roles are active, after applying the company selection rules.



Usage | Utilizzo
----------------

Select the active companies from the web client widget, near the top right corner.
When doing so, the User's security Groups are recomputed, based on the Roles.

When the user changes the company selection, only the groups available to all active companies will be activated.

For example:

* A "SALES PERSON" and a "SALES MANAGER" roles are created.

* A user is assigned to the roles:
    * "SALES PERSON", with no specific company assigned (meaning all)
    * "SALES MANAGER" only to "My Company (Chicago)"

* When selecting active companies from the UI widget:
    * If only "My Company (San Francisco)" is active, "SALES PERSON" will be active.
    * If only "My Company (Chicago)" is active, "SALES PERSON" and "SALES MANAGER" will be active.
    * If both "My Company (San Francisco)" and "My Company (Chicago)" is active, "SALES PERSON" will be active.



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

* Open Source Integrators <False>
* `Odoo Community Association (OCA) <https://odoo-community.org>`__
* `SHS-AV s.r.l. <https://www.zeroincombenze.it>`__



Contributors | Partecipanti
---------------------------

* `Open Source Integrators <https://opensourceintegrators.com>`__
* `* Daniel Reis <dreis@opensourceintegrators.com>`__
* `* Chandresh Thakkar <cthakkr@opensourceintegrators.com>`__
* Maintainers <False>
* ~~~~~~~~~~~ <False>
* This module is maintained by the OCA. <False>
* .. image:: https://odoo-community.org/logo.png <False>
* :alt: Odoo Community Association <False>
* :target: https://odoo-community.org <False>
* OCA, or the Odoo Community Association, is a nonprofit organization whose <False>
* mission is to support the collaborative development of Odoo features and <False>
* promote its widespread use. <False>
* `This module is part of the OCA/server-tools <https://github.com/OCA/server-tools/tree/10.0/base_user_role_company>`__
* You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute. <False>



Maintainer | Manutenzione
-------------------------

* dreispt <False>



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

Last Update / Ultimo aggiornamento: 2024-02-01

.. |Maturity| image:: https://img.shields.io/badge/maturity-Beta-yellow.png
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
