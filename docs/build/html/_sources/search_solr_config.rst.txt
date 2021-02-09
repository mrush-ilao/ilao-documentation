====================
Configuration
====================

.. note::  Staff users do not have access to search configuration.  Please let Gwen know if you see issues.

Known bugs
==============

* Non-node pages do not appear to be indexed.

Search Contents
============================

Our search index includes
---------------------------

* Content of types:

  * ADRM (Lawyer Manuals)
  * Events
  * Job postings
  * Legal content
  * Basic pages
  * Portal content
  * Toolboxes
  * Toolbox tool
  
* Files
* Paragraph bundles used in included content types.

What is not included in search
----------------------------------

The following are not included in our search index:

* All other content types, including organizations, locations, services.
* Comments 
* Custom blocks 
* Custom tokens (these are not indexed because they are included within the rendered legal content)



Processors Used
==================

Before indexing
---------------------

* Index hierarchy - this indexes the hierarchy of taxonomy terms included in content.  
* HTML filter - this strips HTML tags and decodes HTML entities
* Stopwords - this strips out common words from the text of the content to be indexed. ILAO can manage the terms in the list.
* Type specific boosting - this adds a boost factor to some content.

.. note::  List of stopwords:  a, about, above, after, again, against, all, am, an, and, any, are, as, at, be, because, been, before, being, below, between, both, but, by, can, did, do, does, doing, don, down, during, each, few, for, from, further, get, had, has, have, having, he, help, her, here, hers, herself, him, himself, his, how, i, if, in, into, is, it, its, itself, just, legal, me, more, most, my, myself, need, no, nor, not, now, of, off, on, once, only, or, other, our, ours, ourselves, out, over, own, s, same, she, should, so, some, such, t, than, that, the, their, theirs, them, themselves, then, there, these, they, this, those, through, to, too, under, until, up, very, was, we, were, what, when, where, which, while, who, whom, why, will, with, you, your, yours, yourself, yourselves 


Type specific boosting
^^^^^^^^^^^^^^^^^^^^^^^

We lower the boost for events and job postings to make them less relevant compared to legal information and basic pages.

When searching
-----------------

We apply the following:

* HTML filter to strip HTML from search queries
* Stopwords to remove stopwords from query
* Highlight to highlight the search term in the results.

 

..  todo:: Should we make use of any of the other available processors?

