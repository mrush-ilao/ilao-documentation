==================================
Toolbox and related content types
==================================

.. toctree::
   :maxdepth: 2
   :caption: Toolboxes:
   
   cms_toolboxes_admin
   cms_tools_admin
   cms_tool_step_admin
   content_toolbox_use

The toolboxes are a form of legal content designed to help guide a user through a long-term process.  The toolbox includes features that differentiate it from other forms of legal content, including:

* A progress tracker that allows users to check-off their progress
* For logged in users, it remembers their progress over the course of a year and allows the user to pick up where they left off
* For logged in users, it will send follow-up reminders via email and text messages based on the user's notification preferences.

A toolbox should:

* Contain at least 2 related tools.  Each tool must have at least one step.
* Be tied to an existing portal 

Creating a Toolbox
====================

When creating a toolbox
---------------------------

* Add a title
* Add a content description; this is the description that will be used in content pages and search results.
* Add a meta description; this is the description that will be used in search engines like Google and social media
* Selector form label.  This is what appears in a toolbox selector form on portal content
* Overall level of effort. Use easy for anything that can be completed in 1 week or less, medium for anything that takes 1-6 months and hard for anything that typically takes 6 months or more. (this is likely to be deprecated as the level applies more to tools than toolboxes)
* Page components: add a split column layout to add summaries of each tool in the toolbox or other information.  The split column layout requires two items, each with a title and body.  


Do not use:

* Fast fact block; this will be removed in a future update
* Page components other than split column layout.

What users see
------------------

* There is a form automatically created for all of the tools in the toolbox.  
* The `Using this toolbox <https://www.illinoislegalaid.org/block/231>`_ is static and shared across all toolboxes.
* Fast fact blocks are not displayed to users.
* Buttons in split column layouts do not display to users.

.. todo::  Update the level of effort help text; Deprecate these fields and remove from CMS: fast fact block, level of effort


.. image:: ../assets/toolbox_view.png