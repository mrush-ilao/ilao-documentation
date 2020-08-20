=======================
Managing Locations
=======================

Creating a location
=====================
At the bottom of the form is a Parent Organization field.  This is where the organization associated with the location must be set.  When set, this will then confer all of the organizational ownership to the location so that Organization Managers can edit the location.

Contact information
--------------------
* Give the location a title (name).  The name should be descriptive enough that when displayed to users it makes sense.  For example:  Bond County Courthouse, Main Office, Waukegan Office.  
* Indicate whether the address matches the organization address.  For single-location organizations or the main office, this is likely to be Yes.  If it is set to No, the address form will display and be required.
* Indicate whether the phone number is the same as the one in the organization profile.  If it isn't, you'll be required to provide a phone number. 
* Provide additional phone numbers, if they exist for toll-free and tty numbers. 

.. image:: ../assets/otis-location-header.png

Hours of Operations
-----------------------
There are two options to set a location's hours of operations:  regular weekly hours and less frequent hours.  

When a location is open at least 1 day every week, the "Is this location open at least weekly?" should be set to Yes.

The weekly hours form allows one to:

* Set individual hours per day
* Set up to 4 time slots per day; for example:  Monday 8 am - 12pm, 1pm - 5pm

.. image:: ../assets/otis-locations-hours-regular.png

When a location is not open at least once a week, then we have to use the irregular hours form.  This form requires:

* setting a start date for the rule
* setting an end date for the rule
* setting a rule.  The rule can be generated `using this online tool <https://icalendar.org/rrule-tool.html>`_ and then copied and pasted in.

.. image:: ../assets/otis-locations-hours-irregular.png

Holiday
^^^^^^^^^
Holidays should be set for the location and may be overwritten at the service level.  When holidays are set for a location:

* When used in online triage and intake, the holidays will not show up in callback hours options
* When used in referrals, the displayed hours will show the holidays as a closed date.

.. image:  ../assets/otis-locations-holidays.png

Holidays are managed in the `holidays taxonomy <https://www.illinoislegalaid.org/admin/structure/taxonomy/manage/holidays/overview>`_.  Common Illinois and Federal holidays are included in the taxonomy.

.. note:: Custom holidays can be added to the holiday taxonomy to accommodate unusual events where one or more organizations needs to be closed (such as a staff retreat) or for unusual occurrences (such as the every 4-5 years when the day after Thanksgiving is not the 4th Friday).  

Service area
-----------------
The service area consists of at least one question: does the location serve all of Illinois? If the location is less than statewide, then the user is required to set the service area at the county, city, or zip code level.  

.. image:: ../assets/otis-locations-service-area.png

For example, a location that serves Kane, Kendall, and DeKalb counties would have the limit to specific area set to Counties and then would list the 3 counties.  If a location serves only part of a county (for example, just the city of Chicago in Cook county, the limit to specific area should be set to Cities and Chicago should be listed).

.. note:: The service area can be overridden at the service level.  For example, a location may serve 3 counties but have a specialty service that only serves 1 county.



Service costs
-----------------
Every location should indicate what it typically charges users/clients.  There are 4 options:

* Free to everyone.  This should be used when there is generally no charge and everyone is eligible.
* Free to eligible persons/entities.
* Sliding scale based on income
* Flat fee regardless of income

.. image:: ../assets/otis-locations-free-income.png

When free to eligible persons/entities is selected, the user is then required to set an income limit and apply an income standard.  

.. image:: ../assets/otis-locations-fees.png

When the user selects sliding scale or flat fee, a description of those fees is required.

.. note:: These settings can be overwritten at the service level and services can be further restricted to specific populations for the free to eligible persons/entities.

Additional Fields
--------------------

There are a handful of additional fields for locations:

* Volunteer information
* Image
* Attachments.


.. todo:: The volunteer information is no longer used and should be deprecated.

