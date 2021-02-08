========================
SMS Integration
========================

.. note:: This is not built but documentation to guide the build.  This will be built out using Twilio Studio and ILAO API calls.

How This Will Work
====================

Users will text "legal help" to a specific telephone number and provide their legal issue.  Only legal issues offered over Guided Navigation can be triaged over SMS in our pilot.  Users with issues outside of these limited areas will be redirected to apply to Get Legal Help on the website.  

See `conceptual prototype <https://kywpl3.axshare.com/#g=1&p=home>`_.

Legal issue not in Illinois
------------------------------

* Redirect to LSC
* track user as out of state

Legal issue in Guided Navigation
------------------------------------


Legal issue outside Guided Navigation
---------------------------------------
User is sent to /get-legal-help on website



Required APIs for Intake
===========================

* Zip code validation
* Race list
* Ethnicity list
* Income levels per household size
* Income type entities
* Callback types

Required APIs for Triage
===========================

* Classifier processing