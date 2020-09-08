========================
Local content tool
========================

The local content tool appears as a wand on the WYSIWYG tool next to the spell check button.

.. image:: ../assets/cms-local-content-button.png

The tool is used to insert region specific content and supports limiting the markup to the county, city, or zip code level.

.. note:: The tool does not support editing of existing markup.  To edit, a content editor must edit within the inserted span tags.

.. image:: ../assets/cms-local-content-wizard.png

To use:

* Select the region type
* Use the autocomplete to insert a county, city or zip code
* Type in the text you want to include.

This will insert code like: {span|county|Madison|This is content specific to Madison county.} formatted as:

* span
* region type
* region name
* content

.. image:: ../assets/cms-local-inserted.png

The content can then be formatted or edited within the WYSIWYG window.

What users see
=================

Users will see the region specific markup only if it applies to them.  For example a user in zip code 60603 (Chicago, Cook county) would see mark up tagged to 60603, Chicago, or Cook County but would not see mark up tagged to 60626, Evanston, or Kane county.

