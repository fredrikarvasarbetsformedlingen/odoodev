=======
Field Widgets
=======

Each field type is displayed in the form with the appropriate default widget. But additional alternative widgets are available to be used.

For text fields, we have the following widgets:

  • **email** is used to make the email text an actionable "mail-to" address. 
  • **url** is used to format the text as a clickable URL.
  • **html** is used to render the text as HTML content; in edit mode, it features a WYSIWYG editor to allow for the 
    formatting of the content without the need for using the HTML syntax.

For numeric fields, we have the following widgets:
handle is specifically designed for sequence fields in list views and displays a handle that allows you to drag lines to a custom order.
float_time formats a float field with time quantities as hours and minutes. monetary displays a float field as the currency amount. It expects a currency_id companion field, but another field name can be provided with options="{'currency_field': 'currency_id'}".
progressbar presents a float as a progress percentage and can be useful for fields representing a completion rate.
percentage and percentpie are widgets to use with float fields.
For relational and selection fields, we have these additional widgets:
many2many_tags displays values as a list of button-like labels. many2many_checkboxes displays the selectable values as a list of checkboxes. selection uses the selection field widget for a many-to-one field.
radio displays the selection field options using radio buttons.
priority represents the selection field as a list of clickable stars. The selection
options are usually numeric digits.
state_selection shows a semaphore light for the Kanban state selection list.
The normal state is represented in gray, done is represented in green, and any other state is represented in red.
pdf_viewer is for binary fields (introduced in Odoo 12).
