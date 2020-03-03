Resurser


En bra länk.
https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html


En bra film.

Live Coding: Documentation w/ ReadTheDocs.org (RTFD)

https://www.youtube.com/watch?v=UFYPLhhIDSg


Killens egna länk i filmen.

https://github.com/DevDungeon/reStructuredText-Documentation-Reference


Innehållsförteckning.



.. contents::



.. _salesindex:

=========================
Moduler / Arv
=========================
.. toctree::
   :maxdepth: 1

   classic_inherit.rst
   extentions.rst
   delegering.rst



.. note:: Colored boxes: note, seealso, todo and warnings

.. seealso:: Colored boxes: note, seealso, todo and warnings

.. todo:: Colored boxes: note, seealso, todo and warnings

.. warnings:: Colored boxes: note, seealso, todo and warnings

.. topic:: Your Topic Title

    Subsequent indented lines comprise
    the body of the topic, and are
    interpreted as body elements.

.. sidebar:: Sidebar Title
    :subtitle: Optional Sidebar Subtitle

    Subsequent indented lines comprise
    the body of the sidebar, and are
    interpreted as body elements.


.. image:: screens/screens.jpg


Bestrivning av Restructured Text

https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html


.. code-block:: html
    :linenos:

    <h1>code block example</h1>


This is a simple example::

    import math
    print 'import done'



.. toctree::
    :glob:

    Chapter1 description <chapter1>

========
Header 1
========

Header 1.1
==========

some text

Header 1.1.1
------------

some more text

Header 1.2
==========



=========================
Sökrutan
=========================
.. toctree::
   :maxdepth: 2

   search/index.rst



=========================
Vyer
=========================
.. toctree::
   :maxdepth: 2

   views/index.rst


=========================
Chatter
=========================
.. toctree::
   :maxdepth: 1

   chatter.rst

=========================
Aktivitet
=========================
.. toctree::
   :maxdepth: 1

   aktivitet.rst

=========================
Meny
=========================
.. toctree::
   :maxdepth: 1

   meny.rst

=========================
Widgets
=========================
.. toctree::
   :maxdepth: 1

   widgets.rst
   many2many_tags.rst

=========================
Datakatalog
=========================
.. toctree::
   :maxdepth: 1

   datakatalog.rst
