.. _salesindex:

=========================
Kundorder och fakturering
=========================
.. toctree::
   :maxdepth: 1

   introduction.rst

Migrera kundregister från Fortnox
---------------
https://support.fortnox.se/hc/sv/articles/360000632189-Exportera-f%C3%B6retag-kontakter

Följ instruktionerna på länken ovan. Om det blir trassel med teckenuppsättningen, gör då så att du öppnar kundregistret i Google Docs. Dokumentet är skrivskyddat och det stänger du av och sen exporterar du dokumentet till lokal disk.

Detta ”nya” dokumentet ska då ha korrekt teckenuppsättning. Här kan du passa på att rensa bort några av de 69 kolumner från Fortnox som du inte vill importera till Odoo. Ofta är det namn, e-post och adress man vill importera, men det kan variera från gång till annan.

I Odoo, gå till Kontakter, välj att visa kontakter i valet "Lista" (inte förvalet Kanban), välj Importera och ladda upp din fil.

Offerter
---------------
.. toctree::
   :maxdepth: 1

   Xcreate_my_first_quotation
   Xsend_quotation_by_email.rst
   Xchange_your_quotation_layout.rst
   Xset_default_terms_and_conditions.rst
   Xapply_default_tax.rst
   Xsections_on_sales_orders.rst

Offertmallar
------------------
.. toctree::
   :maxdepth: 1

   quick_create_quotation_using_quotation_template.rst
   Xincrease_your_sales_with_suggested_products.rst
   Xonline_customer_approval_on_quotation.rst
   Xonline_customer_approval_and_payment_on_quotation.rst

Produkter och prissättning
-------------------
.. toctree::
   :maxdepth: 1

   apply_manual_discount.rst
   Xadapt_price_based_on_customer_segment.rst
   Xadapt_price_based_on_customer_location.rst
   Xcompute_and_apply_discount_from_pricelist.rst
   X../inventory/inventory_costing/average_costing.rst
   Xproduct_price_per_company.rst
   
   
Fakturering
---------
.. toctree::
  :maxdepth: 1

  Xpro-forma.rst
  Xinvoice_on_order_qty.rst
  Xinvoice_on_deliver_qty.rst
  credit_note_from_order.rst
  Xsingle_order_for_multiple_orders.rst
   
..
  Sales Margin
  ------------
  .. toctree::
    :maxdepth: 1

  compute_sales_margin.rst

  Unit of Measure
  ---------------
  .. toctree::
   :maxdepth: 1

   product_unit_of_measure.rst
   pricelist_for_uom.rst

  Product and Tax
  ---------------
  .. toctree::
   :maxdepth: 1

   price_including_tax.rst
   price_including_tax_and_excluding_tax.rst

  Invoicing
  ---------
  .. toctree::
  :maxdepth: 1

  pro-forma.rst
  invoice_on_order_qty.rst
  invoice_on_deliver_qty.rst
  credit_note_from_order.rst
  single_order_for_multiple_orders.rst

  Delivery Charges
  ----------------
  .. toctree::
   :maxdepth: 1

   free_delivery.rst
   delivery_based_on_weight.rst

  Manage Inventory
  ----------------
  .. toctree::
   :maxdepth: 1

   make_to_order.rst

  Service Product
  ---------------
  .. toctree::
  :maxdepth: 1

  invoice_milestones.rst
  invoice_based_on_timesheet.rst

  Subscription
  ------------
  .. toctree::
  :maxdepth: 1

  subscription/setup_recurring_invoice.rst
  subscription/sell_subscription_throught_sales_quotation.rst
  subscription/sell_subscription_through_ecommerce_platform.rst

  Customer Portal
  ---------------
  .. toctree::
  :maxdepth: 1

  online_approval.rst
  online_payment.rst
  confirm_and_pay_online.rst
