[![Build Status](https://travis-ci.org/zeroincombenze/server-tools.svg?branch=8.0)](https://travis-ci.org/zeroincombenze/server-tools)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/server-tools/badge.svg?branch=8.0)](https://coveralls.io/github/zeroincombenze/server-tools?branch=8.0)
[![codecov](https://codecov.io/gh/zeroincombenze/server-tools/branch/8.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/server-tools/branch/8.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-8.svg)](https://github.com/OCA/server-tools/tree/8.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-8.svg)](http://erp8.zeroincombenze.it)


































[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

SUPER CALENDAR
==============

This module allows to create configurable calendars.

Through the 'calendar configurator' object, you can specify which models have
to be merged in the super calendar. For each model, you have to define the
'description' and 'date_start' fields at least. Then you can define 'duration'
and the 'user_id' fields.

The 'super.calendar' object contains the merged calendars. The
'super.calendar' can be updated by 'ir.cron' or manually.

Installation
------------




Configuration
-------------





After installing the module you can go to

*Super calendar > Configuration > Configurators*

and create a new configurator. For instance, if you want to see meetings and
phone calls, you can create the following lines

Meetings:

.. figure:: static/description/meetings.png
   :alt: meetings
   :width: 600 px

Phonecalls:

.. figure:: static/description/phone_calls.png
   :alt: phone calls
   :width: 600 px

Then, you can use the 'Generate Calendar' button or wait for the scheduled
action (‘Generate Calendar Records’) to be run.

When the calendar is generated, you can visualize it by the 'super calendar' main menu.

Here is a sample monthly calendar:

.. figure:: static/description/month_calendar.png
   :alt: monthly calendar
   :width: 600 px

And here is the weekly one:

.. figure:: static/description/week_calendar.png
   :alt: weekly calendar
   :width: 600 px

As you can see, several filters are available. A typical usage consists in
filtering by 'Configurator' (if you have several configurators,
'Scheduled calls and meetings' can be one of them) and by your user.
Once you filtered, you can save the filter as 'Advanced filter' or even
add it to a dashboard.

Usage
-----







Known issues / Roadmap
----------------------




Bug Tracker
-----------





Bugs are tracked on `GitHub Issues <https://github.com/OCA/server-tools/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smashing it by providing a detailed and welcomed feedback
`here <https://github.com/OCA/server-tools/issues/new?body=module:%20super_calendar%0Aversion:%208.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.


Credits
-------









### Contributors




* Lorenzo Battistini <lorenzo.battistini@agilebg.com>
* Alejandro Santana <alejandrosantana@anubia.es>
* Agathe Mollé <agathe.molle@savoirfairelinux.com>

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

Icon
----
Module icon from WebIconSet.com: http://www.webiconset.com/mobile-icon-set/

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
