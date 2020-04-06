=======
Pivot Widgets
=======

In Pivot view a ``field`` can have a ``widget`` attribute to dictate its format. The ``widget`` should be a field formatter, of which the most interesting are ``date``, ``datetime``, ``float_time``, and ``monetary``.

**Example**

.. code-block:: python

    <pivot string="Timesheet">
        <field name="employee_id" type="row"/>
        <field name="date" interval="month" type="col"/>
        <field name="unit_amount" type="measure" widget="float_time"/>
    </pivot>/>
