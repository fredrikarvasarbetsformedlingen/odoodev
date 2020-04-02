=======
Formulärwidgets
=======

Formulärwidgets för "many2many" -fält i Odoo
====

1. ``many2many`` widget (förvalt)
2. ``many2many_tags`` widget
3. ``many2many_checkboxes`` widget
4. ``many2many_kanban`` widget
5. ``many2many_counter`` widget
6. ``many2many_binary`` widget


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

Ett Facebookliknande flervalsmarkering.

.. image:: many2many_tags_widget.png

Alternativ
====

* ``no_quick_create`` - tar bort ``Create and edit...`` alternativet.
* ``no_quick_edit`` - tar bort ``Skapa "foo"`` alternativet.

.. image:: many2many_tags_widget2.png


* ``no_create`` - ``no_qick_create`` och ``no_create_edit`` kombinerat.


.. image:: many2many_widget.png




.. image:: many2many_checkboxes_widget.png



.. image:: many2many_kanban_widget.png

.. image:: x2many_counter_widget.png

.. image:: many2many_binary_widget.png
