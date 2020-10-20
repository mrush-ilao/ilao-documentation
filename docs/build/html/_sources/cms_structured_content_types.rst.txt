=================================
Structured content types
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

Legal How-to
---------------

Paragraph Bundles
===================

* LegalCode, used in LegalProblem
* CoverageArea, used in Legal Solution, Organization
* TextBlock, used in various


Taxonomies
=============

* life areas (used in legal problem)
* solution types (used in legal solutions)




