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

* only to revision authors with the subject matter expert role
* can only be awarded to the same node/language/author pair once every 24 hours (so that we don't accidentally award points multiple times)

.. note:: Andrew needs to verify that we aren't awarding points to editors who aren't LCV members.  Another option may be to award the points and then send them a "hey, want to be an LCV? You already have 50 points." email.

Manual points 
=================================

Manual points may be awarded via a separate form and may optionally be tied to a legal content node.  This may be most helpful for content editorial contributions that are outside of workflow management such as:

* Easy form reviews
* Toolboxes, tools, tool steps
* Portal main pages





