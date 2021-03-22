======================
OTIS SMS API
======================

This documents our integration between the website and SMS to provide the needed functionality between ILAO's database, LegalServer, and Twilio for online intake.

Create triage user
=====================
Within Twilio, we have the ILAO service for functions.  The `/otis-create-triage-user <https://ilao-8092.twil.io/otis-create-triage-user>`_ function creates a data packet based on ILAO's OTIS Rest API to create a triage user record in our database.  The API returns the UUID of the newly created triage user entity.



Update triage user
=====================
The `/otis-update-triage-user <https://ilao-8092.twil.io/otis-update-triage-user>`_ function creates a data packet based on ILAO's OTIS Rest API to update an existing triage user based on the UUID.  

It ignores any parameters that are not part of the ILAO OTIS Rest API.


Post to legal server
=======================

TBD


Get intake settings
======================

TBD
