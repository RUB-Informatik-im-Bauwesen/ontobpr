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
[Shacl shapes set](#Shaclshapesset),
### Activity
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#Activity`
Is Defined By | https://w3id.org/obpa#Activity
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[ontobpr:isCompleted](iscompleted) (dp) **exactly** 1<br />
Sub-classes |[ontobpr:IssuingNotificationLetter]((5)Issuingnotificationletter) (c)<br />[ontobpr:CreatingNotificationLetter]((5.4)Creatingnotificationletter) (c)<br />[ontobpr:FormulationOfCondition]((5.3a)Formulationofcondition) (c)<br />[ontobpr:JustificationOfNegativeDecision]((5.3b)Justificationofnegativedecision) (c)<br />[ontobpr:NegativePermitDecision]((5.2b)Negativepermitdecision) (c)<br />[ontobpr:Assignment]((2)Assignment) (c)<br />[ontobpr:RequestReviewResults]((5.1)Requestreviewresults) (c)<br />[ontobpr:PositivePermitDecision]((5.2a)Positivepermitdecision) (c)<br />[ontobpr:CompletenessCheck]((1.1)Completenesscheck) (c)<br />[ontobpr:ReviewPreparation]((1.2)Reviewpreparation) (c)<br />[ontobpr:ContentReview]((4)Contentreview) (c)<br />[ontobpr:Participation]((3)Participation) (c)<br />[ontobpr:FormalReview]((1)Formalreview) (c)<br />
In domain of |[ontobpr:isCompleted](iscompleted) (dp)<br />[ontobpr:afterActivity](afteractivity) (op)<br />
In range of |[ontobpr:hasCurrentActivity](hascurrentactivity) (op)<br />[ontobpr:afterActivity](afteractivity) (op)<br />
### (2) Assignment
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#Assignment`
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:FormalReview]((1)Formalreview) (c)<br />
### Building
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#Building`
Is Defined By | https://w3id.org/obpa#Building
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[ontobpr:hasBuildingDocument](hasbuildingdocument) (op) **some** [ct:Document](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Document) (c)<br />
### Building application
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#BuildingApplication`
Is Defined By | https://w3id.org/obpa#BuildingApplication
Restrictions |[ontobpr:hasStatus](hasstatus) (op) **exactly** 1 [ontobpr:ReviewStatus](Reviewstatus) (c)<br />[ontobpr:hasCurrentActivity](hascurrentactivity) (op) **exactly** 1 [ontobpr:Activity](Activity) (c)<br />[ontobpr:hasBuildingApplicationContainer](hasbuildingapplicationcontainer) (op) **exactly** 1 [ct:ContainerDescription](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#ContainerDescription) (c)<br />[ontobpr:hasStatement](hasstatement) (op) **some** [ontobpr:ReviewStatement](Reviewstatement) (c)<br />[ontobpr:hasApplicationDocument](hasapplicationdocument) (op) **some** [ct:Document](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Document) (c)<br />[ontobpr:hasCheckingResults](hascheckingresults) (op) **some** [ontobpr:ReviewCheckingResults](https://w3id.org/ontobpr#ReviewCheckingResults) (c)<br />
In domain of |[ontobpr:hasCurrentActivity](hascurrentactivity) (op)<br />[ontobpr:hasBuildingApplicationContainer](hasbuildingapplicationcontainer) (op)<br />[ontobpr:hasStatement](hasstatement) (op)<br />[ontobpr:hasStatus](hasstatus) (op)<br />
### Building authority
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#BuildingAuthority`
Is Defined By | https://w3id.org/obpa#BuildingAuthority
### (1.1) Completeness check 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#CompletenessCheck`
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:hasShapesSet](hasshapesset) (op) **exactly** 1 [ontobpr:ShaclShapesSet](Shaclshapesset) (c)<br />
### Condition
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#Condition`
Super-classes |[ontobpr:ReviewStatement](Reviewstatement) (c)<br />
### (4) Content review 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#ContentReview`
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:FormalReview]((1)Formalreview) (c)<br />
### (5.4) Creating notification letter
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#CreatingNotificationLetter`
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **max** 1 [ontobpr:FormulationOfCondition]((5.3a)Formulationofcondition) (c)<br />[ontobpr:afterActivity](afteractivity) (op) **max** 1 [ontobpr:JustificationOfNegativeDecision]((5.3b)Justificationofnegativedecision) (c)<br />
### Dictionary
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#Dictionary`
Is Defined By | https://w3id.org/isoprops#Dictionary
### (1) Formal review
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#FormalReview`
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **exactly** 1 [ontobpr:ReviewPreparation]((1.2)Reviewpreparation) (c)<br />[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **exactly** 1 [ontobpr:CompletenessCheck]((1.1)Completenesscheck) (c)<br />
### (5.3a) Formulation of condition 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#FormulationOfCondition`
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:PositivePermitDecision]((5.2a)Positivepermitdecision) (c)<br />
### (5) Issuing notification letter 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#IssuingNotificationLetter`
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **max** 1 [ontobpr:Assignment]((2)Assignment) (c)<br />[ontobpr:afterActivity](afteractivity) (op) **max** 1 [ontobpr:ContentReview]((4)Contentreview) (c)<br />[ontobpr:afterActivity](afteractivity) (op) **max** 1 [ontobpr:Participation]((3)Participation) (c)<br />[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **max** 1 [ontobpr:JustificationOfNegativeDecision]((5.3b)Justificationofnegativedecision) (c)<br />[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **max** 1 [ontobpr:NegativePermitDecision]((5.2b)Negativepermitdecision) (c)<br />[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **exactly** 1 [ontobpr:RequestReviewResults]((5.1)Requestreviewresults) (c)<br />[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **exactly** 1 [ontobpr:CreatingNotificationLetter]((5.4)Creatingnotificationletter) (c)<br />[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **max** 1 [ontobpr:FormulationOfCondition]((5.3a)Formulationofcondition) (c)<br />[obpa:hasSubActivity](https://w3id.org/obpa#hasSubActivity) **max** 1 [ontobpr:PositivePermitDecision]((5.2a)Positivepermitdecision) (c)<br />
### Justification
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#Justification`
Super-classes |[ontobpr:ReviewStatement](Reviewstatement) (c)<br />
### (5.3b) Justification of negative decision 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#JustificationOfNegativeDecision`
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:NegativePermitDecision]((5.2b)Negativepermitdecision) (c)<br />
### (5.2b) Negative permit decision 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#NegativePermitDecision`
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:RequestReviewResults]((5.1)Requestreviewresults) (c)<br />
### (3) Participation 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#Participation`
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:FormalReview]((1)Formalreview) (c)<br />
### (5.2a) Positive permit decision 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#PositivePermitDecision`
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:RequestReviewResults]((5.1)Requestreviewresults) (c)<br />
### (5.1) Request review results 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#RequestReviewResults`
Super-classes |[ontobpr:Activity](Activity) (c)<br />
### (1.2) Review preparation 
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#ReviewPreparation`
Super-classes |[ontobpr:Activity](Activity) (c)<br />
Restrictions |[ontobpr:afterActivity](afteractivity) (op) **exactly** 1 [ontobpr:CompletenessCheck]((1.1)Completenesscheck) (c)<br />
### Review checking result
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#ReviewResult`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[ontobpr:hasCheckingResults](hascheckingresults) (op) **some** [sh:ValidationReport](http://www.w3.org/ns/shacl#ValidationReport) (c)<br />[obpa:hasAgent](https://w3id.org/obpa#hasAgent) **exactly** 1 [obpa:Agent](https://w3id.org/obpa#Agent) (c)<br />[dcterms:issued](http://purl.org/dc/terms/issued) **exactly** 1 [xsd:date](http://www.w3.org/2001/XMLSchema#date) (c)<br />
### Review statement
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#ReviewStatement`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[dcterms:issued](http://purl.org/dc/terms/issued) **exactly** 1 [xsd:date](http://www.w3.org/2001/XMLSchema#date) (c)<br />[obpa:hasAgent](https://w3id.org/obpa#hasAgent) **exactly** 1 [obpa:Agent](https://w3id.org/obpa#Agent) (c)<br />[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment) **exactly** 1 [xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
Sub-classes |[ontobpr:Condition](Condition) (c)<br />[ontobpr:Justification](Justification) (c)<br />
In range of |[ontobpr:hasStatement](hasstatement) (op)<br />
### Review status
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#ReviewStatus`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In range of |[ontobpr:hasStatus](hasstatus) (op)<br />
### Shacl shapes set
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#ShaclShapesSet`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[ontobpr:hasShapes](hasshapes) (op) **some** [sh:Shape](http://www.w3.org/ns/shacl#Shape) (c)<br />
In domain of |[ontobpr:hasShapes](hasshapes) (op)<br />
In range of |[ontobpr:hasShapesSet](hasshapesset) (op)<br />

## Object Properties
[after activity](#afteractivity),
[applies](#applies),
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
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[ontobpr:Activity](Activity) (c)<br />
Range(s) |[ontobpr:Activity](Activity) (c)<br />
[](applies)
### applies
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#applies`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[obpa:BuildingApplication](https://w3id.org/obpa#BuildingApplication) (c)<br />
Range(s) |[isoprops:Dictionary](https://w3id.org/isoprops#Dictionary) (c)<br />
[](checks)
### checks
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#checks`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Dictionary](https://w3id.org/isoprops#Dictionary) (c)<br />
Range(s) |[obpa:BuildingAuthority](https://w3id.org/obpa#BuildingAuthority) (c)<br />
[](hasapplicationdocument)
### has application document
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasApplicationDocument`
Super-properties |[ontobpr:hasDocument](hasdocument) (op)<br />
Range(s) |[ct:Document](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Document) (c)<br />
[](hasbuildingapplicationcontainer)
### has building application container
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasBuildingApplicationContainer`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[ontobpr:BuildingApplication](Buildingapplication) (c)<br />
Range(s) |[ct:ContainerDescription](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#ContainerDescription) (c)<br />
[](hasbuildingdocument)
### has building document
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasBuildingDocument`
Super-properties |[ontobpr:hasDocument](hasdocument) (op)<br />
Range(s) |[ct:Document](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Document) (c)<br />
[](hascheckingresults)
### has checking results
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasCheckingResults`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
[](hascurrentactivity)
### has current activity
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasCurrentActivity`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[ontobpr:BuildingApplication](Buildingapplication) (c)<br />
Range(s) |[ontobpr:Activity](Activity) (c)<br />
[](hasdocument)
### has document
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasDocument`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
[](hasshapes)
### has shapes
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasShapes`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[ontobpr:ShaclShapesSet](Shaclshapesset) (c)<br />
Range(s) |[sh:Shape](http://www.w3.org/ns/shacl#Shape) (c)<br />
[](hasshapesset)
### has shapes set
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasShapesSet`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Range(s) |[ontobpr:ShaclShapesSet](Shaclshapesset) (c)<br />
[](hasstatement)
### has statement
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasStatement`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[ontobpr:BuildingApplication](Buildingapplication) (c)<br />
Range(s) |[ontobpr:ReviewStatement](Reviewstatement) (c)<br />
[](hasstatus)
### has status
Property | Value
--- | ---
IRI | `https://w3id.org/ontobpr#hasStatus`
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