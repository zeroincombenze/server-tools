===========================================
|icon| Mass Editing/mass_editing 10.0.2.1.0
===========================================

.. |icon| image:: https://raw.githubusercontent.com/zeroincombenze/server-tools/10.0/mass_editing/static/description/icon.png


.. contents::



Overview | Panoramica
=====================

|en| This module provides the following features:

* You can add, update or remove the values of more than one records on the fly at the same time.

* You can configure mass editing for any Odoo model.

* The video explaining the features and how-to for OpenERP Version 6 is here http://t.co/wukYMx1A

* The video explaining the features and how-to for OpenERP Version 7 is here : http://www.youtube.com/watch?v=9BH0o74A748&feature=youtu.be

* For more details/customization/feedback contact us on contact@serpentcs.com


|it| Descrizione in italiano non (ancora) disponibile


|thumbnail|

.. |thumbnail| image:: https://raw.githubusercontent.com/zeroincombenze/server-tools/10.0/mass_editing/static/description/description.png


Configuration | Configurazione
------------------------------

To configure this module, you need to:

* Go to *Settings / Mass Editing / Mass Editing* and configure the object and fields for Mass Editing.



Usage | Utilizzo
----------------

This module allows to add, update or remove the values of more than one records on the fly at the same time.

.. image:: https://odoo-community.org/website/image/ir.attachment/5784_f2813bd/datas
   :alt: Try me on Runbot
   :target: https://runbot.odoo-community.org/runbot/149/9.0

As shown in figure you have to configure the object and fields for mass editing.

* Select the object and add the fields of that object on which you want to apply mass editing.

.. image:: /mass_editing/static/description/mass_editing-1.png
   :width: 70%

* *Add Action*: As shown in figure click on *Add Sidebar Button* to add mass editing option in *Action* option in action.

.. image:: /mass_editing/static/description/mass_editing-2.png
   :width: 70%

* *Go for Mass Editing*: As shown in figure, select the records which you want to modify and click on *Action* to open mass editing popup.

.. image:: /mass_editing/static/description/mass_editing-3.png
   :width: 70%

* Select *Set / Remove* action and write down the value to set or remove the value for the given field.

.. image:: /mass_editing/static/description/mass_editing-4.png
   :width: 70%

* This way you can set / remove the values of the fields.

.. image:: /mass_editing/static/description/mass_editing-5.png
   :width: 70%



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

* `Serpent Consulting Services Pvt. Ltd. <https://www.serpentcs.com>`__
* Tecnativa <False>
* brain-tec AG <False>
* `Odoo Community Association (OCA) <https://odoo-community.org>`__
* `Tecnativa S. L. <https://www.tecnativa.com>`__
* `SHS-AV s.r.l. <https://www.zeroincombenze.it>`__



Contributors | Partecipanti
---------------------------

* `Oihane Crucelaegui <oihanecrucelaegi@gmail.com>`__
* `Serpent Consulting Services Pvt. Ltd. <support@serpentcs.com>`__
* `Raul Martin <raul.martin@braintec-group.com>`__
* `Simone Vanin <simone.vanin@agilebg.com>`__
* `Tecnativa S. L. <https://www.tecnativa.com>`__
* * Jairo Llopis <False>
* * Víctor Martínez <False>
* Maintainers <False>
* ~~~~~~~~~~~ <False>
* This module is maintained by the OCA. <False>
* .. image:: https://odoo-community.org/logo.png <False>
* :alt: Odoo Community Association <False>
* :target: https://odoo-community.org <False>
* OCA, or the Odoo Community Association, is a nonprofit organization whose <False>
* mission is to support the collaborative development of Odoo features and <False>
* promote its widespread use. <False>
* `This module is part of the OCA/server-tools <https://github.com/OCA/server-tools/tree/10.0/mass_editing>`__
* You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute. <False>



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

Last Update / Ultimo aggiornamento: 2024-02-01

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
