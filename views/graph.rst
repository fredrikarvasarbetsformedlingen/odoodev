============
Grafik
============

* Etiketter för gjorda val (filter/gruppering/favorit)
* Använd förstoringsglaset för att se extra funktioner


.. image:: Markering_823.png



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


.. image:: Markering_824.png

Första field name är standardsökningen::

    <field name="name" string="Opportunity" 
       filter_domain="['|','|','|',
            ('partner_id','ilike',self),
            ('partner_name','ilike',self),('email_from','ilike',self),
            ('name', 'ilike', self)]"/>
            
            
