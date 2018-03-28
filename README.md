[![Build Status](https://travis-ci.org/zeroincombenze/server-tools.svg?branch=7.0)](https://travis-ci.org/zeroincombenze/server-tools)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/server-tools/badge.svg?branch=7.0)](https://coveralls.io/github/zeroincombenze/server-tools?branch=7.0)
[![codecov](https://codecov.io/gh/zeroincombenze/server-tools/branch/7.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/server-tools/branch/7.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-7.svg)](https://github.com/OCA/server-tools/tree/7.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-7.svg)](http://wiki.zeroincombenze.org/en/Odoo/7.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-7.svg)](http://wiki.zeroincombenze.org/en/Odoo/7.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-7.svg)](http://erp7.zeroincombenze.it)


[![en](https://github.com/zeroincombenze/grymb/blob/master/flags/en_US.png)](https://www.facebook.com/groups/openerp.italia/)
================================================================================================
================================================================================================

Server Environment And Tools
============================

This project aim to deal with modules related to manage Odoo server environment and provide useful tools. You'll find modules that:

 - Manage configuration depending on environment (devs, test, prod,..)
 - Keep the security on update
 - Manage email settings
 -...

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


Available addons
----------------
addon | version | OCA version | summary
--- | --- | --- | ---
[admin_technical_features](admin_technical_features/) | 0.1 | :repeat: | Checks the technical features box for admin user.
[auth_admin_passkey](auth_admin_passkey/) | 2.1.1 | :repeat: | Authentification - Admin Passkey
[auth_from_http_basic](auth_from_http_basic/) | 1.0 | :repeat: | Authenticate via HTTP basic authentication
[auth_from_http_basic_logout](auth_from_http_basic_logout/) | 1.0 | :repeat: | Authenticate via HTTP basic authentication (logout helper)
[base_concurrency](base_concurrency/) | 1.0 | :repeat: | Base Concurrency
[base_export_email](base_export_email/) | 0.1 | :repeat: | Base export email addon
[base_external_dbsource](base_external_dbsource/) | 1.3 | :repeat: | External Database Sources
[base_optional_quick_create](base_optional_quick_create/) | 0.1 | :repeat: | Avoid 'quick create' on m2o fields, on a 'by model' basis
[configuration_helper](configuration_helper/) | 0.8 | :repeat: | Configuration Helper
[cron_run_manually](cron_run_manually/) | 0.1 | :repeat: | Call cron jobs from their form view
[database_cleanup](database_cleanup/) | 0.1 | :repeat: | Database cleanup
[dbfilter_from_header](dbfilter_from_header/) | 1.0 | :repeat: | dbfilter_from_header
[defer_parent_store_computation_import](defer_parent_store_computation_import/) |  | :repeat: | Deferred Parent Computation Import
[disable_openerp_online](disable_openerp_online/) | 1.1 | :repeat: | Remove openerp.com bindings
[document_export_from_db](document_export_from_db/) | 1.0 | :repeat: | Export Existing Documents from Database to File System
[email_template_dateutil](email_template_dateutil/) | 0.1 | :repeat: | Adds extra date functions for email templates
[email_template_template](email_template_template/) | 1.0 | :repeat: | Templates for email templates
[fetchmail_attach_from_folder](fetchmail_attach_from_folder/) | 1.0 | 7.0.1.0.1 | Attach mails in an IMAP folder to existing objects
[fetchmail_bydate](fetchmail_bydate/) | 1.0 | :repeat: | Fetchmail by date and unseen messages
[import_odbc](import_odbc/) | 1.3 | :repeat: | Import data from SQL and ODBC data sources.
[mail_environment](mail_environment/) | 0.1 | :repeat: | Server env config for mail + fetchmail
[mass_editing](mass_editing/) | 1.3 | :repeat: | Mass Editing
[module_parent_dependencies](module_parent_dependencies/) | 7.0.0.1.1 | 0.1 | allows to see the list of installed modules dependencies of a given module, at the full depth of the dependency tree
[scheduler_error_mailer](scheduler_error_mailer/) | 1.0 | :repeat: | Send an e-mail when a scheduler fails
[secure_uninstall](secure_uninstall/) | 0.1 | :repeat: | Ask password to authorize uninstall
[server_environment_files](server_environment_files/) | 1.0 | :repeat: | Example server configuration environment files repository module
[server_monitoring](server_monitoring/) | 0.1 | :repeat: | Server Monitoring
[sql_export](sql_export/) | 0.1 | :repeat: | Export data in csv file with SQL requests
[sql_export_email](sql_export_email/) | 0.1 | :repeat: | SQL export email addon
[super_calendar](super_calendar/) | 0.1 | :repeat: | This module allows to create configurable calendars.
[tree_view_record_id](tree_view_record_id/) | 0.1 | :repeat: | Adds id field to tree views
[users_ldap_groups](users_ldap_groups/) | 1.2.1 | :repeat: | Groups assignment
[users_ldap_mail](users_ldap_mail/) | 1.0 | :repeat: | LDAP mapping for user name and e-mail
[users_ldap_populate](users_ldap_populate/) | 1.2 | :repeat: | LDAP Populate
[web_context_tunnel](web_context_tunnel/) | 2.0 | :repeat: | Web Context Tunnel


Unported addons
---------------
addon | version | OCA version | summary
--- | --- | --- | ---
[ir_config_parameter_viewer](__unported__/ir_config_parameter_viewer/) | 0.1 (unported) | :x: | Ir.config_parameter view
[security_protector](__unported__/security_protector/) | 0.1 (unported) | :x: | Security protector
[server_env_base_external_referentials](__unported__/server_env_base_external_referentials/) | 1.0 (unported) | :x: | Server environment for base_external_referential
[auth_generate_password](auth_generate_password/) | 1.0 (unported) | 7.0.1.0.1 | Authentification - Generate Password
[mail_cleanup](mail_cleanup/) | 0.1 (unported) | 0.1 | Clean up mails regularly
[record_archiver](record_archiver/) | 0.1 (unported) | 0.1 | Records Archiver
[sentry_logger](sentry_logger/) | 1.1 (unported) | 1.1 | Sentry integration
[server_environment](server_environment/) | 1.0 (unported) | 1.0 | server configuration environment files

[//]: # (end addons)

[![chat with us](https://www.shs-av.com/wp-content/chat_with_us.gif)](https://tawk.to/85d4f6e06e68dd4e358797643fe5ee67540e408b)
