==========================
Supported Integrations
==========================

URL Pre-fill method
===================
This method allows for passing in query parameters in the URL to pre-fill the main Get Legal Help form.  It is designed to allow for easier integration from chatbots and external services into OTIS without the user having to re-enter information.


This method supports up to 4 parameters:

* issue, which is the legal issues taxonomy term ID.  ILAO will provide a list of taxonomy term IDs for interested partners of the lowest-level terms so that users bypass additional screening.
* zipcode, the user's zipcode
* household, the size of the household as a number
* helptype[]

  * up to 3 instances of helptype[] are allowed
  * the accepted values for these are lawyer, content, forms
  
Sample usage
-----------------
In these samples, the request is coming from a 3rd party chatbot.

User is in zip code 60603, legal issue is  enforcing a joint parenting plan or agreement 
(514616) and the household size is 3.  

`https://www.illinoislegalaid.org/get-legal-help?issue=514616&zipcode=60603&household=3&helptype[]=lawyer <https://www.illinoislegalaid.org/get-legal-help?issue=514616&zipcode=60603&household=3&helptype[]=lawyer>`_
`https://www.illinoislegalaid.org/get-legal-help?issue=514616&zipcode=60603&household=3&helptype[]=lawyer&helptype[]=content <https://www.illinoislegalaid.org/get-legal-help?issue=514616&zipcode=60603&household=3&helptype[]=lawyer&helptype[]=content>`_

.. image::  ../assets/otis-prefill-mobile.png

