==========================
Structured Content Schema
==========================

Legal Problem

.. code-block:: xml

   <?xml version="1.0" encoding="UTF-8" ?>
   <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
     <xs:sequence>
       <xs:element name="lifeAreaAffected" type="xs:string"/>
       <xs:element name="cause" type="legalCause"/>
       <xs:element name="possibleSolution" type="legalSolution" minoccurs="1" maxoccurs="unbounded" />
       <xs:element name="primaryPrevention" type="legalSolution" minoccurs="0" />
       <xs:element name="secondaryPrevention" type="legalSolution" minoccurs="0" />
       <xs:element name="stage" type="xs:string" minoccurs="1" maxoccurs="unbounded" />
       <xs:element name="subType" type="xs:string" minoccurs="1" maxoccurs="unbounded" />
      </xs:sequence>
   </xs:schema>  
  
.. code-block:: xml

   <?xml version="1.0" encoding="UTF-8" ?>
   <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
     <xs:complexType name="legalCause">
     </xs:complexType>
   </xs:schema>       


Legal Solution

.. code-block:: xml

   <?xml version="1.0" encoding="UTF-8" ?>
   <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
     <xs:complexType name="textBlock">
       <xs:sequence>
         <xs:element name="heading" type="xs:string" minoccurs=0 maxoccurs="1">
         <xs:element name="body" type="xs:string" minoccurs=0 maxoccurs="unbounded">
         <xs:element name="list" type="listBlock" minoccurs=0 maxoccurs="unbounded">    
        </xs:sequence>
     </xs:complexType>
     <xs:complexType name="listBlock">
       <xs:sequence>
         <xs:element name="heading" type="xs:string" minoccurs=0 maxoccurs="1">
         <xs:element name="listType" type="listTypes" minoccurs="1">
         <xs:element name="listItem" type="xs:string" minoccurs=0 maxoccurs="unbounded">    
        </xs:sequence>
     </xs:complexType>
     <xs:simpleType name="solutionType">
       <xs:restriction base="xs:string">
         <xs:enumeration value="ordered" />
         <xs:enumeration value="unordered" />
       </xs:restriction>
     </xs:simpleType>
     <xs:sequence>
       <xs:element name="solutionType" type="solutionType" minoccurs="1" maxoccurs="1"/>
       <xs:element name="legalFormsNeeded" type="legalForms" minoccurs="0"/>
       <xs:element name="informationNeeded" type="xs:string" />
       <xs:element name="estimatedCost" type="monetaryAmount" minoccurs="0" />
       <xs:element name="legalDifficulty" type="xs:string" />
       <xs:element name="estimatedTimeToComplete" type="" />
       <xs:element name="jurisdiction" type="jurisdiction"/>
       <xs:element name="usedToSolve" type="legalProblem" />
       <xs:element name="eligibilityRules" type="textBlock" minoccurs="0" maxoccurs="unbounded"/>
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
       <xs:element name="formName" minoccurs="1" maxoccurs="1"/>
       
     </xs:sequence>
   </xs:complexType>
   <xs:complexType name="monetaryAmount">
     <xs:sequence>
       <xs:element name="currency" minoccurs="1" maxoccurs="1"/>
       <xs:element name="amount" minoccurs="1" maxoccurs="1"/>
     </xs:sequence>
   </xs:complexType>
   <xs:complexType name="jurisdiction">
     <xs:sequence>
       <xs:element name="administrativeArea" minoccurs="1" maxoccurs="1"/>
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
   <legalSolution>

More text here
