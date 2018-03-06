[![Build Status](https://travis-ci.org/zeroincombenze/server-tools.svg?branch=9.0)](https://travis-ci.org/zeroincombenze/server-tools)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/server-tools/badge.svg?branch=9.0)](https://coveralls.io/github/zeroincombenze/server-tools?branch=9.0)
[![codecov](https://codecov.io/gh/zeroincombenze/server-tools/branch/9.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/server-tools/branch/9.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-9.svg)](https://github.com/OCA/server-tools/tree/9.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-9.svg)](http://wiki.zeroincombenze.org/en/Odoo/9.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-9.svg)](http://wiki.zeroincombenze.org/en/Odoo/9.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-9.svg)](http://erp9.zeroincombenze.it)




































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
[admin_technical_features](admin_technical_features/) | 9.0.0.1.0 | :repeat: | Checks the technical features box for admin user.
[attachment_base_synchronize](attachment_base_synchronize/) | 9.0.1.0.0 | :repeat: | Attachment Base Synchronize
[auditlog](auditlog/) | 9.0.1.0.0 | :repeat: | Audit Log
[auth_from_http_remote_user](auth_from_http_remote_user/) | 9.0.1.0.0 | :repeat: | Authenticate via HTTP Remote User
[auth_session_timeout](auth_session_timeout/) | 9.0.1.0.0 | :repeat: | This module disable all inactive sessions since a given delay
[auth_signup_verify_email](auth_signup_verify_email/) | 9.0.1.0.0 | :repeat: | Force uninvited users to use a good email for signup
[auth_supplier](auth_supplier/) | 9.0.2.0.0 | :repeat: | Auth Supplier
[auto_backup](auto_backup/) | 9.0.1.0.0 | 9.0.1.1.1 | Backups database
[base_custom_info](base_custom_info/) | 9.0.1.0.0 | 9.0.2.0.0 | Add custom field in models
[base_export_manager](base_export_manager/) | 9.0.1.1.0 | :repeat: | Manage model export profiles
[base_multi_image](base_multi_image/) | 9.0.1.1.0 | :repeat: | Allow multiple images for database objects
[base_optional_quick_create](base_optional_quick_create/) | 9.0.1.0.0 | :repeat: | Avoid 'quick create' on m2o fields, on a 'by model' basis
[base_report_auto_create_qweb](base_report_auto_create_qweb/) | 9.0.1.0.0 | :repeat: | Report qweb auto generation
[base_suspend_security](base_suspend_security/) | 9.0.1.0.0 | :repeat: | Suspend security checks for a call
[base_technical_features](base_technical_features/) | 9.0.1.0.0 | :repeat: | Access to technical features without activating debug mode
[base_user_gravatar](base_user_gravatar/) | 9.0.1.0.0 | :repeat: | Synchronize Gravatar Image
[configuration_helper](configuration_helper/) | 9.0.1.0.0 | :repeat: | Configuration Helper
[database_cleanup](database_cleanup/) | 9.0.1.0.0 | :repeat: | Database cleanup
[date_range](date_range/) | 9.0.1.0.0 | 9.0.1.0.1 | Manage all kind of date range
[datetime_formatter](datetime_formatter/) | 9.0.1.0.0 | :repeat: | Helper functions to give correct format to date[time] fields
[dbfilter_from_header](dbfilter_from_header/) | 9.0.1.0.0 | :repeat: | Filter databases with HTTP headers
[dead_mans_switch_client](dead_mans_switch_client/) | 9.0.1.0.1 | :repeat: | Be notified when customers' odoo instances go down
[disable_odoo_online](disable_odoo_online/) | 9.0.1.0.0 | :repeat: | Remove odoo.com bindings
[letsencrypt](letsencrypt/) | 9.0.1.0.0 | :repeat: | Request SSL certificates from letsencrypt.org
[mail_cleanup](mail_cleanup/) | 9.0.1.0.0 | :repeat: | Mark as read or delete mails after a set time
[mail_environment](mail_environment/) | 9.0.1.0.0 | :repeat: | Configure mail servers with server_environment_files
[mass_editing](mass_editing/) | 9.0.1.0.0 | :repeat: | Mass Editing
[menu_technical_info](menu_technical_info/) | 9.0.1.0.0 | :repeat: | Fast way to look up technical info about menu item.
[module_prototyper](module_prototyper/) | 9.0.0.1.0 | :repeat: | Prototype your module.
[password_security](password_security/) | 9.0.1.0.2 | 9.0.1.2.3 | Allow admin to set password security requirements.
[res_config_settings_enterprise_remove](res_config_settings_enterprise_remove/) | 9.0.1.0.0 | :repeat: | Remove fields in all settings views marked as enterprise
[scheduler_error_mailer](scheduler_error_mailer/) | 9.0.1.0.0 | :repeat: | Scheduler Error Mailer
[server_environment](server_environment/) | 9.0.1.2.0 | :repeat: | move some configurations out of the database
[server_environment_files_sample](server_environment_files_sample/) | 9.0.1.0.0 | :repeat: | sample config file for server_environment
[test_configuration_helper](test_configuration_helper/) | 9.0.1.0.0 | :repeat: | Configuration Helper - Tests
[users_ldap_mail](users_ldap_mail/) | 9.0.1.0.0 | :repeat: | LDAP mapping for user name and e-mail
[users_ldap_populate](users_ldap_populate/) | 9.0.1.0.0 | :repeat: | LDAP Populate


Unported addons
---------------
addon | version | OCA version | summary
--- | --- | --- | ---
[auth_admin_passkey](auth_admin_passkey/) | 8.0.2.1.1 (unported) | :repeat: | Authentification - Admin Passkey
[auth_dynamic_groups](auth_dynamic_groups/) | 8.0.1.0.0 (unported) | :repeat: | Have membership conditions for certain groups
[auth_from_http_basic](auth_from_http_basic/) | 1.0 (unported) | :repeat: | Authenticate via HTTP basic authentication
[auth_from_http_basic_logout](auth_from_http_basic_logout/) | 1.0 (unported) | :repeat: | Authenticate via HTTP basic authentication (logout helper)
[base_external_dbsource](base_external_dbsource/) | 9.0.1.0.0 (unported) | 9.0.1.0.1 | External Database Sources
[email_template_template](email_template_template/) | 1.0 (unported) | :repeat: | Templates for email templates
[fetchmail_attach_from_folder](fetchmail_attach_from_folder/) | 8.0.1.0.1 (unported) | :repeat: | Attach mails in an IMAP folder to existing objects
[fetchmail_notify_error_to_sender](fetchmail_notify_error_to_sender/) | 8.0.1.0.0 (unported) | 9.0.1.0.0 | If fetching mails gives error, send an email to sender
[import_odbc](import_odbc/) | 1.3 (unported) | :repeat: | Import data from SQL and ODBC data sources.
[ir_config_parameter_viewer](ir_config_parameter_viewer/) | 0.1 (unported) | :repeat: | Ir.config_parameter view
[language_path_mixin](language_path_mixin/) | 8.0.1.0.0 (unported) | :repeat: | Setting the partner's language in RML reports
[mgmtsystem_kpi](mgmtsystem_kpi/) | 7.0.1.1.1 (unported) | :x: | Key Performance Indicator
[qweb_usertime](qweb_usertime/) | 8.0.1.0.0 (unported) | :x: | Add user time rendering support in QWeb
[security_protector](security_protector/) | 0.1 (unported) | :repeat: | Security protector
[server_env_base_external_referentials](server_env_base_external_referentials/) | 1.0 (unported) | :repeat: | Server environment for base_external_referential
[super_calendar](super_calendar/) | 8.0.0.2.0 (unported) | :repeat: | This module allows to create configurable calendars.
[users_ldap_groups](users_ldap_groups/) | 8.0.1.2.0 (unported) | :repeat: | Adds user accounts to groups based on rules defined by the administrator.
[web_context_tunnel](web_context_tunnel/) | 8.0.2.0.0 (unported) | :repeat: | Web Context Tunnel

[//]: # (end addons)

Translation Status
[![Transifex Status](https://www.transifex.com/projects/p/OCA-server-tools-9-0/chart/image_png)](https://www.transifex.com/projects/p/OCA-server-tools-9-0)

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
