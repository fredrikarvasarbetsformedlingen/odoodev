=============================
Vyer startas med en action
=============================



.. image:: Markering_845.png



kod för action::

    <search string="Search Opportunities">
                    <field name="name" string="Opportunity" filter_domain="['|','|','|',('partner_id','ilike',self),('partner_name','ilike',self),('email_from','ilike',self),('name', 'ilike', self)]"/>
                    <field name="tag_ids" string="Tag" filter_domain="[('tag_ids', 'ilike', self)]"/>
                    
