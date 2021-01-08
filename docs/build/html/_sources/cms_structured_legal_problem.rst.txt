=========================
Legal Problem
=========================

A Legal Problem is the top-level container for structured content. All other types of structured content are relate back to one or more legal problems (although depending on the use case, one could render the other elements separately).

.. note::  Fields should comply with our content style guide.

To create a legal problem:

* Add a title. This should describe the problem to be solved or prevented using the embedded solutions.
* Add a subtype.  This should describe any subcategory of a problem.  For example, if the legal problem is "Being a victim of domestic violence," the subtypes might include:

  * Getting an order of protection against a spouse
  * Changing or renewing an order of protection against a spouse
  * Getting a civil no contact order for sexual assault, rape, or sexual abuse.
  
* Add a content description.  This is the description that will 
* Add a meta description.  This is the description that will be used in social media, search indexes, and in any API.  This should be limited to 300 characters.
* Optionally, add a disambiguation description.  This is used to better describe how one problem is different from a related problem.  Examples:

  * For the problem "Being evicted from an apartment" with a subtype of "Private housing" it may have a disambiguation description of "This applies when the tenant is not using a housing voucher and/or their rent is not based on their income." to distinguish it from the problem "Being evicted from an apartment" with a subtype of "subsidized housing"
  * For the problem "Being a victim of abuse" with a subtype of "Getting an order of protection against a spouse," it may have a disambiguation description of "This applies when you do not currently have an order of protection and need to protect yourself from abuse" to distinguish it from other subtypes.

* Tag the legal problem to one or more legal issues. 
* Select the primary legal category
* Add a legal code.  Legal codes should come from either the LSC problem codes or the `LIST <https://taxonomy.legal>`_ codes.  

.. image:: ../assets/cms_structured_legal_code.png

The above image includes the legal code for Food stamps from both the LSC problem codes and LIST.

.. note::  Ideally, we would update this to use a taxonomy.

* Add at least one life area affected.  This is an `ILAO-hosted taxonomy <https://www.illinoislegalaid.org/admin/structure/taxonomy_manager/voc/life_areas>`_.  As of January 2021, the terms include:
  
  * Ability to work
  * Consumer rights
  * Creditworthiness
  * Driving privileges
  * Family
  * Freedom to move
  * Health and safety
  * Housing
  * Immigration status
  * Income
  * Last wishes
  
* Add a possible solution to solve the problem.  This is just a reference to an existing Legal Solution (see the Legal Solution documentation).
* Optionally, add up to 2 preventative solutions.  A preventative solution should help the user avoid the problem.  For example, if the legal problem is I am being evicted, a preventative solution may be to cure a late rent payment.  
* Optionally, add a FAQ by adding individual Legal Questions.  This is just a reference to an existing Legal Question (see the Legal Question documentation).
* Optionally, add one or more related resources by adding individual pieces of legal content.  This is just a reference to an existing Legal content, portal main pages, and toolbox content.  

.. note::  We envision that the API will automatically pull in data about related resources, such as last revised dates and content format.

* Optionally, add any content management tags
* Indicate whether a translation should be requested. 
* Indicate whether an existing transation should be marked as outdated.

.. note:: A legal problem itself contains no real content.  It is a container for other content.  As such, it does not have the last reviewed/revised dates that other content types have.  It will inherit the oldest reviewed/revised dates from its child components.

Full add/edit form
====================

.. image:: ../assets/cms-structured-legal-problem.png

