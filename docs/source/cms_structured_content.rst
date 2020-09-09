==========================
Structured Content Schema
==========================


A legal problem is the primary entity and has within it faqs and solutions.  A solution may have processes (how-to) included.

Legal Problem
===============
A legal problem has:

* one or more possible solutions
* possible preventions
* faqs associated with the problems, built on the faq schema

.. code-block:: xml

   <?xml version="1.0" encoding="UTF-8" ?>
   <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:include schemaLocation="https://schema.org/Question"/>
     <xs:sequence>
       <xs:element name="lifeAreaAffected" type="lifeAreas" minOccurs="1" maxOccurs="unbounded"/>
       <xs:element name="cause" type="legalCause"/>
       <xs:element name="possibleSolution" type="legalSolution" minOccurs="1" maxOccurs="unbounded" />
       <xs:element name="primaryPrevention" type="legalSolution" minOccurs="0" />
       <xs:element name="secondaryPrevention" type="legalSolution" minOccurs="0" />
       <xs:element name="stage" type="xs:string" minOccurs="1" maxOccurs="unbounded" />
       <xs:element name="subType" type="xs:string" minOccurs="1" maxOccurs="unbounded" />
       <xs:element name="legalCode" type="legalCode" minOccurs="1" maxOccurs="1" />
       <xs:element name="questions" type="FAQPage" minOccurs="0" maxOccurs="unbounded" />
      </xs:sequence>
   </xs:schema>  
  
.. code-block:: xml

   <?xml version="1.0" encoding="UTF-8" ?>
   <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
     <xs:complexType name="legalCause">
       <xs:element name="causeOf" type="xs:string" />
     </xs:complexType>
     <xs:simpleType name="lifeAreas">
     <xs:restriction base="xs:string">
         <xs:enumeration value="Housing" />
         <xs:enumeration value="Income" />
         <xs:enumeration value="Family" />
         <xs:enumeration value="Immigration status" />
         <xs:enumeration value="Driving privileges" />
         <xs:enumeration value="Ability to work" />
         <xs:enumeration value="Last wishes" />
         <xs:enumeration value="Freedom to move" />
         <xs:enumeration value="Creditworthiness" />
         <xs:enumeration value="Consumer rights" />
         <xs:enumeration value="Health" />
       </xs:restriction>
     </xs:simpleType>
     <xs:complexType name="legalCode">
       <xs:sequence>
         <xs:element name="codeValue" type="xs:string" />
         <xs:element name="codingSystem" type="xs:string" />
       </xs:sequence>
     </xs:complexType>
   </xs:schema>       

.. code-block:: xml

   <legalProblem>
     <lifeAreaAffected>
       <lifeAreas>Family</lifeAreas>
     </lifeAreaAffected>
     <cause>
       <causeOf>Unknown</causeOf>
     </cause>
     <possibleSolution>
       <legalSolution>
         <solutionType>Court solution</solutionType>
           <legalFormsNeeded>
              <legalForm>
                 <formName>Petition for Order of Protection</formName>
              </legalForm>
              <legalForm>
                 <formName>Emergency Order of Protection</formName>
              </legalForm>
              <legalForm>
                 <formName>Order of Protection</formName>
              </legalForm>
           </legalFormsNeeded>
           <informationNeeded>none</informationNeeded>
          <estimatedCost />
          <legalDifficulty>Hard</legalDifficulty>
         <jurisdiction>
           <administrativeArea>State</administrativeArea>
           <locality>Illinois</locality>
         </jurisdiction>
       <usedToSolve />
       <eligibilityRules>
         <textBlock>
           <heading>One of the following must be true:</heading>
           <list>
             <listType>ordered</listType>
             <listItem>Petitioner lives in Illinois</listItem>
             <listItem>Abuse happened in Illinois</listItem>
             <listItem>Petitioner is staying in Illinois to avoid abuse</listItem>
          </list>
        <textBlock>
           <body>There must have been abuse by the Respondent. Abuse includes physical abuse, harassment, intimidation of a dependent, interference with personal liberty, and willful deprivation.
           </body>
         </textBlock>    
        </eligibilityRules>  
        <process>
    
        </process>      
       </legalSolution>
     </possibleSolution>
     <stage>Prefiling</stage>
     <subType>Changing an order of protection</subType>
     <subType>Renewing an order of protection</subType>
     <legalCode>
     </legalCode>
     <faq>
       <question>
         <body>What if I have children?</body>
         <acceptedAnswer>
           <answer>
            <textBlock>
               <body>The judge can add children as protected persons on an Order of Protection. This means that they will be protected by the order. The judge may give you temporary physical care and control of your children, temporary parental duties, or both.
               </body>
             </textBlock>
             <textBlock>
             <heading>The court may also limit or deny the abuser's parenting time. The judge may do this if the abuser has done, or is likely to do, any of the following:</heading>
             <list>
               <listType>unordered</listType>
               <listItem>Abuse or cause danger to the children during parenting time,</listItem>
	           <listItem>Use parenting time as a chance to abuse or harass you and your family members,</listItem>
               <listItem>Hide the children or keep them from you, or</listItem>
               <listItem>Act in a way that is not in the best interests of the children.</listItem>

             </list>
             </textBlock>
           </answer>
         </acceptedAnswer>
       </question>  
       <question>
         <body>What if my abuser lives with me?</body>
         <answer>
           <textBlock>
             <body>
             "If you live with your abuser, you can ask for exclusive possession of the home. The abuser will have to leave and stay away from the home. If the abuser has a legal right to be in the home, the judge will need to decide whether it is more difficult for you or the abuser to leave. The judge may ask if you have another place to stay, your abuser has another place to stay, any children live with you, both of you work, or if your home is near your workplace or your children's school. If the judge orders exclusive possession, call the police and ask that they escort you home. Tell the police officer that you have an Order of Protection and need the respondent removed from your home. The police will meet you at your home and tell the abuser they have to leave. The court can order that you or the abuser be able to go into the house without the police to get clothing, medicine, or other items you need
             </body>
           </textBlock>
         </answer>
     </faq>
   </legalProblem>  

Legal Solution
================

A legal solution has:

* an associated problem (legal solution is an entity within a problem)
* one or more legal forms
* one or more steps based on the schema.org HowTo schema

.. code-block:: xml

   <?xml version="1.0" encoding="UTF-8" ?>
   <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:include schemaLocation="https://schema.org/HowTo"/>
     <xs:complexType name="textBlock">
       <xs:sequence>
         <xs:element name="heading" type="xs:string" minOccurs=0 maxOccurs="1">
         <xs:element name="body" type="xs:string" minOccurs=0 maxOccurs="unbounded">
         <xs:element name="list" type="listBlock" minOccurs=0 maxOccurs="unbounded">    
        </xs:sequence>
     </xs:complexType>
     <xs:complexType name="listBlock">
       <xs:sequence>
         <xs:element name="heading" type="xs:string" minOccurs=0 maxOccurs="1">
         <xs:element name="listType" type="listTypes" minOccurs="1">
         <xs:element name="listItem" type="xs:string" minOccurs=0 maxOccurs="unbounded">    
        </xs:sequence>
     </xs:complexType>
     <xs:simpleType name="solutionType">
       <xs:restriction base="xs:string">
         <xs:enumeration value="ordered" />
         <xs:enumeration value="unordered" />
       </xs:restriction>
     </xs:simpleType>
     <xs:sequence>
       <xs:element name="solutionType" type="solutionType" minOccurs="1" maxOccurs="1"/>
       <xs:element name="legalFormsNeeded" type="legalForms" minOccurs="0"/>
       <xs:element name="informationNeeded" type="xs:string" />
       <xs:element name="estimatedCost" type="monetaryAmount" minOccurs="0" />
       <xs:element name="legalDifficulty" type="xs:string" />
       <xs:element name="estimatedTimeToComplete" type="" />
       <xs:element name="jurisdiction" type="jurisdiction"/>
       <xs:element name="usedToSolve" type="legalProblem" />
       <xs:element name="eligibilityRules" type="textBlock" minOccurs="0" maxOccurs="unbounded"/>
       <xs:element name="process" type="HowTo" minOccurs="0" maxOccurs="unbounded"/>
     </xs:sequence>
   </xs:schema>
   

   
.. code-block:: xml

   <?xml version="1.0" encoding="UTF-8" ?>
   <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:simpleType name="solutionType">
     <xs:restriction base="xs:string">
       <xs:enumeration value="Court solution" />
       <xs:enumeration value="Agency solution" />
       <xs:enumeration value="Execution solution" />
       <xs:enumeration value="Communication solution" />
     </xs:restriction>
   </xs:simpleType>
   <xs:complexType name="legalForm">
     <xs:sequence>
       <xs:element name="formName" minOccurs="1" maxOccurs="1"/>
       
     </xs:sequence>
   </xs:complexType>
   <xs:complexType name="monetaryAmount">
     <xs:sequence>
       <xs:element name="currency" minOccurs="1" maxOccurs="1"/>
       <xs:element name="amount" minOccurs="1" maxOccurs="1"/>
     </xs:sequence>
   </xs:complexType>
   <xs:complexType name="jurisdiction">
     <xs:sequence>
       <xs:element name="administrativeArea" minOccurs="1" maxOccurs="1"/>
       <xs:element name="locality" maxOccurs="unbounded"/>
     </xs:sequence>
   </xs:complexType>
    <xs:simpleType name="administrativeArea">
     <xs:restriction base="xs:string">
       <xs:enumeration value="Country" />
       <xs:enumeration value="State" />
       <xs:enumeration value="County" />
       <xs:enumeration value="City" />
       <xs:enumeration value="Postal Code" />
     </xs:restriction>
   </xs:simpleType>
  
   </xs:schema>    
         
.. code-block:: xml

   <legalSolution>
     <solutionType>Court solution</solutionType>
     <legalFormsNeeded>
       <legalForm>
         <formName>Petition for Order of Protection</formName>
       </legalForm>
       <legalForm>
         <formName>Emergency Order of Protection</formName>
       </legalForm>
       <legalForm>
         <formName>Order of Protection</formName>
       </legalForm>
     </legalFormsNeeded>
     <informationNeeded>none</informationNeeded>
     <estimatedCost />
     <legalDifficulty>Hard</legalDifficulty>
     <jurisdiction>
       <administrativeArea>State</administrativeArea>
       <locality>Illinois</locality>
    </jurisdiction>
    <usedToSolve />
    <eligibilityRules>
      <textBlock>
        <heading>One of the following must be true:</heading>
        <list>
          <listType>ordered</listType>
          <listItem>Petitioner lives in Illinois</listItem>
          <listItem>Abuse happened in Illinois</listItem>
          <listItem>Petitioner is staying in Illinois to avoid abuse</listItem>
       </list>
      <textBlock>
         <body>There must have been abuse by the Respondent. Abuse includes physical abuse, harassment, intimidation of a dependent, interference with personal liberty, and willful deprivation.</body>
      </textBlock>    
    </eligibilityRules>  
    <process>
    
    </process>      
   <legalSolution>
   
References from Schema.org 
==========================

Schema.org does not have XML schema; I have adapted the applicable schema types to match and indicate parameters as required.


Question and Answer
--------------------
See: 

* https://schema.org/Answer
* https://schema.org/Question

.. code-block:: xml
   
   <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
     <xs:complexType name="FAQPage">
       <xs:sequence>
         <xs:element name="question" type="Question" minOccurs="1" maxOccurs="unbounded">
       </xs:sequence>
     </xs:complexType>
     <xs:complexType name="Question">
       <xs:sequence>
         <xs:element name="body" type="textBlock" minOccurs="1" maxOccurs="1"/> 
         <xs:element name="acceptedAnswer" type="Answer">
         <xs:element name="suggestedAnswer" type="Answer" minOccurs="0" maxOccurs="unbounded">
       </xs:sequence>
     </xs:complexType>
     <xs:complexType name="Answer">
       <xs:sequence>
         <xs:element name="answer" type="textBlock" maxOccurs="unbounded"/>
         <xs:element name="answerExplanation" type="textBlock" minOccurs="0" maxOccurs="unbounded"/>
       </xs:sequence>
     </xs:complexType>
   </xs:schema>  
   
How To
-------------

See 

* https://schema.org/HowTo
* https://schema.org/HowToStep
* https://schema.org/HowToDirection
* https://en.wikipedia.org/wiki/ISO_8601#Durations

.. code-block:: xml

   <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
     <xs:complexType name="HowTo">
       <xs:sequence>
         <xs:element name="name" type="xs:string"/>
         <xs:element name="description" type="xs:string" />
         <xs:element name="estimatedCost" type="monetaryAmount" minOccurs="0" maxOccurs="unbounded">
         <xs:element name="prepTime>" type="Duration" />
    	 <xs:element name="performTime>" type="Duration" />
    	 <xs:element name="step" type="HowToStep" minOccurs="1" maxOccurs="unbounded"/>
    	 <xs:element name="supply" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>
    	 <xs:element name="tool" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>
    	 <xs:element name="totalTime>" type="Duration" />
    	 <xs:element name="yield" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>	 
       </xs:sequence>
     </xs:complexType>
     <xs:complexType name="HowToStep">
       <xs:sequence>
         <xs:element name="name" type="xs:string" />
         <xs:element name="position" type="xs:integer"/>
         <xs:element name="howToDirection" type="HowToDirection" minOccurs="0" maxOccurs="unbounded" />  
         <xs:element name="howToTip" type="HowToTip" minOccurs="0" maxOccurs="unbounded" />  
       </xs:sequence>
     </xs:complexType>
     <xs:complexType name="HowToDirection">
       <xs:sequence>
         <xs:element name="position" type="xs:integer"/>
         <xs:element name="direction" type="textBlock"/>    
       </xs:sequence>
     </xs:complexType>
     <xs:complexType name="HowToTip">
       <xs:sequence>
         <xs:element name="position" type="xs:integer"/>
         <xs:element name="direction" type="textBlock"/>    
       </xs:sequence>
     </xs:complexType>
    </xs:schema> 
    
     
     
     
   
   
   
   