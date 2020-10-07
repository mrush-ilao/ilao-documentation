==========================
Legal content reporting
==========================

Available reports:

* `Content main report (all content) <https://www.illinoislegalaid.org/admin/content>`_
* `Find legal content report <https://www.illinoislegalaid.org/admin/reporting/content/legal-content>`_

Main content report
=====================
This is the basic Drupal report for content.  It includes all available content types.

Report data
---------------
The report includes:

* the ID (node ID)
* the title
* the content type
* the format (this applies only to legal content)
* the author
* the date published (this is the created date unless manually changed)
* the last updated date.  This is the system date.  For legal content specific dates, use the find legal content report.

Filters
-----------
This report can be filtered on:

* node ID.  This will return a specific node. 
* Title (contains)
* Content type (this is the system content type like legal content, event, basic page)
* Published status (yes or no)
* Translation language.  Using this will filter out translations for the same node.


Bulk actions
---------------
This is the system set of actions that can be applied to content.  Some of these are not relevant.

* Delete content  **Be careful** this will in fact delete selected content.  
* Save content.  This will re-save content and update the last updated/changed date.
* Publish content.  This will publish unpublished content AND update the last updated/changed date.  It will not move legal content revisions that is under moderation from an unpublished state like draft/revise to published.  
* Unpublish content.  This will unpublish published content and update the last updated/changed date.  
* Update URL alias.  **Use only if Gwen tells you to**  This will reset path aliases.  This is helpful for some content types **other than legal content.**

.. todo:: Update the action list to only relevant items.


Legal content report
======================
Includes the following content types:

* Legal content
* ADRM content
* Portal content
* Toolboxes
* Toolbox tools
* Tool steps

Report data
-----------------

* Node ID (ID) of the content
* Title of the content
* Format of the content.  Applies only to legal content.
* Primary legal category of the content. 
* Created date.  This is the date the system creates when the node is first created in any state.  It does not necessarily represent published date.
* Original author
* Last changed.  This is the date the system last recorded a change.  This is triggered whenever:

  * A user saves the node
  * A system update saves the node.  This may happen if there is a scheduled change, Google analytics data added, or any other system action that causes a call to the node save function.
  
* Last revised.  This is the "last internal revision" field. This date is manually sent when a staff user makes a substantive change to the content. Does not include typos, grammatical fixes, or style changes. Does include anything that adds or removes information, especially law changes.
* Last expert review. 
* Published status (Yes or No)
* Language of the node (content in more than one language will have multiple rows in the report)

.. note::  The last revised and last expert review fields are not translatable in legal content but are translatable in toolbox, tool, and tool step content.    The last changed date is per language. 

.. todo:: Last revised and last expert review fields need to be added to ADRM content; standardize date fields (translatable vs not translatable), apply formats to toolbox, ADRM content, portal pages.    


Filters
--------------
The find legal content report has many filters.  Filters are based on an AND condition.  

* ID is the node ID
* Title is the partial match of the title
* Category is the primary legal category for the content.  This is the single select dropdown for category versus the legal issues multiple-select field.
* Published status (yes or no).  Note that publish status is per node.  An unpublished translation in Spanish with a published English version would show as published.
* Content format.  This applies to legal content only and is set based on the paragraphs bundles included in the node.  
* Translation exists is duplicative of the translation language field and should be removed.
* Created filters on the created date and can be set with a start date and/or end date
* Last revised filters on the last internal revision date and can be set with a start date and/or end date
* Last expert review filters on the last expert review date and can be set with a start date and/or end date
* Level (basic or advanced)
* Legal position
* Restrict (whether content is marked as restricted to legal aid or pro bono members)
* Jurisdiction (whether content is marked as national, statewide or relevant only to specific counties or cities) and to what counties, cities, or zip codes the content is tagged.  Applies only to legal content type content.
* Annual updates tagged to the content  Applies only to legal content type content and ADRM content.
* Whether the translation is currently marked as outdated
* Whether there is an open request to create a translation.  This field applies only to legal content.  
* Translation language.  This should be used to limit the list to English, Spanish or Polish.
* Content management tags.  This should be used to limit the results to those that have a term from the content management tags taxonomy.  Separate terms by commas.

.. note:: because of the way jurisdictions were handled on the D7 site, the counties, cities and zipcodes show what jurisdictions the content is tagged to but the report **does not show** whether the relationship between the jurisdiction (some part of Illinois) includes or excludes the jurisdictions.  As of August 2020, the jurisdiction data is not used in any way on the website's front-end.

.. todo:: Determine whether toolbox and portal content should have translation fields.  

Moderated content report
===========================
This is a system report accessible from the main content report.  It needs review.

Pending reports
=================

We need to add reports for:

* comments and ratings
* localized content
* toolbox and tool usage reports
* revision historical data
* possibly other reports TBD under structured content grant

