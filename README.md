Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.4

# OntoBPR: An ontological workflow for building permit review

## Metadata
* **IRI**
  * `https://w3id.org/ontobpr`
* **Creators(s)**
  * [Dr. Judith Fauth](https://orcid.org/0000-0002-9078-8393)
    [[ORCID]](https://orcid.org/0000-0002-9078-8393)
    (<jf805@cam.ac.uk></a>) of [University of Cambridge, GB](https://www.linkedin.com/in/judith-fauth-5b5137bb)
  * [Dr. Philipp Hagedorn](https://orcid.org/0000-0002-6249-243X)
    [[ORCID]](https://orcid.org/0000-0002-6249-243X)
    (<philipp.hagedorn-n6v@rub.de></a>) of [Ruhr University Bochum, DE](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/philipp_hagedorn.html.en)
  * [Sebastian Seiss](https://orcid.org/0000-0001-5808-695X)
    [[ORCID]](https://orcid.org/0000-0001-5808-695X)
    (<sebastian.seiss@uni-weimar.de></a>) of [Bauhaus-Universitaet Weimar, DE](https://www.uni-weimar.de/de/bau-und-umwelt/professuren/baubetrieb-und-bauverfahren/personen/sebastian-seiss-msc/)
  * [Sven Zentgraf](https://orcid.org/0000-0001-6058-7614)
    [[ORCID]](https://orcid.org/0000-0001-6058-7614)
    (<sven.zentgraf@rub.de></a>) of [Ruhr University Bochum, DE](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/sven_zentgraf.html.en)
* **Ontology RDF**
  * RDF ([ontobpr.ttl](turtle))
### Description
<p>To avoid a digital disruption in planning buildings and structures, this research presents a workflow in which building codes are represented as machine-readable knowledge graphs and ontologies as an integration to the building permit review procedure and the participation process. Therefore, the building permit process was analyzed, and possible applications of ontology-based knowledge representations are explored. An ontology-based building permit review (OntoBPR) is proposed, reusing two existing ontologies for modeling the permit review workflow for representing the building codes. The OntoBPR ontology extends the approach with a connection to Information Containers for linked Document Delivery (ICDD) that are used for submitting the building application, and the Shapes Constraint Language (SHACL) of which rules are generated from the building code knowledge graphs.</p>

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Datatype Properties](#datatypeproperties)
1. [Named Individuals](#namedindividuals)
1. [Namespaces](#namespaces)
1. [Legend](#legend)


## Overview

**Figure 1:** Ontology overview
## Classes
[(1) Formal review](#(1)Formalreview),
[(1.1) Completeness check ](#(1.1)Completenesscheck),
[(1.2) Review preparation ](#(1.2)Reviewpreparation),
[(2) Assignment](#(2)Assignment),
[(3) Participation ](#(3)Participation),
[(4) Content review ](#(4)Contentreview),
[(5) Issuing notification letter ](#(5)Issuingnotificationletter),
[(5.1) Request review results ](#(5.1)Requestreviewresults),
[(5.2a) Positive permit decision ](#(5.2a)Positivepermitdecision),
[(5.2b) Negative permit decision ](#(5.2b)Negativepermitdecision),
[(5.3a) Formulation of condition ](#(5.3a)Formulationofcondition),
[(5.3b) Justification of negative decision ](#(5.3b)Justificationofnegativedecision),
[(5.4) Creating notification letter](#(5.4)Creatingnotificationletter),
[Activity](#Activity),
[Building](#Building),
[Building application](#Buildingapplication),
[Building authority](#Buildingauthority),
[Condition](#Condition),
[Dictionary](#Dictionary),
[Justification](#Justification),
[Review checking result](#Reviewcheckingresult),
[Review statement](#Reviewstatement),
[Review status](#Reviewstatus),
[SHACL shapes set](#SHACLshapesset),
### Activity
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#Activity`
Description | <p>an Activity executed throughout the building permit review</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[ontobpr:isCompleted](iscompleted) (dp) **exactly** 1<br />
Sub-classes |[ontobpr:CompletenessCheck]((1.1)Completenesscheck) (c)<br />[ontobpr:RequestReviewResults]((5.1)Requestreviewresults) (c)<br />[ontobpr:FormalReview]((1)Formalreview) (c)<br />[ontobpr:JustificationOfNegativeDecision]((5.3b)Justificationofnegativedecision) (c)<br />[ontobpr:CreatingNotificationLetter]((5.4)Creatingnotificationletter) (c)<br />[ontobpr:Participation]((3)Participation) (c)<br />[ontobpr:FormulationOfCondition]((5.3a)Formulationofcondition) (c)<br />[ontobpr:IssuingNotificationLetter]((5)Issuingnotificationletter) (c)<br />[ontobpr:ReviewPreparation]((1.2)Reviewpreparation) (c)<br />[ontobpr:PositivePermitDecision]((5.2a)Positivepermitdecision) (c)<br />[ontobpr:NegativePermitDecision]((5.2b)Negativepermitdecision) (c)<br />[ontobpr:Assignment]((2)Assignment) (c)<br />[ontobpr:ContentReview]((4)Contentreview) (c)<br />
In domain of |[ontobpr:afterActivity](afteractivity) (op)<br />[ontobpr:isCompleted](iscompleted) (dp)<br />
In range of |[ontobpr:belongsToActivity](belongstoactivity) (op)<br />[ontobpr:afterActivity](afteractivity) (op)<br />[ontobpr:hasCurrentActivity](hascurrentactivity) (op)<br />
### (2) Assignment
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#Assignment`
Description | <p>the Assignment activity</p>
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:FormalReview]((1)Formalreview) (c)<br />
### Building
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#Building`
Description | <p>The building that is subject of this building application</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[ontobpr:hasBuildingDocument](hasbuildingdocument) (op) **some** [ct:Document](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Document) (c)<br />
In domain of |[ontobpr:hasBuildingDocument](hasbuildingdocument) (op)<br />
### Building application
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#BuildingApplication`
Is Defined By | https://w3id.org/obpa#BuildingApplication
Description | <p>the building application that is submitted by an applicant for review</p>
Restrictions |[ontobpr:hasStatement](hasstatement) (op) **some** [ontobpr:ReviewStatement](Reviewstatement) (c)<br />[ontobpr:hasCheckingResults](hascheckingresults) (op) **some** [ontobpr:ReviewResult](Reviewcheckingresult) (c)<br />[ontobpr:hasBuildingApplicationContainer](hasbuildingapplicationcontainer) (op) **exactly** 1 [ct:ContainerDescription](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#ContainerDescription) (c)<br />[ontobpr:hasCurrentActivity](hascurrentactivity) (op) **exactly** 1 [ontobpr:Activity](Activity) (c)<br />[ontobpr:hasStatus](hasstatus) (op) **exactly** 1 [ontobpr:ReviewStatus](Reviewstatus) (c)<br />[ontobpr:hasApplicationDocument](hasapplicationdocument) (op) **some** [ct:Document](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Document) (c)<br />
In domain of |[ontobpr:hasBuildingApplicationContainer](hasbuildingapplicationcontainer) (op)<br />[ontobpr:hasStatement](hasstatement) (op)<br />[ontobpr:hasDocument](hasdocument) (op)<br />[ontobpr:hasStatus](hasstatus) (op)<br />[ontobpr:hasApplicationDocument](hasapplicationdocument) (op)<br />[ontobpr:hasCheckingResults](hascheckingresults) (op)<br />[ontobpr:applies](applies) (op)<br />[ontobpr:hasCurrentActivity](hascurrentactivity) (op)<br />
### Building authority
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#BuildingAuthority`
Is Defined By | https://w3id.org/obpa#BuildingAuthority
Description | <p>a building authority that is involved in a building permit review</p>
In domain of |[ontobpr:checks](checks) (op)<br />
### Dictionary
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#BuildingCodeDictionary`
Description | <p>A dictionary containing properties and shapes from a building code</p>
Restrictions |[ontobpr:hasShapesSet](hasshapesset) (op) **exactly** 1 [ontobpr:ShaclShapesSet](SHACLshapesset) (c)<br />
In domain of |[ontobpr:hasShapesSet](hasshapesset) (op)<br />
In range of |[ontobpr:applies](applies) (op)<br />[ontobpr:checks](checks) (op)<br />
### (1.1) Completeness check 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#CompletenessCheck`
Description | <p>the Completeness check activity</p>
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:hasShapesSet](hasshapesset) (op) **exactly** 1 [ontobpr:ShaclShapesSet](SHACLshapesset) (c)<br />
### Condition
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#Condition`
Description | <p>a formulated condition statement of a conditionally accepted application</p>
Super-classes |[ontobpr:ReviewStatement](Reviewstatement) (c)<br />
### (4) Content review 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#ContentReview`
Description | <p>The Content review activity</p>
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:FormalReview]((1)Formalreview) (c)<br />
### (5.4) Creating notification letter
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#CreatingNotificationLetter`
Description | <p>The Creating notification letter activity</p>
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **max** 1 [ontobpr:JustificationOfNegativeDecision]((5.3b)Justificationofnegativedecision) (c)<br />[ontobpr:afterActivity](afteractivity) (op) **max** 1 [ontobpr:FormulationOfCondition]((5.3a)Formulationofcondition) (c)<br />
### (1) Formal review
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#FormalReview`
Description | <p>The Formal review activity</p>
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **exactly** 1 [ontobpr:CompletenessCheck]((1.1)Completenesscheck) (c)<br />[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **exactly** 1 [ontobpr:ReviewPreparation]((1.2)Reviewpreparation) (c)<br />
### (5.3a) Formulation of condition 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#FormulationOfCondition`
Description | <p>the Formulation of condition activity</p>
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:PositivePermitDecision]((5.2a)Positivepermitdecision) (c)<br />
### (5) Issuing notification letter 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#IssuingNotificationLetter`
Description | <p>the Issuing notification letter activity</p>
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **exactly** 1 [ontobpr:CreatingNotificationLetter]((5.4)Creatingnotificationletter) (c)<br />[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **max** 1 [ontobpr:PositivePermitDecision]((5.2a)Positivepermitdecision) (c)<br />[ontobpr:afterActivity](afteractivity) (op) **max** 1 [ontobpr:Participation]((3)Participation) (c)<br />[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **max** 1 [ontobpr:NegativePermitDecision]((5.2b)Negativepermitdecision) (c)<br />[ontobpr:afterActivity](afteractivity) (op) **max** 1 [ontobpr:Assignment]((2)Assignment) (c)<br />[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **max** 1 [ontobpr:JustificationOfNegativeDecision]((5.3b)Justificationofnegativedecision) (c)<br />[ontobpr:afterActivity](afteractivity) (op) **max** 1 [ontobpr:ContentReview]((4)Contentreview) (c)<br />[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **exactly** 1 [ontobpr:RequestReviewResults]((5.1)Requestreviewresults) (c)<br />[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **max** 1 [ontobpr:FormulationOfCondition]((5.3a)Formulationofcondition) (c)<br />
### Justification
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#Justification`
Description | <p>justification statement of a negative building permit review decision</p>
Super-classes |[ontobpr:ReviewStatement](Reviewstatement) (c)<br />
### (5.3b) Justification of negative decision 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#JustificationOfNegativeDecision`
Description | <p>the Justification of negative decision activity</p>
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:NegativePermitDecision]((5.2b)Negativepermitdecision) (c)<br />
### (5.2b) Negative permit decision 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#NegativePermitDecision`
Description | <p>the Negative permit decision activity</p>
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:RequestReviewResults]((5.1)Requestreviewresults) (c)<br />
### (3) Participation 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#Participation`
Description | <p>the Participation activity</p>
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:FormalReview]((1)Formalreview) (c)<br />
### (5.2a) Positive permit decision 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#PositivePermitDecision`
Description | <p>the Positive permit decision activity</p>
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:RequestReviewResults]((5.1)Requestreviewresults) (c)<br />
### (5.1) Request review results 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#RequestReviewResults`
Description | <p>the Request review results activity</p>
Super-classes |[ontobpr:Activity](Activity) (c)<br />
### (1.2) Review preparation 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#ReviewPreparation`
Description | <p>the Review preparation activity</p>
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:CompletenessCheck]((1.1)Completenesscheck) (c)<br />
### Review checking result
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#ReviewResult`
Description | <p>the review result of a particular agent incorporating a sh:ValidationReport</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[ontobpr:hasCheckingResults](hascheckingresults) (op) **some** [sh:ValidationReport](http://www.w3.org/ns/shacl#ValidationReport) (c)<br />[obpa:hasAgent](https://w3id.org/obpa#hasAgent) **exactly** 1 [obpa:Agent](https://w3id.org/obpa#Agent) (c)<br />[dcterms:issued](http://purl.org/dc/terms/issued) **exactly** 1 [xsd:date](http://www.w3.org/2001/XMLSchema#date) (c)<br />
In range of |[ontobpr:hasCheckingResults](hascheckingresults) (op)<br />
### Review statement
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#ReviewStatement`
Description | <p>a general review statement for logging events during the building permit review</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[dcterms:issued](http://purl.org/dc/terms/issued) **exactly** 1 [xsd:date](http://www.w3.org/2001/XMLSchema#date) (c)<br />[obpa:hasAgent](https://w3id.org/obpa#hasAgent) **exactly** 1 [obpa:Agent](https://w3id.org/obpa#Agent) (c)<br />[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment) **exactly** 1 [xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />[ontobpr:belongsToActivity](belongstoactivity) (op) **exactly** 1 [ontobpr:Activity](Activity) (c)<br />
Sub-classes |[ontobpr:Condition](Condition) (c)<br />[ontobpr:Justification](Justification) (c)<br />
In domain of |[ontobpr:belongsToActivity](belongstoactivity) (op)<br />
In range of |[ontobpr:hasStatement](hasstatement) (op)<br />
### Review status
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#ReviewStatus`
Description | <p>the status of the building application within the building permit review</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In range of |[ontobpr:hasStatus](hasstatus) (op)<br />
### SHACL shapes set
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#ShaclShapesSet`
Description | <p>a set of SHACL shapes for validating data at various activities of the building permit review</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[ontobpr:hasShapes](hasshapes) (op) **some** [sh:Shape](http://www.w3.org/ns/shacl#Shape) (c)<br />
In domain of |[ontobpr:hasShapes](hasshapes) (op)<br />
In range of |[ontobpr:hasShapesSet](hasshapesset) (op)<br />

## Object Properties
[after activity](#afteractivity),
[applies](#applies),
[belongs to activity](#belongstoactivity),
[checks](#checks),
[has application document](#hasapplicationdocument),
[has building application container](#hasbuildingapplicationcontainer),
[has building document](#hasbuildingdocument),
[has checking results](#hascheckingresults),
[has current activity](#hascurrentactivity),
[has document](#hasdocument),
[has shapes](#hasshapes),
[has shapes set](#hasshapesset),
[has statement](#hasstatement),
[has status](#hasstatus),
[](afteractivity)
### after activity
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#afterActivity`
Description | an activity is executed after another activity
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[ontobpr:Activity](Activity) (c)<br />
Range(s) |[ontobpr:Activity](Activity) (c)<br />
[](applies)
### applies
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#applies`
Description | BuildingApplication applies a BuildingCodeDictionary for checking
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[obpa:BuildingApplication](https://w3id.org/obpa#BuildingApplication) (c)<br />[ontobpr:BuildingApplication](Buildingapplication) (c)<br />
Range(s) |[isoprops:Dictionary](https://w3id.org/isoprops#Dictionary) (c)<br />[ontobpr:BuildingCodeDictionary](Dictionary) (c)<br />
[](belongstoactivity)
### belongs to activity
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#belongsToActivity`
Description | a ReviewStatement belongs to a particular Activity
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[ontobpr:ReviewStatement](Reviewstatement) (c)<br />
Range(s) |[ontobpr:Activity](Activity) (c)<br />
[](checks)
### checks
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#checks`
Description | BuildingAuthority checks a building regarding a BuildingCodeDictionary
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[obpa:BuildingAuthority](https://w3id.org/obpa#BuildingAuthority) (c)<br />[ontobpr:BuildingAuthority](Buildingauthority) (c)<br />
Range(s) |[isoprops:Dictionary](https://w3id.org/isoprops#Dictionary) (c)<br />[ontobpr:BuildingCodeDictionary](Dictionary) (c)<br />
[](hasapplicationdocument)
### has application document
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasApplicationDocument`
Description | a BuildingApplication has a respective document (e.g. PDF) representing a human-readable version of the application
Super-properties |[ontobpr:hasDocument](hasdocument) (op)<br />
Domain(s) |[ontobpr:BuildingApplication](Buildingapplication) (c)<br />
Range(s) |[ct:Document](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Document) (c)<br />
[](hasbuildingapplicationcontainer)
### has building application container
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasBuildingApplicationContainer`
Description | the reference from a BuildingApplication to an ICDD container
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[ontobpr:BuildingApplication](Buildingapplication) (c)<br />
Range(s) |[ct:ContainerDescription](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#ContainerDescription) (c)<br />
[](hasbuildingdocument)
### has building document
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasBuildingDocument`
Description | A Building has a document, which is the IFC representation of this Building
Super-properties |[ontobpr:hasDocument](hasdocument) (op)<br />
Domain(s) |[ontobpr:Building](Building) (c)<br />
Range(s) |[ct:Document](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Document) (c)<br />
[](hascheckingresults)
### has checking results
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasCheckingResults`
Description | either a BuildingApplication has ReviewResult or a ReviewResult has sh:ValidationReport
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[ontobpr:BuildingApplication](Buildingapplication) (c)<br />
Range(s) |[ontobpr:ReviewResult](Reviewcheckingresult) (c)<br />
[](hascurrentactivity)
### has current activity
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasCurrentActivity`
Description | a BuildingApplication is in the current Activity
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[ontobpr:BuildingApplication](Buildingapplication) (c)<br />
Range(s) |[ontobpr:Activity](Activity) (c)<br />
[](hasdocument)
### has document
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasDocument`
Description | abstract property grouping hasApplicationDocument and hasBuildingDocument
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[ontobpr:BuildingApplication](Buildingapplication) (c)<br />
Range(s) |[ct:Document](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Document) (c)<br />
[](hasshapes)
### has shapes
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasShapes`
Description | ShaclShapesSet has sh:Shape instances
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[ontobpr:ShaclShapesSet](SHACLshapesset) (c)<br />
Range(s) |[sh:Shape](http://www.w3.org/ns/shacl#Shape) (c)<br />
[](hasshapesset)
### has shapes set
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasShapesSet`
Description | either an Activity or a BuildingCodeDictionary has a ShaclShapesSet
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[ontobpr:BuildingCodeDictionary](Dictionary) (c)<br />
Range(s) |[ontobpr:ShaclShapesSet](SHACLshapesset) (c)<br />
[](hasstatement)
### has statement
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasStatement`
Description | any ReviewStatement of any reviewer is attached to a BuildingApplication
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[ontobpr:BuildingApplication](Buildingapplication) (c)<br />
Range(s) |[ontobpr:ReviewStatement](Reviewstatement) (c)<br />
[](hasstatus)
### has status
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasStatus`
Description | the ReviewStatus of a BuildingApplication
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[ontobpr:BuildingApplication](Buildingapplication) (c)<br />
Range(s) |[ontobpr:ReviewStatus](Reviewstatus) (c)<br />

## Datatype Properties
[is completed](#iscompleted),
[](iscompleted)
### is completed
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#isCompleted`
Description | a boolean property indicating whether an activity is completet or not
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[ontobpr:Activity](Activity) (c)<br />
Range(s) |[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean) (c)<br />

## Named Individuals
[Accepted](#Accepted),
[Accepted with conditions](#Acceptedwithconditions),
[Rejected](#Rejected),
[Request information](#Requestinformation),
[Under review](#Underreview),
### Accepted <sup>c</sup>
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#Accepted`
* **Contributor(s)**
  * [ontobpr:ReviewStatus](https://w3id.org/ontobpr#ReviewStatus)
### Accepted with conditions <sup>c</sup>
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#AcceptedWithConditions`
* **Contributor(s)**
  * [ontobpr:ReviewStatus](https://w3id.org/ontobpr#ReviewStatus)
### Rejected <sup>c</sup>
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#Rejected`
* **Contributor(s)**
  * [ontobpr:ReviewStatus](https://w3id.org/ontobpr#ReviewStatus)
### Request information <sup>c</sup>
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#RequestInformation`
* **Contributor(s)**
  * [ontobpr:ReviewStatus](https://w3id.org/ontobpr#ReviewStatus)
### Under review <sup>c</sup>
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#UnderReview`
* **Contributor(s)**
  * [ontobpr:ReviewStatus](https://w3id.org/ontobpr#ReviewStatus)
## Namespaces
* **default (:)**
  * `https://w3id.org/ontobpr#`
* **ct**
  * `https://standards.iso.org/iso/21597/-1/ed-1/en/Container#`
* **dc**
  * `http://purl.org/dc/elements/1.1/`
* **dcterms**
  * `http://purl.org/dc/terms/`
* **isoprops**
  * `https://w3id.org/isoprops#`
* **obpa**
  * `https://w3id.org/obpa#`
* **ontobpr**
  * `https://w3id.org/ontobpr#`
* **owl**
  * `http://www.w3.org/2002/07/owl#`
* **prov**
  * `http://www.w3.org/ns/prov#`
* **rdf**
  * `http://www.w3.org/1999/02/22-rdf-syntax-ns#`
* **rdfs**
  * `http://www.w3.org/2000/01/rdf-schema#`
* **sdo**
  * `https://schema.org/`
* **sh**
  * `http://www.w3.org/ns/shacl#`
* **skos**
  * `http://www.w3.org/2004/02/skos/core#`
* **vann**
  * `http://purl.org/vocab/vann/`
* **xml**
  * `http://www.w3.org/XML/1998/namespace`
* **xsd**
  * `http://www.w3.org/2001/XMLSchema#`

## Legend
* Classes: c
* Object Properties: op
* Functional Properties: fp
* Data Properties: dp
* Annotation Properties: dp
* Properties: p
* Named Individuals: ni