---
title: CapabilityStatements for the IG
layout: default
active: capstatements
---
<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

* Do not remove this line (it will not be displayed)
{:toc}

<!-- end TOC -->


The section outlines conformance requirements for each of the CRN actors which includes the specific profiles, operations, security mechanisms and search parameters that need to be supported.

### CRN Instrument and Meta data Repository Conformance Requirements

The following are the conformance requirements for the CRN Instrument and Meta data Repository.

The CRN Instrument and Meta data Repository **SHALL**:

* Support the Questionnaire resource, SDC Questionnaire profile and PRO Questionnaire profile.
* Implement the RESTful behavior according to the FHIR specification.
    * which includes returning the following response classes:
        * (Status 200): successful operation
        * (Status 400): invalid parameter
        * (Status 401/4xx): unauthorized request
        * (Status 403): insufficient scope
        * (Status 404): unknown resource
        * (Status 410): deleted resource.
    * Support json resource formats for all CRN interactions.
* Declare a CapabilityStatement identifying the list of profiles, operations, and search parameters supported.

The CRN Instrument and Meta data Repository **SHOULD**:

* Support xml resource formats for all PRO interactions.
* Identify the SDC, PRO and CRN profiles supported as part of the FHIR meta.profile attribute for each instance.

The CRN Instrument and Meta data Repository **MAY**:

* Support other resource profiles

#### Profile Interactions:

The CRN Instrument and Meta data Repository SHALL support 
* **FHIR POST interaction for Questionnaire.** 
* **FHIR READ interaction for Questionnaire.** 
* **FHIR Search interaction for Questionnaire.**

The CRN Instrument and Meta data Repository MAY support other FHIR profile interactions.

#### Security:

The CRN Instrument and Meta data Repository **SHALL** support the Communication security mechanisms outlined in [FHIR Security](http://hl7.org/fhir/security.html)

The CRN Instrument and Meta data Repository **SHOULD** support other security recommendations outlined in [FHIR Security](http://hl7.org/fhir/security.html) as appropriate.

#### Search Parameters

The CRN Instrument and Meta data Repository **SHALL** support the following search parameters and combination for the Questionnaire resource

* identifier - Search by Questionnaire identifier (e.g QOL)
* identifier & version - Search by Questionnaire identifier and version (e.g PHQ-9 v1)

The following is an example of the search query.

`GET [FHIR Server URL]/Questionaire?identifier – Search by Questionnaire Identifier (e.g PHQ-9)`

`GET [FHIR Server URL]/Questionaire?identifier & version – Search by Questionnaire Identifier and version (e.g PHQ-9 v1)`


### External CRN Data Collection System Conformance Requirements

The following are the conformance requirements for the External CRN Data Collection System.

The External PRO Administration System **SHALL**:

* Support the Questionnaire, QuestionnaireResponse resources and specific SDC and PRO profiles developed for these resources.
* Support the US Core profiles to be used for pre-populating the CRN Instrument
* Support the US Core profiles to convert QuestionnaireResponses to FHIR Resources.

* Implement the RESTful behavior according to the FHIR specification
    * which includes returning the following response classes:
        * (Status 200): successful operation
        * (Status 400): invalid parameter
        * (Status 401/4xx): unauthorized request
        * (Status 403): insufficient scope
        * (Status 404): unknown resource
        * (Status 410): deleted resource.
    * Support json resource formats for all CRN interactions.
* Declare a CapabilityStatement identifying the list of profiles, operations, and search parameters supported.

The External CRN Data Collection System **SHOULD**:

* Support the resource profiles identified on the [Profiles page](profiles.html) .
* Support xml resource formats for all CRN interactions.
* Identify the CRN profiles supported as part of the FHIR meta.profile attribute for each instance.

The External CRN Data Collection System **MAY**:

* Support other resource profiles

#### Profile Interactions:

The External CRN Data Collection System **SHALL** support 

* ** FHIR POST interaction for Questionnaire, QuestionnaireResponse, CRN profiles and US Core profiles ** 
* ** FHIR READ interaction for Questionnaire, QuestionnaireResponse, CRN profiles and US Core profiles ** 
* ** FHIR Search interaction for Questionnaire, QuestionnaireResponse, CRN profiles and US Core profiles **

The External CRN Data Collection System **MAY** support other FHIR profile interactions.

#### Security:
The External CRN Data Collection System **SHALL** support the Communication security mechanisms outlined in [FHIR Security specification](http://hl7.org/fhir/security.html)

The External CRN Data Collection System **SHOULD** support other security recommendations outlined in [FHIR Security specification](http://hl7.org/fhir/security.html) as appropriate.

In the case of interacting with an EHR system for storing CRN data collected, the External CRN Data Collection System **SHALL** support the SMART on FHIR Authorization specification with patient launch context.

#### Search:
The External CRN Data Collection System **SHALL** support the following search parameters and combinations

Questionnaire Resource Search parameters
    * identifier - Search by Questionnaire identifier (e.g PHQ-9)
    * identifier & version - Search by Questionnaire identifier and version (e.g PHQ-9 v1)
QuestionnaireResponse Resource Search parameters
    * identifier - Search by Questionnaire identifier (e.g PHQ-9)
    * Search Parameters for QuestionnaireResponse defined at http://hl7.org/fhir/questionnaireresponse.html
Search parameters as identified by US Core profiles
Search parameters as identified by CRN profiles


{% include list-capabilitystatements.xhtml %}
<br />
