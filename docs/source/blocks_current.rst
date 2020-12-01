==================
Heading blocks
==================

Only one of these should appear on any given page.  To create a heading banner:

* Go to Structure => Block layout => Custom block library
* Add custom block
* Select basic
* Enter a block description; this is what appears in the block library as the name of the block
* Enter the body.   Use the header banner code below to provide the correct style.
* **DO NOT** add an image.

When placing the block:

* add the block to the Header section on the block layout page by clicking Place block
* the block must be ordered just above the disabled blocks to keep the block from interfering with menus, site slogan blocks.
* set the block CSS class to ilao-banner-block to cause it to display correctly full-width.

.. image:: ../assets/header-block-config.png


Header banner code
=====================

This is the code used in the header banner to provide the correct style.

.. code-block:: html
   
   <div style="background-color:#F8FAFA;width:100%; padding:20px;font-weight:bold;box-shadow: 0 0.125rem 0.5rem rgba(106,107,113,0.2);">
   <p style="padding-bottom:0;font-weight:bold;">
   Text goes here
   </p>
   </div>



Current header banner blocks
==============================

* Donation-A
* Donation-B
* Donation-C

The covid-banner block has been moved to the left sidebar.
