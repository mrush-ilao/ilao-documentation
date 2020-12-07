===========================
Structured content API
===========================


List of API calls
====================

* taxonomy terms
* list of legal problems
* specific legal problem
* list of solutions
* specific solution
* list of questions
* specific questions in a specific FAQ
* specific question
* list of how-tos
* specific how-to from a specific solution
* eligibility rules from a specific solution
* information needed from a specific solution
* forms needed from a specific solution
* result for a specific solution


Taxonomy terms
=========================
Returns the list of taxonomy terms from ILAO's structured content:

* life areas
* solution types
* form prep programs

Function call
---------------

Method: GET

 
Sample Output
----------------

.. code-block:: json

   [{
   "name":"White"},
   {"name":"Black"},
   {"name":"Red"},
   {"name":"Green"},
   {"name":"Blue"},
   {"name":"Orange"}]


Get list of legal problems
============================

Returns a list of legal problem content from the website.  This is a simple list of:

* name
* description
* identifier
* language

Function call
----------------

Method: GET


Sample Output
---------------

.. code-block:: json

    [{
 		"name": "Being a victim of domestic violence",
 		"description": "Legal problem of being a victim of DV",
 		"identifier": "a6a6eb74-38c3-11eb-adc1-0242ac120002",
 		"language": "en"

 	},
 	{
 		"name": "Being evicted",
 		"description": "Legal problem of being evicted",
 		"identifier": "a6a6eb74-38c3-11eb-adc1-0242ac120002",
 		"language": "en"
 	}
 ]
 
Parameters
--------------------
* lifeAreaAffected (optional)
* legal code (array of code values and coding system); NSMI and LSC problem codes are supported (optional)
* language based on the 2 character ISO language codes (optional)


Get specific problem 
========================
Returns a specific legal problem package.  This includes the full content:  problem, solutions, etc.

Parameters
-------------

* exactly one identifier

Sample Output
----------------

See the order of protection JSON file.

Get list of questions
Get list of how-tos
Get list of steps

Get list of solutions
======================

Returns a list of solutions along with nested information on the problem(s) the solution solves.

Function call
---------------

Method: GET


Sample Output
----------------

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
---------------

* problem_identifier:  the identifier of the legal problem the solution is attached to; will return all solutions if this is omitted
* solution type 

Get solution
===============
Returns the entire schema for a specific solution.  While solutions exist within problems, it is sometimes helpful to pull in just the solution segment.

Function call
----------------

Method: GET

Get list of questions
=======================

Returns list of questions from the legal question content type.


Function call
---------------

Method: GET


Sample Output
----------------

.. code-block:: json

   [{
	"questions": [{
			"name": "How long does an Order of Protection last?",
			"identifier": "b06e8c24-38ab-11eb-adc1-0242ac120002",
			"language": "en"
		},
		{
			"name": "What if my abuser lives with me?",
			"identifier": "b06e8c24-38ab-11eb-adc1-0242ac120002",
			"language": "en"
		},
		{
			"name": "What if I have pets?",
			"identifier": "b06e8c24-38ab-11eb-adc1-0242ac120002",
			"language": "en"
		}

	]
  }]
  

Parameters
---------------

Get FAQ
============
Returns set of questions with answers from a specific problem 

Function call
---------------

Method: GET


Sample Output
----------------

.. code-block:: json

	[{
	"questions": [{
			"name": "How long does an Order of Protection last?",
			"acceptedAnswer": {
				"body": ["If you live with your abuser, you can ask for exclusive possession of the home. The abuser will have to leave and stay away from the home. If the abuser has a legal right to be in the home, the judge will need to decide whether it is more difficult for you or the abuser to leave.",
					"The judge may ask if you have another place to stay, your abuser has another place to stay, any children live with you, both of you work, or if your home is near your workplace or your children's school. ",
					"If the judge orders exclusive possession, call the police and ask that they escort you home. Tell the police officer that you have an Order of Protection and need the respondent removed from your home. The police will meet you at your home and tell the abuser they have to leave.",
					"The court can order that you or the abuser be able to go into the house without the police to get clothing, medicine, or other items you need."
				]
			},
			"identifier": "b06e8c24-38ab-11eb-adc1-0242ac120002",
			"language": "en"
		},
		{
			"name": "What if my abuser lives with me?",
			"acceptedAnswer": {
				"body": ["If you live with your abuser, you can ask for exclusive possession of the home. The abuser will have to leave and stay away from the home. If the abuser has a legal right to be in the home, the judge will need to decide whether it is more difficult for you or the abuser to leave.",
					"The judge may ask if you have another place to stay, your abuser has another place to stay, any children live with you, both of you work, or if your home is near your workplace or your children's school. ",
					"If the judge orders exclusive possession, call the police and ask that they escort you home. Tell the police officer that you have an Order of Protection and need the respondent removed from your home. The police will meet you at your home and tell the abuser they have to leave.",
					"The court can order that you or the abuser be able to go into the house without the police to get clothing, medicine, or other items you need."
				]
			},
			"identifier": "b06e8c24-38ab-11eb-adc1-0242ac120002",
			"language": "en"
		},
		{
			"name": "What if I have pets?",
			"identifier": "b06e8c24-38ab-11eb-adc1-0242ac120002",
			"language": "en"
		}
	]
    }]		


Parameters
----------------

* problem_identifier = the identifier for the specific problem.  Required and limited to 1.

Get question
===============
Returns a specific question

Function call
----------------

Sample Output
---------------

.. code-block:: json

   [{
	"question": [{
			"name": "How long does an Order of Protection last?",
			"acceptedAnswer": {
				"body": ["If you live with your abuser, you can ask for exclusive possession of the home. The abuser will have to leave and stay away from the home. If the abuser has a legal right to be in the home, the judge will need to decide whether it is more difficult for you or the abuser to leave.",
					"The judge may ask if you have another place to stay, your abuser has another place to stay, any children live with you, both of you work, or if your home is near your workplace or your children's school. ",
					"If the judge orders exclusive possession, call the police and ask that they escort you home. Tell the police officer that you have an Order of Protection and need the respondent removed from your home. The police will meet you at your home and tell the abuser they have to leave.",
					"The court can order that you or the abuser be able to go into the house without the police to get clothing, medicine, or other items you need."
				]
			},
			"identifier": "b06e8c24-38ab-11eb-adc1-0242ac120002",
			"language": "en"
		}

	]
  }]
  
Parameters
-------------

* question_identifier:  uuid of the question to return.    





Get eligibility rules
=======================

Returns the eligibility rules for a specific legal solution.  

Function call
---------------

Sample Output
-----------------

.. code-block:: json

   [{
 		"body": [
 			"One of the following must be true:"
 		],
 		"list": [{
 			"itemListOrder": "Ascending",
 			"itemListElements": [{
 					"item": "Petitioner lives in Illinois",
 					"position": 1
 				},
 				{
 					"item": "Abuse happened in Illinois, or",
 					"position": 2
 				},
 				{
 					"item": "Petitioner is staying in Illinois to avoid abuse",
 					"position": 3
 				}
 			]
 		}]
 	},
 	{
 		"body": [
 			"There must have been abuse by the Respondent. Abuse includes physical abuse, harassment, intimidation of a dependent, interference with personal liberty, and willful deprivation."
 		]
 	},
 ]

Parameters
-------------
* solution_identifier:  uuid of the solution.

Get information needed
========================

Returns the eligibility rules for a specific legal solution.  

Function call
---------------

Sample Output
-----------------
.. code-block:: json
  
 [
 	"Petitioner's address",
 	"Petitioner's alternate address for safety (optional)",
 	"Respondent's address",
 	"Physical description of Respondent",
 	"Respondent's employer",
 	"Details about any other Orders of Protection or other court cases involving the Petitioner or the Respondent.",
 	"Details about the abuse and when it took place.",
 	"Details about personal property that Petitioner wants back."
 ]

Parameters
-------------
* solution_identifier:  uuid of the solution.

Get legal forms needed
=======================

Returns the list of legal forms needed from a specific solution

Function call
---------------

Sample Output
-----------------

.. code-block:: json

   [{
		"formName": "Petition for Order of Protection",
		"filledOutWith": [{
				"name": "Order of Protection",
				"url": "https://www.illinoislegalaid.org/legal-information/order-protection",
				"formPrepProgramType": "HotDocs"
			},
			{
				"name": "Petition for Order of Protection",
				"url": "https://www.illinoislegalaid.org/legal-information/order-protection.pdf",
				"formPrepProgramType": "PDF"
			}
		]
	},
	{
		"formName": "Emergency Order of Protection",
		"filledOutWith": [{
			"name": "Order of Protection",
			"url": "https://www.illinoislegalaid.org/legal-information/order-protection",
			"formPrepProgramType": "HotDocs"
		}],
		"formUse": "An EOP is only valid for 14 to 21 days"
	}
  ]

Parameters
-------------
* solution_identifier:  uuid of the solution.

Get list of how-to's
========================

Returns a list of all how-to's

Function call
--------------

Sample output
----------------

.. code-block:: json

   [{
		"name": "Getting an order of protection",
		"description": "An Order of Protection can help protect you or a loved one from abuse. This article explains how to get one",
		"identifier": "9ea16654-38cb-11eb-adc1-0242ac120002",
		"language": "en"
	},
	{
		"name": "Changing or renewing an order of protection",
		"description": "The person who asked for an Order of Protection can ask the judge to change, end, or renew it.",
		"identifier": "9ea16654-38cb-11eb-adc1-0242ac120002",
		"language": "en"
	}
  ]

Parameters
------------
* solution_identifier:  uuid of the solution; when provided will limit the list of how-tos to those tied to a solution.

Get a specific how-to
======================

Returns a specific how-to for a legal solution.  

Function call
----------------

Sample output
---------------

See the order of protection json

Parameters
-------------
* howto_identifier:  uuid of the howto.  Required


Get a result from a solution
==============================

Returns the result for a solution.

Function call
--------------

Sample output
----------------

.. code-block:: json

   [{
		"body": [
			"When a judge signs an Order of Protection, it makes it illegal for the Respondent to do or not do certain things.  A judge may require the Respondent to:"
		],
		"list": [{
			"itemListOrder": "Unordered",
			"itemListElements": [{
					"item": "Stop abusive acts,"
				},
				{
					"item": "Stay away from the victim and other people protected by the order,"
				},
				{
					"item": "Not contact the victim via telephone calls, mail, email, written notes, or third parties,"
				},
				{
					"item": "Stay away from the victim's home, school, or work,"
				}
			]
		}]
	}
   ]


Parameters
------------
* solution_identifier:  uuid of the solution; required.

