==============================
Content API:  Solutions List
==============================


Returns a list of solutions along with nested information on the problem(s) the solution solves.

Function call
==================

Method: GET


Sample response
=================

.. code-block:: json

    [{
 		"name": "Order of Protection",
 		"description": "An Order of Protection is a court order that helps someone who is being abused. It stops the abuser from further abusing the victim",
 		"identifier": "a6a6eb74-38c3-11eb-adc1-0242ac120002",
 		"language": "en",
 		"solutionType": "Court solution"
 		"solutionFor": [
 		{ 
          "name": "Being a victim of domestic violence",
 	      "description": "Legal problem of being a victim of DV",
 		  "identifier": "https://www.illinoislegalaid.org/legal-problems/dv",
 		  "language": "en"
 		}]
 	}
  ]
  

Parameters
===============
All parameters are optional.

* problem_identifier:  the identifier of the legal problem the solution is attached to; will return all solutions if this is omitted
* solution type: taxonomy term of the type of solution
* coverage area:

   * administrativeArea (one of County, City, Postal code)
   * locality: the value of the administrativeArea to return