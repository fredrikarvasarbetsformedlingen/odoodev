============
Kalender
============




.. image:: Markering_844.png



kod för kalender::

       <calendar string="Meetings" date_start="start" date_stop="stop" date_delay="duration" all_day="allday"
                                  readonly_form_view_id="384" event_open_popup="true" event_limit="3" color="partner_id">
                <field name="name"/>
                <field name="partner_ids" write_model="calendar.contacts" write_field="partner_id"         
                                                                             avatar_field="image_small"/>
                <field name="is_highlighted" invisible="1"/>
            </calendar>
            
            
   

=========================
Söktyper
=========================
.. toctree::
   :maxdepth: 1

   freetext.rst

.. toctree::
   :maxdepth: 1

   filter.rst

.. toctree::
   :maxdepth: 1
   
   group_by.rst
