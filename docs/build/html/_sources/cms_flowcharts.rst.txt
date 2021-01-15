======================
Flowcharts
======================

Working with the flowchart library
====================================


<div class="mermaid">
graph TB
    A[Hard edge] -->|Link text| B(Round edge)
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
</div>
<hr>

Supported shapes:

* Start
* End
* Operation [rectangle]
* Input/Output [parallelogram]
* Subroutine [links to another flowchart]
* Condition [diamond shape]

