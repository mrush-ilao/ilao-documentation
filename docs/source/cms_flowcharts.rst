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
      C -->|Two| E[fa:fa-car Result two]
      click D "https://www.illinoislegalaid.org" "Home"
    </div>

.. image:: ../assets/cms-flowchart.png

In the above image:
    
    * the flowchart is set to be top to bottom (graph TB)
    * A, B, C, D, E are the ids of the 5 blocks
    * Text within | | are text between pathways, for example One between C & D
    * Both hard edge and round edge use the rectangle, but the round edge class has rounded edges.
    * Result one includes a hyperlink to our website with a tooltip of Home
    * Result two includes the car font-awesome icon.
    


Configuration
===============
Flowcharts must be created using the text format "Diagrams." This ensures that characters are not escaped in a way that breaks the image.

To create a flowchart, use the `flowchart syntax <https://mermaid-js.github.io/mermaid/#/flowchart>`_ documentation. 

Theming
========
ILAO will design a standard visual design for flowcharts. Staff can use other themes as appropriate, or switch to the base theme and set custom theme variables.

See `theming documentation <https://mermaid-js.github.io/mermaid/#/theming>`_.

Icon support
=============

Mermaid supports the use of basic `font-awesome <https://fontawesome.com/icons?d=gallery>`_ icons.  While ILAO has a pro account, only the basic class is currently supported. 

.. todo:: determine if ILAO just needs to add support for fal/fas clases in font awesome to support the additional icon set.

Content format
================
Pages with a flowchart should be set to a content format of Flowchart.  This will cause the flowchart label and icon to display.

Process Server Flowchart
=========================
.. note:: DO NOT EDIT THIS

graph TD
    A[start] --> B(Determine who you need to serve)
    B --> C{A person or business?}
    C --> D[Business]
    C --> E[Person]
    E --> F[\Fill out the summons and complaint form\]
    D --> a1
    subgraph one [Who to serve]
    a1>"Summons has to be served to a <br />Registered Legal Agent of the Business<br /> through any of the service methods below"]---a2
    a2["Go to the Secretary of State website to search for the Registered Agent of the Corporation or LLC you wish to serve a summons on"]-->a3
    a3["
Once on the site, click #quot;Search#quot;, select #quot;Corporation and LLC#quot;, click #quot;Submit#quot;, and finally enter the name or keywords you are looking for"]-->a4
    a4["Select the corporation or LLC and scroll down to find the contact info for the Registered Agent that you must serve the summons to"]-->a5
    a5>"
If the business is not incorporated, then put the name of the owner and put them as D/B/A (doing business as) and then the name of the business"]
    a5-->F
    end
    F-->G
    G["File complaint and summons form with the local county circuit court in person or online with e-filing"]-->H
    H>Now you have to make sure that the defendant is served.]-->I{"How will you serve?"}
    I --> |Most common| J[Sheriff] -->b1
    I --> K[Professional process server or an adult not part of the case]-->c1
    subgraph two [Having the sheriff service]
    b1[Staple Summons on top of copy of complaint being served] --> b2
    b2[Ask the sheriff of the county in person or via mail where the summons will be served where the party you want to serve lives]-->b3
    b3>There will be a fee unless you have a fee waiver]-->b4{Does the defendant <br />live in the same county where the lawsuit was filed}
    b4-->|No| b5["Call the sheriff of the county of the party being sued lives in to get the sheriff's contact info"]-->b6
    b4-->|Yes| b6{"How are you going to take it to the sheriff?"}
    b6-->|In person|b7["test"]
    b6-->|Mail|b8["text"]
    end
    subgraph Professional process server[three]
    c1-->c2
    end
