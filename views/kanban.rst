============
Kanban
============


I Kanban fokusera man på att avsluta uppgifter inte inleda dem. Kanban kännetecknar också att man med tydliga och visuella signaler visar organisationens arbetsflöde. Man ser till att begränsa pågående arbetsuppgifter,  man använder visuella metoder som lappar för att kommunicera, man jagar flaskhalsar och man ser till att återkoppla för att effektivisera ytterligare.

.. image:: Markering_833.png

Kanban-strukturen::
    <kanban>
           Lista ingående fält         
           <field name="priority"/>
           <field name="xxxx"/>
                    
          <progressbar/>
          
                    
                    <templates>
                           Beskrivning av lappen
                    </templates>
   </kanban>


1) Kanban-record::
     <kanban 
         default_group_by="stage_id" 
                     class="o_kanban_small_column o_opportunity_kanban" 
         on_create="quick_create" 
         quick_create_view="crm.quick_create_opportunity_form" 
         archivable="false">

2) Progressbar::

     <progressbar field="activity_state" 
         colors="{&quot;planned&quot;: &quot;success&quot;, &quot;today&quot;: &quot;warning&quot;, &quot;overdue&quot;: &quot;danger&quot;}" 
         sum_field="planned_revenue" 
         help="This bar allows to filter the opportunities based on scheduled activities."/>
 
3) Lappen::
     <templates>
            <t t-name="kanban-box">
                <div t-attf-class="#{kanban_color(record.color.raw_value)} oe_kanban_global_click">
                    <div class="o_dropdown_kanban dropdown"/>  Meny
                </div>                            
                <div class="oe_kanban_content">
                         Innehåll
                        <div class="o_kanban_record_bottom">
                            <div class="oe_kanban_bottom_left" />
                            <div class="oe_kanban_bottom_right" />
                        </div>
                </div>
            </t>
        </templates>


Hela kanban-koden::

    <kanban default_group_by="stage_id" class="o_kanban_small_column o_opportunity_kanban" on_create="quick_create" quick_create_view="crm.quick_create_opportunity_form" archivable="false">
                    <field name="stage_id" options="{&quot;group_by_tooltip&quot;: {&quot;requirements&quot;: &quot;Description&quot;, &quot;legend_priority&quot;: &quot;Use of stars&quot;}}"/>
                    <field name="color"/>
                    <field name="priority"/>
                    <field name="planned_revenue"/>
                    <field name="kanban_state"/>
                    <field name="activity_date_deadline"/>
                    <field name="user_email"/>
                    <field name="user_id"/>
                    <field name="partner_address_email"/>
                    <field name="message_needaction_counter"/>
                    <field name="partner_id"/>
                    <field name="activity_summary"/>
                    <field name="active"/>
                    <field name="company_currency"/>
                    <field name="activity_state"/>
                    <field name="activity_ids"/>
                    <progressbar field="activity_state" colors="{&quot;planned&quot;: &quot;success&quot;, &quot;today&quot;: &quot;warning&quot;, &quot;overdue&quot;: &quot;danger&quot;}" sum_field="planned_revenue" help="This bar allows to filter the opportunities based on scheduled activities."/>
                    <templates>
                        <t t-name="kanban-box">
                            <div t-attf-class="#{kanban_color(record.color.raw_value)} oe_kanban_global_click">
                                <div class="o_dropdown_kanban dropdown">

                                    <a class="dropdown-toggle o-no-caret btn" role="button" data-toggle="dropdown" href="#" aria-label="Dropdown menu" title="Dropdown menu">
                                        <span class="fa fa-ellipsis-v"/>
                                    </a>
                                    <div class="dropdown-menu" role="menu">
                                        <t t-if="widget.editable"><a role="menuitem" type="edit" class="dropdown-item">Edit</a></t>
                                        <t t-if="widget.deletable"><a role="menuitem" type="delete" class="dropdown-item">Delete</a></t>
                                        <ul class="oe_kanban_colorpicker" data-field="color"/>
                                    </div>
                                </div>
                                <div class="oe_kanban_content">
                                    <div>
                                        <strong class="o_kanban_record_title"><field name="name"/></strong>
                                    </div>
                                    <div>
                                        <field name="tag_ids" widget="many2many_tags" options="{'color_field': 'color'}"/>
                                    </div>
                                    <div class="text-muted o_kanban_record_subtitle">
                                        <t t-if="record.planned_revenue.raw_value"><field name="planned_revenue" widget="monetary" options="{'currency_field': 'company_currency'}"/><span t-if="record.partner_id.value">,</span></t> <span t-if="record.partner_id.value"> <t t-esc="record.partner_id.value"/></span>
                                    </div>

                                    <div class="o_kanban_record_bottom">
                                        <div class="oe_kanban_bottom_left">
                                            <field name="priority" widget="priority" groups="base.group_user"/>
                                            <t t-if="record.message_needaction_counter.raw_value">
                                                <span role="alert" class="oe_kanban_mail_new" title="Unread Messages"><i class="fa fa-comments" aria-label="Unread messages" role="img"/><t t-raw="record.message_needaction_counter.raw_value"/></span>
                                            </t>
                                            <field name="activity_ids" widget="kanban_activity"/>
                                        </div>
                                        <div class="oe_kanban_bottom_right">
                                            <img t-att-src="kanban_image('res.users', 'image_small', record.user_id.raw_value)" t-att-title="record.user_id.value" t-att-alt="record.user_id.value" width="24" height="24" class="oe_kanban_avatar"/>
                                        </div>
                                    </div>
                                </div>
                                <div class="oe_clear"/>
                            </div>
                        </t>
                    </templates>
                </kanban>




