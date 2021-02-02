===============================
Points System
===============================

.. note:: this is not yet built

Point Types
==============

Users with the role staff may create point categories and view a list of all point categories.

* Automatic points are awarded when a piece of legal content or ADRM content transitions across workflows

  * On transition from published to draft - this may be triggered when a user starts an assignment
  * On transition from ready to review to published - this may be triggered when a staff member finalizes submitted work
  * On transition from draft to published - this may be triggered when a staff member creates a draft, inputs SME changes, and then publishes the revision.
  * On transition from published to ready to review -- this may be triggered when a user turns in completed work and never saved it as a draft
  * On transition from draft to ready to review -- this may be triggered when a user turns in completed work and had saved as a draft
  
* Manual points are awarded by someone with the staff role. 

Points may be configured to be awarded at a flat rate or based on the number of words in the node. 

Rules for Automated Point Awards
==================================

Automated point awards will be awarded:

* to revision authors who do not have the staff or intern role
* can only be awarded to the same node/language/author pair once every 24 hours (so that we don't accidentally award points multiple times)


Manual points 
=================================

Manual points may be awarded via a separate form and may optionally be tied to a legal content node.  This may be most helpful for content editorial contributions that are outside of workflow management such as:

* Easy form reviews
* Toolboxes, tools, tool steps
* Portal main pages

Point Tracking
=================

Point awards should be recorded in the website with the following information:

* the timestamp of when the record is created
* the timestamp of when the record was last updated
* a reference to the point type awarded
* the user ID of the person earning the point.  

  * for automated points, it is always the revision author.
  * for manual points, it is the user added to the user field on the form
  
* the entity id of the node associated with the points, if one exists 

  * for automated awards, it is the node of the content being revised
  * for manual awards, it comes from the manual credit form.  

* the revision id of the revision being tracked, for automated awards 
* the language code of the revision, for automated awards 
* the primary legal category associated with the points

  * for automated awards, it is the primary legal category of the node at the time the points are awarded
  * for manual awards, it comes from the manual credit form
  
* the number of points awarded
* the number of words in the node at the time points were awarded
* the user id of the person awarding the points (for automated awards, this is anonymous as the system user)
* the date the points were earned (this may be different from when they are awarded)




  
  



