============
Diagram
============

* Urval, grupperingar, värden dynamiskt valbara
* Lägg på anslagstavla


.. image:: Markering_846.png


kod för sökrutan::

        <record id="crm_lead_view_graph" model="ir.ui.view">
            <field name="name">crm.lead.view.graph</field>
            <field name="model">crm.lead</field>
            <field name="arch" type="xml">
                <graph string="Opportunities">
                    <field name="stage_id" type="col"/>
                    <field name="user_id" type="row"/>
                </graph>
            </field>
        </record>


