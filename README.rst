
==================================
|Zeroincombenze| server-tools 10.0
==================================

|Maturity| |Build Status| |Coverage Status| |Codecov Status| |license gpl| |Tech Doc| |Help| |Try Me|

.. contents::


Overview / Panoramica
=====================

|en| Server Environment And Tools

This project aim to deal with modules related to manage Odoo server environment and provide useful tools. You'll find modules that:

* Manage configuration depending on environment (devs, test, prod,..)
* Keep the security on update
* Manage email settings


|it| Strumenti per gestione server

Progetto basato sui moduli OCA Strumenti per gestione server

Avaiable Addons / Moduli disponibili
------------------------------------

+--------------------------------------+------------+------------+----------------------------------------------------+
| Name / Nome                          | Version    | OCA Ver.   | Description / Descrizione                          |
+--------------------------------------+------------+------------+----------------------------------------------------+
| admin_technical_features             | |halt|     | |halt|     | Checks the technical features box for admin user.  |
+--------------------------------------+------------+------------+----------------------------------------------------+
| attachment_base_synchronize          | 10.0.1.0.0 | |same|     | Attachment Base Synchronize                        |
+--------------------------------------+------------+------------+----------------------------------------------------+
| auditlog                             | 10.0.1.0.0 | |same|     | Audit Log                                          |
+--------------------------------------+------------+------------+----------------------------------------------------+
| auth_admin_passkey                   | |halt|     | |same|     | Authentification - Admin Passkey                   |
+--------------------------------------+------------+------------+----------------------------------------------------+
| auth_brute_force                     | 10.0.2.2.0 | |same|     | Track Authentication Attempts and Prevent Brute-fo |
+--------------------------------------+------------+------------+----------------------------------------------------+
| auth_dynamic_groups                  | |halt|     | |halt|     | Have membership conditions for certain groups      |
+--------------------------------------+------------+------------+----------------------------------------------------+
| auth_from_http_basic                 | |halt|     | |halt|     | Authenticate via HTTP basic authentication         |
+--------------------------------------+------------+------------+----------------------------------------------------+
| auth_from_http_basic_logout          | |halt|     | |halt|     | Authenticate via HTTP basic authentication (logout |
+--------------------------------------+------------+------------+----------------------------------------------------+
| auth_from_http_remote_user           | |halt|     | |halt|     | Authenticate via HTTP Remote User                  |
+--------------------------------------+------------+------------+----------------------------------------------------+
| auth_oauth_multi_token               | 10.0.1.0.0 | |same|     | Allow multiple connection with the same OAuth acco |
+--------------------------------------+------------+------------+----------------------------------------------------+
| auth_session_timeout                 | 10.0.1.0.2 | |same|     | This module disable all inactive sessions since a  |
+--------------------------------------+------------+------------+----------------------------------------------------+
| auth_signup_verify_email             | 10.0.2.0.0 | |same|     | Force uninvited users to use a good email for sign |
+--------------------------------------+------------+------------+----------------------------------------------------+
| auth_supplier                        | 10.0.1.0.0 | |same|     | Auth Supplier                                      |
+--------------------------------------+------------+------------+----------------------------------------------------+
| auth_totp                            | 10.0.2.0.0 | |same|     | Allows users to enable MFA and add optional truste |
+--------------------------------------+------------+------------+----------------------------------------------------+
| auth_totp_password_security          | 10.0.1.0.0 | |same|     | auth_totp and password_security compatibility      |
+--------------------------------------+------------+------------+----------------------------------------------------+
| auth_user_case_insensitive           | |halt|     | |same|     | Makes the user login field case insensitive        |
+--------------------------------------+------------+------------+----------------------------------------------------+
| auto_backup                          | 10.0.1.0.2 | |same|     | Backups database                                   |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_cron_exclusion                  | 10.0.1.0.0 | |same|     | Allow you to select scheduled actions that should  |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_custom_info                     | 10.0.1.0.0 | |same|     | Add custom field in models                         |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_debug4all                       | |halt|     | |no_check| | Shows full debug options for all users             |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_exception                       | 10.0.2.0.1 | |same|     | This module provide an abstract model to manage cu |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_export_manager                  | 10.0.1.0.0 | |same|     | Manage model export profiles                       |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_export_security                 | 10.0.1.0.0 | |same|     | Security features for Odoo exports                 |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_external_dbsource               | 10.0.2.0.0 | |same|     | External Database Sources                          |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_external_dbsource_firebird      | 10.0.1.0.0 | |same|     | External Database Source - Firebird                |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_external_dbsource_mssql         | 10.0.1.0.0 | |same|     | External Database Source - MSSQL                   |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_external_dbsource_mysql         | 10.0.1.0.0 | |same|     | External Database Source - MySQL                   |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_external_dbsource_odbc          | 10.0.1.0.0 | |same|     | External Database Source - ODBC                    |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_external_dbsource_oracle        | 10.0.1.0.0 | |same|     | External Database Source - Oracle                  |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_external_dbsource_sqlite        | 10.0.1.0.0 | |same|     | External Database Source - SQLite                  |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_external_system                 | 10.0.1.0.0 | |same|     | Data models allowing for connection to external sy |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_fontawesome                     | 10.0.4.7.0 | |same|     | Up to date Fontawesome resources.                  |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_import_default_enable_tracking  | 10.0.1.0.0 | |same|     | This modules simply enables history tracking when  |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_import_match                    | 10.0.1.0.0 | |same|     | Try to avoid duplicates before importing           |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_import_security_group           | 10.0.1.0.0 | |same|     | Group-based permissions for importing CSV files    |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_jsonify                         | 10.0.12.0. | 10.0.1.0.0 | Base module that provide the jsonify method on all |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_kanban_stage                    | 10.0.1.2.1 | |same|     | Provides stage model and abstract logic for inheri |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_kanban_stage_state              | 10.0.1.0.0 | |same|     | Maps stages from base_kanban_stage to states       |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_locale_uom_default              | 10.0.1.0.0 | |same|     | This provides settings to select default UoMs at t |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_manifest_extension              | 10.0.1.0.0 | |same|     | Adds useful keys to manifest files                 |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_multi_image                     | |halt|     | |same|     | Allow multiple images for database objects         |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_optional_quick_create           | 10.0.1.0.1 | |same|     | Avoid 'quick create' on m2o fields, on a 'by model |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_report_auto_create_qweb         | 10.0.1.0.0 | |same|     | Report qweb auto generation                        |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_search_fuzzy                    | 10.0.12.0. | 10.0.1.1.0 | Fuzzy search with the PostgreSQL trigram extension |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_suspend_security                | 10.0.1.0.0 | |same|     | Suspend security checks for a call                 |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_technical_features              | 10.0.1.0.1 | |same|     | Access to technical features without activating de |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_technical_user                  | 10.0.1.0.0 | |same|     | Add a technical user parameter on the company      |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_tier_validation                 | 10.0.1.0.1 | |same|     | Implement a validation process based on tiers.     |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_user_gravatar                   | 10.0.1.0.1 | |same|     | Synchronize Gravatar Image                         |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_user_role                       | 10.0.1.0.3 | |same|     | User roles                                         |
+--------------------------------------+------------+------------+----------------------------------------------------+
| base_view_inheritance_extension      | 10.0.1.0.1 | |same|     | Adds more operators for view inheritance           |
+--------------------------------------+------------+------------+----------------------------------------------------+
| configuration_helper                 | 10.0.1.0.0 | |same|     | Configuration Helper                               |
+--------------------------------------+------------+------------+----------------------------------------------------+
| database_cleanup                     | |halt|     | |same|     | Database cleanup                                   |
+--------------------------------------+------------+------------+----------------------------------------------------+
| date_range                           | |halt|     | |same|     | Manage all kind of date range                      |
+--------------------------------------+------------+------------+----------------------------------------------------+
| datetime_formatter                   | 10.0.1.0.0 | |same|     | Helper functions to give correct format to date[ti |
+--------------------------------------+------------+------------+----------------------------------------------------+
| dbfilter_from_header                 | 10.0.1.0.0 | |same|     | Filter databases with HTTP headers                 |
+--------------------------------------+------------+------------+----------------------------------------------------+
| dead_mans_switch_client              | 10.0.1.0.0 | |same|     | Be notified when customers' Odoo instances go down |
+--------------------------------------+------------+------------+----------------------------------------------------+
| disable_odoo_online                  | 10.0.1.0.0 | |same|     | Remove odoo.com Bindings                           |
+--------------------------------------+------------+------------+----------------------------------------------------+
| email_template_template              | |halt|     | |halt|     | Templates for email templates                      |
+--------------------------------------+------------+------------+----------------------------------------------------+
| excel_import_export                  | 10.0.12.0. | |no_check| | Base module for easy way to develop Excel import/e |
+--------------------------------------+------------+------------+----------------------------------------------------+
| excel_import_export_demo             | 10.0.12.0. | |no_check| | Excel Import/Export Demo                           |
+--------------------------------------+------------+------------+----------------------------------------------------+
| fetchmail_attach_from_folder         | |halt|     | |halt|     | Attach mails in an IMAP folder to existing objects |
+--------------------------------------+------------+------------+----------------------------------------------------+
| fetchmail_notify_error_to_sender     | |halt|     | |same|     | If fetching mails gives error, send an email to se |
+--------------------------------------+------------+------------+----------------------------------------------------+
| html_image_url_extractor             | 10.0.1.0.0 | |same|     | Extract images found in any HTML field             |
+--------------------------------------+------------+------------+----------------------------------------------------+
| html_text                            | 10.0.12.0. | 10.0.1.0.0 | Generate excerpts from any HTML field              |
+--------------------------------------+------------+------------+----------------------------------------------------+
| import_odbc                          | |halt|     | |halt|     | Import data from SQL and ODBC data sources.        |
+--------------------------------------+------------+------------+----------------------------------------------------+
| ir_config_parameter_viewer           | |halt|     | |halt|     | Ir.config_parameter view                           |
+--------------------------------------+------------+------------+----------------------------------------------------+
| keychain                             | 10.0.2.0.1 | |same|     | Store accounts and credentials                     |
+--------------------------------------+------------+------------+----------------------------------------------------+
| language_path_mixin                  | |halt|     | |halt|     | Setting the partner's language in RML reports      |
+--------------------------------------+------------+------------+----------------------------------------------------+
| letsencrypt                          | 10.0.1.0.0 | |same|     | Request SSL certificates from letsencrypt.org      |
+--------------------------------------+------------+------------+----------------------------------------------------+
| mail_environment                     | 10.0.1.0.0 | |same|     | Configure mail servers with server_environment_fil |
+--------------------------------------+------------+------------+----------------------------------------------------+
| mail_log_message_to_process          | 10.0.1.0.0 | |same|     | Log all messages received, before they start to be |
+--------------------------------------+------------+------------+----------------------------------------------------+
| mass_editing                         | 10.0.1.1.0 | |same|     | Mass Editing                                       |
+--------------------------------------+------------+------------+----------------------------------------------------+
| mass_sorting                         | 10.0.1.0.0 | |same|     | Sort any models by any fields list                 |
+--------------------------------------+------------+------------+----------------------------------------------------+
| menu_technical_info                  | |halt|     | |halt|     | Fast way to look up technical info about menu item |
+--------------------------------------+------------+------------+----------------------------------------------------+
| mgmtsystem_kpi                       | |halt|     | |no_check| | Key Performance Indicator                          |
+--------------------------------------+------------+------------+----------------------------------------------------+
| module_auto_update                   | |halt|     | |same|     | Automatically update Odoo modules                  |
+--------------------------------------+------------+------------+----------------------------------------------------+
| module_prototyper                    | 10.0.1.0.0 | |same|     | Prototype your module.                             |
+--------------------------------------+------------+------------+----------------------------------------------------+
| onchange_helper                      | 10.0.1.0.0 | |same|     | Technical module that ease execution of onchange i |
+--------------------------------------+------------+------------+----------------------------------------------------+
| password_security                    | 10.0.1.1.4 | |same|     | Allow admin to set password security requirements. |
+--------------------------------------+------------+------------+----------------------------------------------------+
| res_config_settings_enterprise_remov | 10.0.1.0.0 | |same|     | Remove fields in all settings views marked as ente |
+--------------------------------------+------------+------------+----------------------------------------------------+
| scheduler_error_mailer               | 10.0.1.0.0 | |same|     | Scheduler Error Mailer                             |
+--------------------------------------+------------+------------+----------------------------------------------------+
| security_protector                   | |halt|     | |halt|     | Security protector                                 |
+--------------------------------------+------------+------------+----------------------------------------------------+
| sentry                               | 10.0.12.0. | 10.0.1.0.1 | Report Odoo errors to Sentry                       |
+--------------------------------------+------------+------------+----------------------------------------------------+
| sequence_check_digit                 | 10.0.1.0.0 | |same|     | Adds a check digit on sequences                    |
+--------------------------------------+------------+------------+----------------------------------------------------+
| sequence_date_range                  | |halt|     | |same|     | Module used to use the year of the date_to
    int |
+--------------------------------------+------------+------------+----------------------------------------------------+
| server_env_base_external_referential | |halt|     | |halt|     | Server environment for base_external_referential   |
+--------------------------------------+------------+------------+----------------------------------------------------+
| server_environment                   | |halt|     | |same|     | move some configurations out of the database       |
+--------------------------------------+------------+------------+----------------------------------------------------+
| server_environment_files_sample      | 10.0.1.0.0 | |same|     | sample config file for server_environment          |
+--------------------------------------+------------+------------+----------------------------------------------------+
| server_environment_ir_config_paramet | 10.0.1.0.1 | |same|     | Override System Parameters from server environment |
+--------------------------------------+------------+------------+----------------------------------------------------+
| sql_export                           | 10.0.1.0.0 | |same|     | Export data in csv file with SQL requests          |
+--------------------------------------+------------+------------+----------------------------------------------------+
| sql_request_abstract                 | 10.0.12.0. | 10.0.1.0.1 | Abstract Model to manage SQL Requests              |
+--------------------------------------+------------+------------+----------------------------------------------------+
| subscription_action                  | 10.0.1.0.0 | |same|     | Run a server action on a newly created document    |
+--------------------------------------+------------+------------+----------------------------------------------------+
| super_calendar                       | |halt|     | |halt|     | This module allows to create configurable calendar |
+--------------------------------------+------------+------------+----------------------------------------------------+
| user_immutable                       | 10.0.1.0.0 | |same|     | Add Immutable User Support                         |
+--------------------------------------+------------+------------+----------------------------------------------------+
| user_threshold                       | 10.0.1.0.1 | |same|     | Add Configurable User Threshold Support            |
+--------------------------------------+------------+------------+----------------------------------------------------+
| users_ldap_groups                    | |halt|     | |same|     | Adds user accounts to groups based on rules define |
+--------------------------------------+------------+------------+----------------------------------------------------+
| users_ldap_mail                      | 10.0.1.0.0 | |same|     | LDAP mapping for user name and e-mail              |
+--------------------------------------+------------+------------+----------------------------------------------------+
| users_ldap_populate                  | 10.0.1.0.3 | |same|     | LDAP Populate                                      |
+--------------------------------------+------------+------------+----------------------------------------------------+
| webhook                              | 10.0.1.0.0 | |same|     | Webhook                                            |
+--------------------------------------+------------+------------+----------------------------------------------------+


OCA comparation / Confronto con OCA
-----------------------------------

+-----------------------------------------------------------------+-------------------+-----------------------+--------------------------------+
| Description / Descrizione                                       | Odoo Italia       | OCA                   | Notes / Note                   |
+-----------------------------------------------------------------+-------------------+-----------------------+--------------------------------+
| Coverage / Copertura test                                       |  |Codecov Status| | |OCA Codecov Status|  | |OCA project|                  |
+-----------------------------------------------------------------+-------------------+-----------------------+--------------------------------+


Getting started / Come iniziare
===============================

|Try Me|


Prerequisites / Prerequisiti
----------------------------


* python2.7+
* postgresql 9.2+

Installation / Installazione
----------------------------

+---------------------------------+------------------------------------------+
| |en|                            | |it|                                     |
+---------------------------------+------------------------------------------+
| These instruction are just an   | Istruzioni di esempio valide solo per    |
| example to remember what        | distribuzioni Linux CentOS 7, Ubuntu 14+ |
| you have to do on Linux.        | e Debian 8+                              |
|                                 |                                          |
| Installation is built with:     | L'installazione è costruita con:         |
+---------------------------------+------------------------------------------+
| `Zeroincombenze Tools <https://github.com/zeroincombenze/tools>`__         |
+---------------------------------+------------------------------------------+
| Suggested deployment is:        | Posizione suggerita per l'installazione: |
+---------------------------------+------------------------------------------+
| /opt/odoo/10.0/server-tools/                                               |
+----------------------------------------------------------------------------+

::

    cd $HOME
    git clone https://github.com/zeroincombenze/tools.git
    cd ./tools
    ./install_tools.sh -p
    export PATH=$HOME/dev:$PATH
    odoo_install_repository server-tools -b 10.0 -O zero
    for pkg in os0 z0lib; do
        pip install $pkg -U
    done
    sudo manage_odoo requirements -b 10.0 -vsy -o /opt/odoo/10.0


Upgrade / Aggiornamento
-----------------------

+---------------------------------+------------------------------------------+
| |en|                            | |it|                                     |
+---------------------------------+------------------------------------------+
| When you want upgrade and you   | Per aggiornare, se avete installato con  |
| installed using above           | le istruzioni di cui sopra:              |
| statements:                     |                                          |
+---------------------------------+------------------------------------------+

::

    odoo_install_repository server-tools -b 10.0 -O zero -U
    # Adjust following statements as per your system
    sudo systemctl restart odoo


Support / Supporto
------------------


|Zeroincombenze| This project is mainly maintained by the `SHS-AV s.r.l. <https://www.zeroincombenze.it/>`__



Get involved / Ci mettiamo in gioco
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

Credits / Titoli di coda
========================

Copyright
---------

Odoo is a trademark of `Odoo S.A. <https://www.odoo.com/>`__ (formerly OpenERP)


----------------


|en| **zeroincombenze®** is a trademark of `SHS-AV s.r.l. <https://www.shs-av.com/>`__
which distributes and promotes ready-to-use **Odoo** on own cloud infrastructure.
`Zeroincombenze® distribution of Odoo <https://wiki.zeroincombenze.org/en/Odoo>`__
is mainly designed to cover Italian law and markeplace.

|it| **zeroincombenze®** è un marchio registrato di `SHS-AV s.r.l. <https://www.shs-av.com/>`__
che distribuisce e promuove **Odoo** pronto all'uso sullla propria infrastuttura.
La distribuzione `Zeroincombenze® è progettata per le esigenze del mercato italiano.


|chat_with_us|


|

Last Update / Ultimo aggiornamento: 2019-04-13

.. |Maturity| image:: https://img.shields.io/badge/maturity-Alfa-red.png
    :target: https://odoo-community.org/page/development-status
    :alt: Alfa
.. |Build Status| image:: https://travis-ci.org/zeroincombenze/server-tools.svg?branch=10.0
    :target: https://travis-ci.org/zeroincombenze/server-tools
    :alt: github.com
.. |license gpl| image:: https://img.shields.io/badge/licence-LGPL--3-7379c3.svg
    :target: http://www.gnu.org/licenses/lgpl-3.0-standalone.html
    :alt: License: LGPL-3
.. |license opl| image:: https://img.shields.io/badge/licence-OPL-7379c3.svg
    :target: https://www.odoo.com/documentation/user/9.0/legal/licenses/licenses.html
    :alt: License: OPL
.. |Coverage Status| image:: https://coveralls.io/repos/github/zeroincombenze/server-tools/badge.svg?branch=10.0
    :target: https://coveralls.io/github/zeroincombenze/server-tools?branch=10.0
    :alt: Coverage
.. |Codecov Status| image:: https://codecov.io/gh/zeroincombenze/server-tools/branch/10.0/graph/badge.svg
    :target: https://codecov.io/gh/OCA/server-tools/branch/10.0
    :alt: Codecov
.. |OCA project| image:: Unknown badge-OCA
    :target: https://github.com/OCA/server-tools/tree/10.0
    :alt: OCA
.. |Tech Doc| image:: https://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-10.svg
    :target: https://wiki.zeroincombenze.org/en/Odoo/10.0/dev
    :alt: Technical Documentation
.. |Help| image:: https://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-10.svg
    :target: https://wiki.zeroincombenze.org/it/Odoo/10.0/man
    :alt: Technical Documentation
.. |Try Me| image:: https://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-10.svg
    :target: https://erp10.zeroincombenze.it
    :alt: Try Me
.. |OCA Codecov Status| image:: https://codecov.io/gh/OCA/server-tools/branch/10.0/graph/badge.svg
    :target: https://codecov.io/gh/OCA/server-tools/branch/10.0
    :alt: Codecov
.. |Odoo Italia Associazione| image:: https://www.odoo-italia.org/images/Immagini/Odoo%20Italia%20-%20126x56.png
   :target: https://odoo-italia.org
   :alt: Odoo Italia Associazione
.. |Zeroincombenze| image:: https://avatars0.githubusercontent.com/u/6972555?s=460&v=4
   :target: https://www.zeroincombenze.it/
   :alt: Zeroincombenze
.. |en| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/flags/en_US.png
   :target: https://www.facebook.com/groups/openerp.italia/
.. |it| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/flags/it_IT.png
   :target: https://www.facebook.com/groups/openerp.italia/
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
.. |chat_with_us| image:: https://www.shs-av.com/wp-content/chat_with_us.gif
   :target: https://tawk.to/85d4f6e06e68dd4e358797643fe5ee67540e408b
