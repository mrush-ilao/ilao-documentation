======================
Fast Entry Form
======================

The fast entry form can be used to quickly refer users to OTIS partners, bypassing all triage rules and the standard online intake forms.

Fast entry permissions
========================

The fast entry form is accessible at /get-legal-help/fast-entry but is only accessible to:

* ILAO staff
* Legal aid members who are also organization managers of an OTIS partner organization
* Website users who have been given the fast entry role within the organization settings of an OTIS partner organization by an organization manager of the OTIS partner organization


Fast entry form
====================

`Prototype form <https://7antm8.axshare.com/good_prototype.html>`_


Data capture & reporting
==========================

On submission, the form will create an etransfer into legal server. In the etransfer, the unique ID will be ilao-fe[triage-id] rather than the ilao-web[triage-id].  Because there is no triage the data will be slightly different than triage intake:

* triage created and triage changed time stamps should be the submission time, which will also match the intake created and intake changed times
* the triage status will be Bypassed
* source will be Fast Entry
* the user id associated with the application will be that of the user submitting the form
* last screen viewed will be fast entry form
* intake_organization will be the intake settings associated with the organization.  The system will select the first intake settings for the organization that matches the county of the user.  
* Legal problem term will be stored in the lsc_code table
* Legal problem term will be stored in the oas_triage_search field


.. todo:: Update triage status documentation

.. todo:: Evaluate whether an organization should have a fast entry intake settings simply for the purpose of tagging the organization and location in reports.



 A record will be created in ILAO's triage user database table.
