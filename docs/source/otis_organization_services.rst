============================
Managing Location Services
============================

Locations within an organization have services.  An organization may have one service or may have multiple services, each with different eligibility rules and service areas.

ILAO staff, organization managers, and OTIS managers can all add or edit locations.  

The add/edit location form is the same for both ILAO staff and organization/OTIS managers.

.. note:: Because of the complexity of the logic behind the location services form, it does take longer than other forms to load.


Types of Location Services
============================
Our platform supports five types of location services, each with different fields that must be captured in the location services form.  These are:

* Direct representation
* Legal information and education (not a legal self-help center)
* Legal self-help center
* Lawyer referral service
* Policy, impact litigation, support, or other

Common Elements
==================
All 5 types share some fields:

* Title
* Whether the service is open or not.  A service must be both open and published to be returned in referrals or displayed on the website.
* Location.  The location associated with the service.
* Service type (the 5 available types)
* Phone number
* Income eligibility
* Populations
* Service area
* Parent organization


.. todo:: The location dropdown is difficult to use as it list the locations by name and does not filter out locations organization managers do not manage.

Phone number
-------------
Every service requires a phone number.  By checking "Yes" to "Same phone number as location," the phone number from the location will be copied.

Income eligibility
--------------------
Every service should provide income eligibility and costs.  These can be inherited from the location by checking "Same income eligibility as location" or be entered individually if they differ from the location.

Like the location, there are 4 options:

* Free to everyone.  This should be used when there is generally no charge and everyone is eligible.
* Free to eligible persons/entities.  This should be used when the location generally has income limits.  For example, the location only serves clients with income less than 125% of the federal poverty level.
* Sliding scale based on income.  
* Flat fee regardless of income

When free to eligible persons/entities is selected, the user is then required to set an income limit and apply an income standard.  

.. image:: ../assets/otis-locations-free-income.png

When the user selects sliding scale or flat fee, a description of those fees is required.

.. image:: ../assets/otis-locations-fees.png

Populations
--------------
Services can be limited to one or more populations.  Users self-identify populations on the main Get Legal Help page and referrals will not return any population-restricted service the user does not match and OTIS will prioritize population-specific services over unrestricted services.

.. image:: ../assets/otis-populations.png

.. note::  Populations are managed in the `intake populations taxonomy <https://www.illinoislegalaid.org/admin/structure/taxonomy/manage/intake_populations/overview>`_.  Only ILAO staff can add or edit this taxonomy.
 

Service area
---------------

The service can inherit the service area from the location by checking "Yes" to the "Same service area as location" question.  Or the service can set its own service area. 

.. image:: ../assets/otis-service-service-area.png

For example, a service that serves Kane, Kendall, and DeKalb counties would have the limit to specific area set to Counties and then would list the 3 counties.  If a location serves only part of a county (for example, just the city of Chicago in Cook county, the limit to specific area should be set to Cities and Chicago should be listed).

.. note:: 
   It is not possible to limit a service to a mix of counties, cities, and zip codes.  In those scenarios, multiple services should be created with different service areas.


Direct Representation
=======================

Services designated as the type "Direct representation," have additional fields.  

* Whether the service is a hotline
* Whether the service is an advice desk or walk-in clinic
* Level of service provided.  This is a multi-select and includes options for extended representation, brief services, advice, mediation/ADR, and pro bono placement.
* How the service is delivered (in person, phone, or online/remote)




