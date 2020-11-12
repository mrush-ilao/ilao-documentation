==============================================
Natural language processing of legal problem
==============================================

The current website uses an autocomplete to our legal issues taxonomy to direct a user to the appropriate triage rules or referrals.  The accuracy of this is dependent on how the user interacts with the field:

* Users can pick a term from the autocomplete.  If they do:

  * and it is the lowest level term in the taxonomy, they are matched to the triage rules
  * and it is not the lowest level term in the taxonomy, they are taken to a screen to filter through the taxonomy to the lowest level, starting with the term they entered.
  
* Users can type text into the autocomplete.  If they do:

  * and it is an exact match to a term in the taxonomy, then it is treated as if the user selected the term from the autocomplete
  * and it is not an exact match to a term in the taxonomy, the user is taken to the top of our legal issues taxonomy to filter down to the lowest level problem.
  
The classifiers will be used to improve that last use case, where the user doesn't match to anything in the taxonomy, to at least get the user into a more discrete top level category than the full list of top categories.

Processor Algorithm
=====================

If the user's input is an exact match to the legal issues taxonomy => no change in the current system is made

If the user's input is not an exact match to the legal issues taxonomy:

* User input is passed to both Houston.ai and Spot classifier
* A combined list of results are culled together, ranked and mapped back to ILAO's IA
* The user is presented with a short list of options based on the classifier data.

.. todo:: Figure out how to map all these taxonomies to a single index.  We have our IA, a LSC code to our IA.  Nothing that maps our IA to NSMI 
  
    