======================
Flowcharts
======================

Flowchart library
====================================
ILAO is using the `Mermaid.js <https://mermaid-js.github.io/mermaid/#/>`_ library to build and integrate Flowcharts and other diagrams into the website.

There is a `live editor <https://mermaid-js.github.io/mermaid-live-editor/#>`_ that can be used to build diagrams. 

.. code-block:: html

    <div class="mermaid">
    graph TB
    A[Hard edge] -->|Link text| B(Round edge)
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
    </div>

Configuration
===============
Flowcharts must be created using the text format "Diagrams." This ensures that characters are not escaped in a way that breaks the image.

Icon support
=============

Mermaid supports the use of basic font-awesome icons.  While ILAO has a pro account, only the basic class is currently supported. 

.. todo:: determine if ILAO just needs to add support for fal/fas clases in font awesome to support the additional icon set.


Technical Notes
=================

* Needs a content format added that does not use CKeditor (named diagrams)
* Needs a paragraph type of formatted text long that defaults to the diagrams format
* Should be tagged to a content format of decision tree
* Needs to include the JS:

.. code-block:: html

   <script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
   <script>mermaid.initialize({startOnLoad:true,'securityLevel': 'loose', 'theme':'base'});




