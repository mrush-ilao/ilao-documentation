=======================
Automated eUpdate
=======================

The automated eUpdate compiles information from the website into a Mailchimp template that is then sent to targeted groups.

Who Gets the eUpdate
=======================

Any registered user of IllinoisLegalAid.org can get the eUpdate.  When creating an account:

* Legal aid members default newsletter settings to select the eUpdate every Tuesday morning
* All others membership types default newsletter settings to select the eUpdate every month.

.. note:: Users may unselect the defaults before saving their account.

What is in the eUpdate
===========================
The weekly version includes content from the current date minus 7 days
The monthly version includes content from the current date minus 30 days


The content includes:

* Legal content, portal main pages, tools, toolboxes, and ADRM content that has a last revised date within the selected timeframe
* The next 3 upcoming calendar events
* The 3 most recently updated published job postings

Sending
===========
The eUpdate is scheduled to send at:

* 9am Tuesdays for weekly subscribers.
* 9am on the 1st of the month for weekly subscribers.

Because the scheduled task runs once per hour, it may be delayed and run anytime between 9am and 10am.

Tracking
==========
Links within the eUpdate are tracked using:

* campaign = date the eUpdate is sent
* source = eUpdate
* medium = email

These can be tracked in Google Analytics.  Mailchimp also tracks data.


Testing
===========
There is a check group in the master segment that is made up of Gwen and various members of the QED42 team.  This is the default send-to on all non-production instances to prevent accidentally sending from these machines to all users.

.. note:: Mailchimp campaigns sent to the check group may be safely deleted.




