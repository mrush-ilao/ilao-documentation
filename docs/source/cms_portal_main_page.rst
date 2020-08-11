==============================
Portal main page content type
==============================

.. note:: The 2020 migration resulted in a new portal template.  As a result, there are fields that are no longer used, such as the hero image. At some point in the future, the deprecated fields will be removed.



Portal page types
==================
Despite the content type name of "portal main page", there are three types of portal pages:

* Main page
* Subpages
* Toolbox selector form (deprecated I think)

A portal should have no more than 1 main page and may have an unlimited number of subpages.

Fields
========

Every portal page requires:

* A title
* A subdomain.  For main pages, this is the url that the the website is accessed at.  While the field is called subdomain, it is no longer an actual subdomain.  Instead, it becomes https://www.illinoislegalaid.org/[node:subdomain].  For sub pages and toolbox selector form, this binds the pages together and results in a url of https://www.illinoislegalaid.org/[node:subdomain]/[node:title]
* A page type
* A meta description.  This is used in socia media and SEO.
* A content description.  This is used in listing pages and search results pages
* Hero title and subtitle are required but not used.
* Primary legal category and legal issues; this is used throughout the site to aid in navigation, filtering, and reporting
* One or more paragraphs (components)
* An image.  This is used for social media sharing
* An hero image.  This is no longer used but is still required.

.. todo::  Remove hero title, subtitle and image.

Components
============
The supported components within a portal are:

* Portal layout webform
* Portal layout grid
* Portal layout summary
* Portal layout timeline
* Portal layout sidebar
* Portal layout split column layout
* Portal layout structured content


Navigation
===========

The main portal page should be linked to in the Quick Links in the footer.  

.. todo:: We will add portal main page where the page type is main page to the legal resources pages to improve findability.  