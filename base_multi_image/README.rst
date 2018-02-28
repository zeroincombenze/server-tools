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
   :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
   :alt: License: AGPL-3

Multiple Images Base
====================

This module extends the functionality of any model to support multiple images
(a gallery) attached to it and allow you to manage them.

Installation
------------





This module adds abstract models to work on. Its sole purpose is to serve as
base for other modules that implement galleries, so if you install this one
manually you will notice no change. You should install any other module based
on this one and this will get installed automatically.

Configuration
-------------




Usage
-----







=====

To manage all stored images, you need to:

* Go to *Settings > Configuration > Multi images*.

... but you probably prefer to manage them from the forms supplied by
submodules that inherit this behavior.

Development

To develop a module based on this one:

* See module ``product_multi_image`` as an example.

* You have to inherit model ``base_multi_image.owner`` to the model that needs
  the gallery::

    class MyOwner(models.Model):
        _name = "my.model.name"
        _inherit = ["my.model.name", "base_multi_image.owner"]

        # If you need this, you will need ``post_init_hook_for_submodules``
        old_image_field = fields.Binary(related="image_main", store=False)

* Somewhere in the owner view, add::

    <field
        name="image_ids"
        nolabel="1"
        context="{
            'default_owner_model': 'my.model.name',
            'default_owner_id': id,
        }"
        mode="kanban"/>

* If the model you are extending already had an image field, and you want to
  trick Odoo to make those images to multi-image mode, you will need to make
  use of the provided :meth:`~.hooks.pre_init_hook_for_submodules`, like
  the ``product_multi_image`` module does::

    from openerp.addons.base_multi_image.hooks import \
        pre_init_hook_for_submodules


    def pre_init_hook(cr):
        pre_init_hook_for_submodules(cr, "product.template", "image")
        pre_init_hook_for_submodules(cr, "product.product", "image_variant")


.. image:: https://odoo-community.org/website/image/ir.attachment/5784_f2813bd/datas
   :alt: Try me on Runbot
   :target: https://runbot.odoo-community.org/runbot/149/8.0

Known issues / Roadmap
----------------------





* *OS file* storage mode for images is meant to provide a path where Odoo has
  read access and the image is already found, **not for making the module store
  images there**. It would be nice to add that feature though.

Bug Tracker
-----------





Bugs are tracked on `GitHub Issues
<https://github.com/OCA/server-tools/issues>`_. In case of trouble, please
check there if your issue has already been reported. If you spotted it first,
help us smashing it by providing a detailed and welcomed `feedback
<https://github.com/OCA/
server-tools/issues/new?body=module:%20
base_multi_image%0Aversion:%20
8.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Credits
-------





Original implementation
This module is inspired in previous module *product_images* from OpenLabs
and Akretion.





### Contributors





* Pedro M. Baeza <pedro.baeza@serviciosbaeza.com>
* Rafael Blasco <rafabn@antiun.com>
* Jairo Llopis <yajo.sk8@gmail.com>

### Funders

### Maintainer








.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

This module is maintained by the OCA.

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

To contribute to this module, please visit http://odoo-community.org.

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
