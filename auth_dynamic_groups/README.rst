[![Build Status](https://travis-ci.org/zeroincombenze/server-tools.svg?branch=9.0)](https://travis-ci.org/zeroincombenze/server-tools)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/server-tools/badge.svg?branch=9.0)](https://coveralls.io/github/zeroincombenze/server-tools?branch=9.0)
[![codecov](https://codecov.io/gh/zeroincombenze/server-tools/branch/9.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/server-tools/branch/9.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-9.svg)](https://github.com/OCA/server-tools/tree/9.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-9.svg)](http://wiki.zeroincombenze.org/en/Odoo/9.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-9.svg)](http://wiki.zeroincombenze.org/en/Odoo/9.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-9.svg)](http://erp9.zeroincombenze.it)




































[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

Description
===========
This module allows defining groups whose membership is a condition expressed as
python code. For every user, it is evaluated during login if she belongs to
the group or not.

Installation
------------





Configuration
-------------





Usage
-----






Check `Dynamic` on a group you want to be dynamic. Now fill in the condition,
using `user` which is a browse record of the user in question that evaluates
truthy if the user is supposed to be a member of the group and falsy if not.

There is a constraint on the field to check for validity if this expression.
When you're satisfied, click the button `Evaluate` to prefill the group's
members. The condition will be checked now for every user who logs in.

Example
We have a group called `Amsterdam` and want it to contain all users from
city of Amsterdam. So we use the membership condition

```
user.partner_id.city == 'Amsterdam'
```

Now we can be sure every user living in this city is in the right group, and we
can start assigning local menus to it, adjust permissions, etc. Keep in mind
that view overrides can also be restricted by a group id, this gives a lot of
possibilities to dynamically adapt views based on arbitrary properties
reachable via the user record.

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
