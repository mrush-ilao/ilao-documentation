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

`Prototype form <https://7antm8.axshare.com/revised_prototype.html>`_


Data capture & reporting
==========================

On submission, the form will create an etransfer into legal server. Because there is no triage the data will be slightly different than triage intake:

Oas Triage User Data Fields
------------------------------

* created should be the time stamp the form is submitted
* changed should be the time stamp the form is submitted
* intake_created should be the time stamp the form is submitted
* intake_changed should be the time stamp the form is submitted
* zip_code should be the zip code entered in the address fields
* last_screen_viewed should be fast-entry
* county should be derived from zip_code
* state should be pulled from address fields
* triage_status should be Intake Available
* intake_status should be eTransferred
* intake_organization should be: [TBD]
* lsc_code should be the name of the legal category term reference
* referral_source should be "Fast Entry"
* gender should be the gender name from the taxonomy
* race should be race name from the taxonomy
* marital_status should be should be the marital status name from the related taxonomy
* primary_language should be the language name from the related taxonomy
* etransfer_data should be the serialized etransfer packet


Other fields in ILAO's database
----------------------------------

* If the user entered a mobile phone, it should be stored in oas_triage_user__oas_mobile_phone
* Response to "Does client consent to receive confirmation and follow-up text messages from IllinoisLegalAid.org?* " should be stored in oas_triage_user__oas_opt_in_sms
* legal problem should be stored in oas_triage_user__oas_triage_search (check this) 

Notes only elements
----------------------

* Does client consent to text messages from referral organization should be appended to notes as "Client consents to text messages: Yes" or Client consents to text messages: No"
* Adverse party should be appended to notes as 
* Describe the client's problem as entered with a prefix of Problem description: 
* Upcoming dates/deadlines should be appended to notes formatted as "Upcoming court dates and deadlines: date (description); date(description)"
* Additional notes as entered with a prefix of Additional notes: 

Not stored elements
---------------------

* Yes/no for client consents
* Yes/no for related court date

If either of these are no, there should be no data saved at all and no eTransfer created.


.. todo:: Evaluate whether an organization should have a fast entry intake settings simply for the purpose of tagging the organization and location in reports.



 A record will be created in ILAO's triage user database table.
