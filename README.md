[![Build Status](https://travis-ci.org/zeroincombenze/server-tools.svg?branch=8.0)](https://travis-ci.org/zeroincombenze/server-tools)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/server-tools/badge.svg?branch=8.0)](https://coveralls.io/github/zeroincombenze/server-tools?branch=8.0)
[![codecov](https://codecov.io/gh/zeroincombenze/server-tools/branch/8.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/server-tools/branch/8.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-8.svg)](https://github.com/OCA/server-tools/tree/8.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-8.svg)](http://erp8.zeroincombenze.it)


































[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

Server Environment And Tools
============================

This project aim to deal with modules related to manage Odoo server environment and provide useful tools. You'll find modules that:

 - Manage configuration depending on environment (devs, test, prod,..)
 - Keep the security on update
 - Manage email settings

[//]: # (addons)


Available addons
----------------
addon | version | OCA version | summary
--- | --- | --- | ---
[admin_technical_features](admin_technical_features/) | 8.0.0.1.0 | :repeat: | Checks the technical features box for admin user.
[attachment_metadata](attachment_metadata/) | 8.0.1.0.0 | :repeat: | Attachment Metadata
[auditlog](auditlog/) | 8.0.1.3.0 | :repeat: | Audit Log
[auth_admin_passkey](auth_admin_passkey/) | 8.0.2.1.1 | :repeat: | Authentification - Admin Passkey
[auth_brute_force](auth_brute_force/) | 8.0.1.0.0 | :repeat: | Tracks Authentication Attempts and Prevents Brute-force Attacks module
[auth_dynamic_groups](auth_dynamic_groups/) | 8.0.1.0.0 | :repeat: | Have membership conditions for certain groups
[auth_from_http_remote_user](auth_from_http_remote_user/) | 8.0.1.0.0 | :repeat: | Authenticate via HTTP Remote User
[auth_signup_verify_email](auth_signup_verify_email/) | 8.0.1.0.0 | :repeat: | Force uninvited users to use a good email for signup
[auth_supplier](auth_supplier/) | 8.0.1.0.0 | :repeat: | Auth Supplier
[auto_backup](auto_backup/) | 8.0.1.0.1 | 8.0.1.0.3 | Backups database
[base_concurrency](base_concurrency/) | 8.0.1.1.0 | :repeat: | Base Concurrency
[base_custom_info](base_custom_info/) | 8.0.1.0.0 | :repeat: | Add custom field in models
[base_debug4all](base_debug4all/) | 8.0.1.0.0 | :repeat: | Shows full debug options for all users
[base_export_manager](base_export_manager/) | 8.0.2.1.0 | :repeat: | Manage model export profiles
[base_external_dbsource](base_external_dbsource/) | 8.0.1.3.0 | :repeat: | External Database Sources
[base_field_validator](base_field_validator/) | 8.0.1.0.0 | :repeat: | Validate fields using regular expressions
[base_import_match](base_import_match/) | 8.0.1.0.1 | :repeat: | Try to avoid duplicates before importing
[base_ir_filters_active](base_ir_filters_active/) | 8.0.1.0.0 | :repeat: | Allows you to disable (hide) filters
[base_module_doc_rst](base_module_doc_rst/) | 8.0.1.0.0 | :repeat: | Modules Technical Guides in RST and Relationship Graphs
[base_multi_image](base_multi_image/) | 8.0.2.0.0 | :repeat: | Allow multiple images for database objects
[base_name_search_improved](base_name_search_improved/) | 8.0.1.0.1 | 8.0.1.0.2 | Friendlier search when typing in relation fields
[base_optional_quick_create](base_optional_quick_create/) | 8.0.0.1.0 | :repeat: | Avoid 'quick create' on m2o fields, on a 'by model' basis
[base_report_auto_create_qweb](base_report_auto_create_qweb/) | 8.0.1.0.0 | :repeat: | Report qweb auto generation
[base_search_fuzzy](base_search_fuzzy/) | 8.0.1.0.0 | :repeat: | Fuzzy search with the PostgreSQL trigram extension
[base_suspend_security](base_suspend_security/) | 8.0.1.0.0 | 8.0.1.0.1 | Suspend security checks for a call
[base_user_gravatar](base_user_gravatar/) | 8.0.1.0.0 | :repeat: | Synchronize Gravatar image
[base_user_reset_access](base_user_reset_access/) | 8.0.1.0.0 | :repeat: | Reset User Access Right
[cron_run_manually](cron_run_manually/) | 8.0.1.0.0 | :repeat: | Call cron jobs from their form view
[database_cleanup](database_cleanup/) | 8.0.0.1.0 | :repeat: | Database cleanup
[datetime_formatter](datetime_formatter/) | 8.0.1.0.0 | :repeat: | Helper functions to give correct format to date[time] fields
[dbfilter_from_header](dbfilter_from_header/) | 8.0.1.0.1 | :repeat: | dbfilter_from_header
[dead_mans_switch_client](dead_mans_switch_client/) | 8.0.1.0.1 | :repeat: | Be notified when customers' odoo instances go down
[dead_mans_switch_server](dead_mans_switch_server/) | 8.0.1.0.0 | :repeat: | Be notified when customers' odoo instances go down
[disable_openerp_online](disable_openerp_online/) | 8.0.1.1.0 | :repeat: | Remove odoo.com bindings
[fetchmail_attach_from_folder](fetchmail_attach_from_folder/) | 8.0.1.0.1 | :repeat: | Attach mails in an IMAP folder to existing objects
[fetchmail_notify_error_to_sender](fetchmail_notify_error_to_sender/) | 8.0.1.0.1 | :repeat: | If fetching mails gives error, send an email to sender
[field_char_transformed](field_char_transformed/) | 8.0.1.0.0 | :repeat: | Allows to transform input in character fields before writing or reading it to/from the database
[field_rrule](field_rrule/) | 8.0.1.0.0 | 8.0.1.0.1 | Provides a field and widget for RRules according to RFC 2445
[html_image_url_extractor](html_image_url_extractor/) | 8.0.1.0.0 | :repeat: | Extract images found in any HTML field
[html_text](html_text/) | 8.0.1.0.0 | :repeat: | Generate excerpts from any HTML field
[inactive_session_timeout](inactive_session_timeout/) | 8.0.1.0.0 | :repeat: | This module disable all inactive sessions since a given delay
[language_path_mixin](language_path_mixin/) | 8.0.1.0.0 | :repeat: | Setting the partner's language in RML reports
[letsencrypt](letsencrypt/) | 8.0.1.0.0 | :repeat: | Request SSL certificates from letsencrypt.org
[log_forwarded_for_ip](log_forwarded_for_ip/) | 8.0.1.0.0 | :repeat: | Displays source IPs in log when behind a reverse proxy
[mail_environment](mail_environment/) | 8.0.0.1.0 | :repeat: | Server env config for mail + fetchmail
[mass_editing](mass_editing/) | 8.0.1.3.0 | :repeat: | Mass Editing
[module_prototyper](module_prototyper/) | 8.0.0.3.0 | :repeat: | Prototype your module.
[qweb_usertime](qweb_usertime/) | 8.0.1.0.0 | :repeat: | Add user time rendering support in QWeb
[save_translation_file](save_translation_file/) | 8.0.1.0.0 | :repeat: | Allows developpers to easily generate i18n files
[scheduler_error_mailer](scheduler_error_mailer/) | 8.0.1.0.0 | :repeat: | Send an e-mail when a scheduler fails
[secure_uninstall](secure_uninstall/) | 8.0.1.0.0 | :repeat: | Ask password to authorize uninstall
[server_environment](server_environment/) | 8.0.1.1.0 | :repeat: | server configuration environment files
[server_environment_files_sample](server_environment_files_sample/) | 8.0.1.0.0 | :repeat: | Example server configuration environment files repository module
[shell](shell/) | 8.0.1.0.0 | :repeat: | Backport of the v9 shell CLI command.
[super_calendar](super_calendar/) | 8.0.0.2.0 | :repeat: | This module allows to create configurable calendars.
[users_ldap_groups](users_ldap_groups/) | 8.0.1.2.1 | 8.0.1.2.2 | Adds user accounts to groups based on rules defined by the administrator.
[users_ldap_mail](users_ldap_mail/) | 8.0.1.0.0 | :repeat: | LDAP mapping for user name and e-mail
[users_ldap_populate](users_ldap_populate/) | 8.0.1.2.0 | 8.0.1.2.1 | LDAP Populate
[users_ldap_push](users_ldap_push/) | 8.0.1.0.0 | :repeat: | Creates a ldap entry when you create a user in Odoo
[web_context_tunnel](web_context_tunnel/) | 8.0.2.0.0 | :repeat: | Web Context Tunnel


Unported addons
---------------
addon | version | OCA version | summary
--- | --- | --- | ---
[auth_from_http_basic](auth_from_http_basic/) | 1.0 (unported) | :repeat: | Authenticate via HTTP basic authentication
[auth_from_http_basic_logout](auth_from_http_basic_logout/) | 1.0 (unported) | :repeat: | Authenticate via HTTP basic authentication (logout helper)
[configuration_helper](configuration_helper/) | 0.8 (unported) | :repeat: | Configuration Helper
[email_template_template](email_template_template/) | 1.0 (unported) | :repeat: | Templates for email templates
[import_odbc](import_odbc/) | 1.3 (unported) | 8.0.0.1.3 | Import data from SQL and ODBC data sources.
[ir_config_parameter_viewer](ir_config_parameter_viewer/) | 0.1 (unported) | :repeat: | Ir.config_parameter view
[security_protector](security_protector/) | 0.1 (unported) | :repeat: | Security protector
[server_env_base_external_referentials](server_env_base_external_referentials/) | 1.0 (unported) | :repeat: | Server environment for base_external_referential

[//]: # (end addons)

Translation Status
[![Transifex Status](https://www.transifex.com/projects/p/OCA-server-tools-8-0/chart/image_png)](https://www.transifex.com/projects/p/OCA-server-tools-8-0)

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

[![chat with us](https://www.shs-av.com/wp-content/chat_with_us.gif)](https://tawk.to/85d4f6e06e68dd4e358797643fe5ee67540e408b)
