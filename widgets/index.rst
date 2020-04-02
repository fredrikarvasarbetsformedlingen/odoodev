=======
Formulärwidgets
=======

Formulärwidgets för ``many2many`` -fält i Odoo
====

#. ``many2many`` widget (förvalt)
#. ``many2many_tags`` widget
#. ``many2many_checkboxes`` widget
#. ``many2many_kanban`` widget
#. ``many2many_counter`` widget
#. ``many2many_binary`` widget


``many2many`` widget (förvalt)
====

Widgeten ``many2many`` använder en förvald listvy för relaterad modell för att visa en lista av relaterade objekt.


Alternativ
====

* ``no_create`` - tar bort "Create" knappen.


Exempel
====

.. code-block:: python

    <field name="field_name" options="{'no_create': True}"/>


Widgeten ``many2many_tags``
****

En Facebookliknande flervalsmarkering.

.. image:: many2many_tags_widget.png

Alternativ
====

* ``no_quick_create`` - tar bort ``Create and edit...`` alternativet.
* ``no_quick_edit`` - tar bort ``Skapa "foo"`` alternativet.

.. image:: many2many_tags_widget2.png


* ``no_create`` - ``no_qick_create`` och ``no_create_edit`` kombinerat.


Exempel
====

.. code-block:: python

    <field name="field_name"
    widget="many2many_tags"
    options="{'no_create_edit': True}"/>


****


Widgeten ``many2many_checkboxes``
****

.. image:: many2many_checkboxes_widget.png


Enligt en notering i dokumentationen till Odoo:

.. This type of field display a list of checkboxes. It works only with m2ms. This field 
.. will display one checkbox for each record existing in the model targeted by the 
.. relation, according to the given domain if one is specified. Checked records will 
.. be added to the relation.


Det finns ingen möjlighet far denna widgt att skapa nya poster, exempelvis produkter.
****

.. image:: many2many_widget.png







.. image:: many2many_kanban_widget.png

.. image:: x2many_counter_widget.png

.. image:: many2many_binary_widget.png
