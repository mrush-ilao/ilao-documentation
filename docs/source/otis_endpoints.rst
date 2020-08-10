======================
Triage rule endpoints
======================

There are 3 supported end points in OTIS webforms:

* by_pass
* pro_bono_end_point
* phone_end_point

These are set as the webform element's key.

.. image:: ../assets/otis_endpoints.png

These endpoints are set via responses to Yes/No questions.  When no end point is set, the user will not get routed to intake or referrals.  


Standard Usage
================

Bypass
----------
Bypass is used when a program wants users to call immediately versus apply online due to the emergency nature of a legal issue.  

The standard question for bypass is "Online applications are not taken for this problem, but there is a dedicated number to call for help. Would you like to know how to reach them?"  

* When the user says yes, they are given the bypass exit screen
* When the user says no, they are diverted to referrals to other organizations

In the webform, the question must have a key of "by_pass"

Pro Bono
----------

Phone
-------

The standard usage for phone_end_point is to ask a user a yes/no question if they have a safe phone number to call them at.  When this 