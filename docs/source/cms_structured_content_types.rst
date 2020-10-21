=================================
Structured Content Types
=================================

Content Types
===============

Legal Problem
----------------
The primary content type for structured content is the Legal Problem.  

+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Title (name)    | Title field       | 1; required    | Name of the legal problem   |
+-----------------+-------------------+----------------+-----------------------------+
| Description     | Text area (plain) | 1; required    | Description of the problem  |
+-----------------+-------------------+----------------+-----------------------------+
| Disambiguation  | Text area (plain) | 1              | A short description of the  |
| Description     |                   |                | item used to disambiguate   |
|                 |                   |                | from other, similar items   |
+-----------------+-------------------+----------------+-----------------------------+
| Identifier      | Hidden            |                | Node UUID                   |
+-----------------+-------------------+----------------+-----------------------------+
| Stage           | Text field        | 1              | The stage of the legal      |
|                 |                   |                | problem, if applicable. For |
|                 |                   |                | example, pre-filing, post-  |
|                 |                   |                | filing/pre-trial, trial, etc|
+-----------------+-------------------+----------------+-----------------------------+
| Subtype         | Term reference    | unlimited      | A more specific type of the |
|                 | to Legal Problem  |                | legal problem. For example, |
|                 | Subtypes          |                | 'being evicted from public  |
|                 |                   |                | housing' under the problem  |
|                 |                   |                | "being evicted"             |
+-----------------+-------------------+----------------+-----------------------------+
| LegalCode       | Paragraphs: Legal | unlimited      | Legal code from standard    |
|                 |                   |                | coding systems              |
+-----------------+-------------------+----------------+-----------------------------+
| LifeAreaAffected| Term reference    | unlimited      | The area of a person's life |
|                 | to Life Areas     |                | that is affected by the     |
|                 |                   |                | legal problem.              |
+-----------------+-------------------+----------------+-----------------------------+
|Possible solution| Entity reference  | unlimited      | Entity reference to Legal   |
|                 |                   |                | Solution nodes              |
+-----------------+-------------------+----------------+-----------------------------+ 
| Primary         | Entity reference  | 1              | Entity reference to legal   |
| prevention      |                   |                | solution nodes              |
+-----------------+-------------------+----------------+-----------------------------+ 
| Secondary       | Entity reference  | 1              | Entity reference to legal   |
| prevention      |                   |                | solution nodes              |
+-----------------+-------------------+----------------+-----------------------------+ 
| FAQ             | Entity reference  | unlimited      | Entity reference to         |
|                 |                   |                | Legal Question              |
+-----------------+-------------------+----------------+-----------------------------+ 
| RelatedResources| Entity reference  | unlimited      | Entity reference to legal   |
|                 |                   |                | content types               |
+-----------------+-------------------+----------------+-----------------------------+ 
| Image           | Image             | 1              | Image to associate with node|
+-----------------+-------------------+----------------+-----------------------------+ 
| Language        | Hidden            | 1              | Language of the node        |
+-----------------+-------------------+----------------+-----------------------------+ 
| url             | Hidden            | 1              | Website url for the node    |
+-----------------+-------------------+----------------+-----------------------------+

.. note:: 
   
   The related resources will automatically pull the name, last modified (last internal revision date), last reviewed (last expert review date), url, and content format as additionalType in exporting the schema.

Legal Solution
----------------

+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Title (body)    | Title field       | 1              | Question title              |
+-----------------+-------------------+----------------+-----------------------------+
| Alternate name  | Text field        | 1              | An alternative name for the |
|                 |                   |                | solution                    |
+-----------------+-------------------+----------------+-----------------------------+
| Description     | Text area         | 1              |                             |
+-----------------+-------------------+----------------+-----------------------------+
| Disambiguation  | Text area (plain) | 1              | A short description of the  |
| Description     |                   |                | item used to disambiguate   |
|                 |                   |                | from other, similar items   |
+-----------------+-------------------+----------------+-----------------------------+
| Identifier      | Hidden            | 1              | Node UUID                   |
+-----------------+-------------------+----------------+-----------------------------+
| url             | Hidden            | 1              | Website url for the node    |
+-----------------+-------------------+----------------+-----------------------------+
| solution type   | Term reference    | 1              | Reference to solution types |
+-----------------+-------------------+----------------+-----------------------------+
| legal forms     | Entity reference  | unlimited      | Reference to legal forms    |
| needed          |                   |                |                             |
+-----------------+-------------------+----------------+-----------------------------+
| information     | Text field        | unlimited      |                             |
| needed          |                   |                |                             |
+-----------------+-------------------+----------------+-----------------------------+
| legalDifficulty | Text area         | 1              | Explanation of the legal    |
|                 |                   |                | difficulty involved         |
+-----------------+-------------------+----------------+-----------------------------+
| estimated time  | Duration          | 1              |                             |
| required        |                   |                |                             |
+-----------------+-------------------+----------------+-----------------------------+
| eligibilityRules| Paragraphs        | unlimited      | Text blocks                 |
+-----------------+-------------------+----------------+-----------------------------+
| jurisdiction    | Paragraphs        | unlimited      | Coverage area paragraphs    |
+-----------------+-------------------+----------------+-----------------------------+
| helpful         | TBD               | unlimited      | Helpful organizations to    |
| organizations   |                   |                | refer persons to            |
+-----------------+-------------------+----------------+-----------------------------+
| howTos          | Entity reference  | unlimited      | Reference to a legal how to |
+-----------------+-------------------+----------------+-----------------------------+
| result          | Paragraphs        | one            | Text blocks                 |
+-----------------+-------------------+----------------+-----------------------------+ 


Legal Question
----------------

Single question; packaged within an FAQ in a legal problem.  

+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Title (body)    | Title field       | 1              | Question title              |
+-----------------+-------------------+----------------+-----------------------------+
| Accepted Answer | Paragraphs        | 1              | Text block paragraphs       |
+-----------------+-------------------+----------------+-----------------------------+
| Suggested       | Paragraphs        | unlimited      | Text block paragraphs       |
| Answer          |                   |                |                             |
+-----------------+-------------------+----------------+-----------------------------+

Legal Forms
---------------
+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Title (formName)| Title field       | 1              | Form title                  |
+-----------------+-------------------+----------------+-----------------------------+
| FilledOutWith   | Paragraphs        | unlimited      | FormPrep Program paragraphs |
+-----------------+-------------------+----------------+-----------------------------+
| formUse         | Text area         | 1              | Explanation of how/when the |
|                 |                   |                | form is used                |
+-----------------+-------------------+----------------+-----------------------------+



Legal How-to
---------------
+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Title (Name)    | Title field       | 1, required    | Title                       |
+-----------------+-------------------+----------------+-----------------------------+
| Description     | Text area         | 1, required    | Description of the how-to   |
+-----------------+-------------------+----------------+-----------------------------+
| prepTime        | duration          | 1, required    |                             |
+-----------------+-------------------+----------------+-----------------------------+
| performTime     | duration          | 1, required    |                             |
+-----------------+-------------------+----------------+-----------------------------+
| totalTime       | duration          | 1, required    | Prep time + perform time    |
+-----------------+-------------------+----------------+-----------------------------+
| stepSections    | paragraphs bundle | unlimited      | Reference to step sections  |
+-----------------+-------------------+----------------+-----------------------------+
| supply          | text field        | unlimited      | Things needed to complete   |
|                 |                   |                | the how-to                  |
+-----------------+-------------------+----------------+-----------------------------+
| tool            | text field        | unlimited      | Tools needed to complete the|
|                 |                   |                | how to                      |
+-----------------+-------------------+----------------+-----------------------------+
| yield           | text field        | one            | The quantity that results by|
|                 |                   |                | performing instructions     |
+-----------------+-------------------+----------------+-----------------------------+



Legal Steps
-------------
+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Title (Name)    | Title field       | 1, required    |                             |
+-----------------+-------------------+----------------+-----------------------------+
| Directions      | paragraphs bundle | unlimited      | Directions bundle           |
+-----------------+-------------------+----------------+-----------------------------+
| Tips            | paragraphs bundle | unlimited      | Tips bundle                 | 
+-----------------+-------------------+----------------+-----------------------------+

.. note:: There is also a position property in the legal steps in the schema.  This is computed in the step sections paragraph bundle in the How-to and not stored directly in the steps.  This will allow for step re-use.


Legal Organization
---------------------
.. note::
   ILAO already has organization profile data that should be used for any organization in our system.  New entities should only be added to reference organizations that are not legal services providers within our Organization platform.
   
   Fields will be hidden when an Organization is included.

+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Title (Name)    | Title field       | 1, required    |                             |
+-----------------+-------------------+----------------+-----------------------------+
| Organization    | Entity reference  | 1              | Reference to an existing    |
|                 |                   |                | organization                |
+-----------------+-------------------+----------------+-----------------------------+
| Description     | Text area         | 1              |                             |
+-----------------+-------------------+----------------+-----------------------------+
| Address         | Address           | 1              |                             |
+-----------------+-------------------+----------------+-----------------------------+
| Area Served     | Paragraphs bundle | unlimited      | Coverage area               |
+-----------------+-------------------+----------------+-----------------------------+
| Email           | Email             | 1              |                             |
+-----------------+-------------------+----------------+-----------------------------+
| Telephone       | Text field        | 1              |                             |
+-----------------+-------------------+----------------+-----------------------------+
| Contact         | Paragraphs bundle | one            |                             |
+-----------------+-------------------+----------------+-----------------------------+

Paragraph Bundles
===================

There are a number of paragraphs bundle created to support the content entities in the schema:

* LegalCode, used in LegalProblem
* FormPrepProgram, used in LegalForms
* Step section, a holder for steps in Legal How-to
* How to tips, used in Legal Steps
* How to directions, used in Legal Steps
* CoverageArea, used in Legal Solution, Organization
* TextBlock, used in various text output where we need more control over structure.
* Contact point

Legal Code
------------
+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Code value      | Text field        | 1              |                             |
+-----------------+-------------------+----------------+-----------------------------+
| Coding system   | Text field        | 1              |                             |
+-----------------+-------------------+----------------+-----------------------------+

Form Prep Program
--------------------

+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| name            | text  field       | 1              | Name of the form prep       |
|                 |                   |                | package or Easy Form        |                
+-----------------+-------------------+----------------+-----------------------------+
| url             | link              | 1              | link to the form prep       |
+-----------------+-------------------+----------------+-----------------------------+
| formPrepProgram | term reference    | 1              | Reference to the form prep  |
|                 |                   |                | programs taxonomy           |
+-----------------+-------------------+----------------+-----------------------------+

Legal Step Sections
----------------------
+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Title (Name)    | Title field       | 1, required    | Required by Drupal only     |
+-----------------+-------------------+----------------+-----------------------------+
| Include title?  | Boolean           | 1, required    | Include title in API feed?  |
+-----------------+-------------------+----------------+-----------------------------+
| Steps           | Entity reference  | unlimited      | Reference to legal steps    |
+-----------------+-------------------+----------------+-----------------------------+

.. note:: There is also a position property in the steps section in the schema.  This is computed in the How To and not stored directly in the steps. 

How To Tips
---------------

+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Tip with markup | Text area         | 1, required    | WYISIWYG text               |
+-----------------+-------------------+----------------+-----------------------------+
| Tip             | Hidden            | 1, required    | Clean version of tip        |
+-----------------+-------------------+----------------+-----------------------------+
| referencedUrls  | Links             | unlimited      | Links included in markup    |
+-----------------+-------------------+----------------+-----------------------------+

.. note:: There is also a position property in the schema.  This is computed in the How-to and not stored in the database.

How To  Directions
---------------------

+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Direction       | Text area         | 1, required    | WYISIWYG text               |
| with markup     |                   |                |                             |
+-----------------+-------------------+----------------+-----------------------------+
| Direction       | Hidden            | 1, required    | Clean version of direction  |
+-----------------+-------------------+----------------+-----------------------------+
| referencedUrls  | Links             | unlimited      | Links included in markup    |
+-----------------+-------------------+----------------+-----------------------------+

.. note:: There is also a position property in the schema.  This is computed in the How-to and not stored in the database.

Text Block
-------------

+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Heading         | Text field        | 1              |                             |
+-----------------+-------------------+----------------+-----------------------------+
| Body            | Hidden            | unlimited,     | Clean version of body with  |
|                 |                   | required       | markup                      |
+-----------------+-------------------+----------------+-----------------------------+
| Body with markup| Text area         | unlimited,     | WYSIWYG                     |
|                 |                   | required       |                             |
+-----------------+-------------------+----------------+-----------------------------+
| List            | Paragraphs bundle | unlimited      | Item list bundle            |
+-----------------+-------------------+----------------+-----------------------------+            

Item List
------------

+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Item List Order | Select            | 1, required    | ascending, descending, or   |
|                 |                   |                | unordered                   |
+-----------------+-------------------+----------------+-----------------------------+
| Item List       | Paragraphs bundle | unlimited,     | Item List element bundle    |
| Elements        |                   | required       |                             |  
+-----------------+-------------------+----------------+-----------------------------+

Item list Elements
----------------------     

+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Item            | Text area         | 1, required    | WYISIWYG text               |
| with markup     |                   |                |                             |
+-----------------+-------------------+----------------+-----------------------------+
| Item            | Hidden            | 1, required    | Clean version of direction  |
+-----------------+-------------------+----------------+-----------------------------+

.. note:: There is also a position property in the schema.  This is computed in the How-to and not stored in the database.  

Coverage Area
----------------

+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Administrative  | Select            | 1, required    | Country, state, city,       |
| area            |                   |                | postal code                 |
+-----------------+-------------------+----------------+-----------------------------+
| Locality        | Term reference    | unlimited      | Region taxonomy             |
+-----------------+-------------------+----------------+-----------------------------+

Contact Point
------------------
+-----------------+-------------------+----------------+-----------------------------+
| Field           | Type              | Cardinality    | Description                 |
+=================+===================+================+=============================+
| Contact type    | Text field        | unlimited      |                             |
+-----------------+-------------------+----------------+-----------------------------+
| Area served     | Paragraphs bundle | unlimited      | Coverage area bundle        |
+-----------------+-------------------+----------------+-----------------------------+
| Email           | Email             | 1              |                             |
+-----------------+-------------------+----------------+-----------------------------+
| Telephone       | Text field        | 1              |                             |
+-----------------+-------------------+----------------+-----------------------------+
| Hours           | Hours field       | unlimited      |                             |
+-----------------+-------------------+----------------+-----------------------------+
| Products        | Text field        | unlimited      | Type of service or product  |
| Supported       |                   |                | offered through the         |
|                 |                   |                | organization.               |
+-----------------+-------------------+----------------+-----------------------------+

Taxonomies
=============

* life areas (used in legal problem)
* solution types (used in legal solutions)
* form prep programs (used in Legal forms)


Technical Notes
===================

* We can use \Drupal\Core\Mail\MailFormatHelper::htmlToText($string) to render plain text with urls as footnotes from the with markup fields. 


.. image:: ../assets/clean-markup.png



