==================================================
Content API: Legal Solution Helpful Organization
==================================================


Returns a specific helpful organization

Function call
================

Method: GET

Sample response
=================

.. code-block:: json

  [{
		"name": "Illinois Domestic Violence Helpline",
		"identifier": "e862348a-3a3d-11eb-adc1-0242ac120002",
		"description": "A hotline open 24/7 for people in Illinois who need help with domestic violence.",
		"contact": {
			"contactType": [
				"phone"
			],
			"telephone": "(877) 863-6338"
		},
		"areaServed": [{
				"administrativeArea": "County",
				"locality": [
					"Kane", "Lake", "Will"
				]
			},
			{
				"administrativeArea": "Postal code",
				"locality": [
					"60505", "60506"
				]
			}

		]
	}]

Parameters
=============
* identifier: uuid of the organization; required
