============================
Design Guide
============================

Button classes
====================

.. note::  Hyperlinks in legal content even when styled with the button class are showing the wrong link color; they should be white for primary and secondary links.  However, tertiary class is the best class for most content situations.

Primary
---------

The primary CTA button is the bright blue button with white text.  It can be added in the WYSIWYG using the class name "cta-primary"

.. code-block:: HTML

  <a href="#" class="cta-primary">Primary CTA</a>

 
Use for:

 * Buttons that serve as the primary call to action for a page.
 * Submit button for forms

Do not use:

 * When there is already a primary call to action.  For example, on the why donate page, the donate button is the primary call to action and Learn more about connector's circle or other ways to give should be secondary buttons.
 * On any legal content that already has a primary button such as Easy Forms, download, link content, toolboxes, tools, tool steps, or blank forms

Secondary
--------------
The secondary CTA button is the dark blue button with white text. It can be added in the WYSIWYG using the class name "cta-secondary"

.. code-block:: HTML

  <a href="#" class="cta-secondary">Secondary CTA</a>
  <a href="#" class="cta-secondary" style="color:white">Secondary CTA in legal content</a>

Use for:

 *  On about pages, for important buttons where the button is not the primary CTA on the page
 * On legal content (other than toolbox, tool, tool step content), for a primary next step in an article such as to call out the next immediate step the user must take (for example, filing an answer or appearance in an article on responding to a lawsuit).  Legal content should never have more than one secondary button within the text.  If there are more than one critical action to highlight (for example, linking to an answer and an appearance separately, use two tertiary buttons).

Do not use:

 * For form submit buttons
 * For cancel buttons
 * For links that are designed to take the user somewhere rather than taking an action.  For example, using a button to send a user to take a user from reading about donating to the donation page is okay but senidng a user from one piece of legal content to another is not since the only action is to read (see tertiary buttons below)

Tertiary
-------------

The tertiary CTA button is white with a border and dark blue text. It can be added in the WYSIWYG using the class name "cta-tertiary"

.. code-block:: HTML

  <a href="#" class="cta-tertiary">Tertiary CTA</a>

Use for:

 * Cancel actions
 * When you absolutely need to use a button to direct a user to another node without an actual action (other than learning more, reading the page, etc) or when you need to call out two actions of similar weight (for example, File divorce with kids and file divorce without kids)


