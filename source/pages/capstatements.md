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

### CRN Instrument and Metadata Repository Conformance Requirements

The following are the conformance requirements for the CRN Instrument and Meta data Repository.

#### Behavior and Formats

The CRN Instrument and Meta data Repository **SHALL**: 
* Implement the RESTful behavior according to the [FHIR HTTP Specification](http://hl7.org/fhir/http.html).
* Support **json** resource formats for all CRN interactions.
* Declare a CapabilityStatement identifying the list of profiles, operations and search parameters supported.

---
**Implementation Note**
The FHIR HTTP specification outlines specific requirements on how to deal with successful operations, invalid parameters, unauthorized request, insufficient scopes, unknown resources etc.

---
#### Profiles and Interactions

The CRN Instrument and Meta data Repository needs to implement the profile specific interactions as specified in the table below.

---
**Implementation Note**
The way to read the table (for example the first row) is as follows

The CRN Instrument and Metadata Repository **SHALL** support the CREATE, READ, SEARCH operations, SHOULD support the vREAD and HISTORY operations for the SDC Questionnaire profile.

--- 

| Profile Name          | create     | read       | search (type level)      | vread          |  history (instance level) |
|:----------------------|-----------:|-----------:|-------------------------:|---------------:|--------------------------:|
|[SDC Questionnaire](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire.html)|SHALL|SHALL|SHALL|SHOULD|SHOULD|
|[SDC Populatable Questionnaire](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire-populate.html)|SHALL|SHALL|SHALL|SHOULD|SHOULD|
|[SDC Extractable Questionnaire](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire-extract.html)|SHALL|SHALL|SHALL|SHOULD|SHOULD|
|[SDC Adaptive Questionnaire](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire-adapt.html)|SHALL|SHALL|SHALL|SHOULD|SHOULD|

#### Search and Other Parameters

The CRN Instrument and Meta data Repository needs to implement the search parameters as specified in the table below.

---
**Implementation Note**
The way to read the table (for example the first row) is as follows

The CRN Instrument and Metadata Repository **SHALL** support _id, identifier, combination of identifier & version search parameters and _summary search result parameters for the SDC Questionnaire profile.

--- 

| Profile Name          | SEARCH and Search Result parameters and combinations     |   
|:----------------------|---------------------------------------------------------:|
|[All SDC Questionnaire profiles](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire.html)|_id (SHALL)|
||identifier (SHALL)|
||identifier & version (SHALL)|
||_summary (SHALL)|


#### Security Requirements

The CRN Instrument and Meta data Repository **SHALL** support the Communication security mechanisms outlined in [FHIR Security Specification](http://hl7.org/fhir/security.html#http)

The CRN Instrument and Meta data Repository **SHALL** support the Authenitication security mechanisms outlined in [FHIR Security Specification](http://hl7.org/fhir/security.html#authentication)

The CRN Instrument and Meta data Repository **SHOULD** support other security recommendations outlined in FHIR Security as appropriate.

### External CRN Data Collection System Conformance Requirements

The following are the conformance requirements for the External CRN Data Collection System.

#### Behavior and Formats

The External CRN Data Collection System **SHALL**: 
* Implement the RESTful behavior according to the [FHIR HTTP Specification](http://hl7.org/fhir/http.html).
* Support **json** resource formats for all CRN interactions.
* Declare a CapabilityStatement identifying the list of profiles, operations and search parameters supported.

---
**Implementation Note**
The FHIR HTTP specification outlines specific requirements on how to deal with successful operations, invalid parameters, unauthorized request, insufficient scopes, unknown resources etc.

---
#### Profiles and Interactions

The External CRN Data Collection System needs to implement the profile specific interactions as specified in the table below.

---
**Implementation Note**
The way to read the table (for example the first row) is as follows

The External CRN Data Collection System **SHALL** support the CREATE, READ, SEARCH operations, SHOULD support the vREAD and HISTORY operations for the SDC Questionnaire profile.

--- 

| Profile/Resource Name          | create     | read       | search (type level)      | vread          |  history (instance level) |
|:----------------------|-----------:|-----------:|-------------------------:|---------------:|--------------------------:|
|[SDC Questionnaire](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire.html)|SHALL|SHALL|SHALL|SHOULD|SHOULD|
|[SDC QuestionnaireResponse](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaireresponse.html)|SHALL|SHALL|SHALL|SHOULD|SHOULD|
|[SDC Populatable Questionnaire - Note2](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire-populate.html)|SHOULD|SHOULD|SHOULD|SHOULD|SHOULD|
|[SDC Extractable Questionnaire - Note2](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire-extract.html)|SHOULD|SHOULD|SHOULD|SHOULD|SHOULD|
|[SDC Adaptive Questionnaire - Note2](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire-adapt.html)|SHOULD|SHOULD|SHOULD|SHOULD|SHOULD|
|[US Core Profiles - Note1](http://hl7.org/fhir/us/core/index.html)|MAY|MAY|MAY|MAY|MAY|

---
**Note1**
US Core Profiles are optional and only needs to be supported if the External CRN Data Collection System intends to auto populate the Questionnaire or extract data from QuestionnaireResponse.

**Note2**
The different variations of Questionnaire profiles are optional only needed if the External CRN Data Collection System intends to autopopulate, transform collected data to FHIR Resources, administer adaptive Questionnaires.

--- 

#### Search and Other Parameters

The External CRN Data Collection System needs to implement the search parameters as specified in the table below.

---
**Implementation Note**
The way to read the table (for example the first row) is as follows

The External CRN Data Collection System **SHALL** support _id, identifier, combination of identifier & version search parameters and _summary search result parameters for the SDC Questionnaire profile.

--- 

| Profile Name          | SEARCH and Search Result parameters and combinations     |   
|:----------------------|---------------------------------------------------------:|
|[All SDC Questionnaire profiles](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire.html)|_id (SHALL)|
||identifier (SHALL)|
||identifier & version (SHALL)|
||_summary (SHALL)|
|[SDC QuestionnaireResponse](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaireresponse.html)|_id (SHALL)|
||identifier (SHALL)|
||patient (SHALL)|
||questionnaire (SHALL)|
||author (SHALL)|
||authored (SHALL)|
|[US Core profiles](http://hl7.org/fhir/us/core/index.html)|SHOULD support Search parameters as specified by US Core|

#### Auto population options

External CRN Data Collection System **SHOULD** support the auto population of CRN instrument using the [Questionnaire Populate](http://build.fhir.org/questionnaire-operations.html#populate) operation leveraging the following techniques
* Use FHIRPath to determine auto population questions and resources. This is described further in [SDC Populate Page](http://build.fhir.org/ig/HL7/sdc/populate.html#path-pop).
* Using SMART on FHIR EHR launch sequence to obtain essential context data 
* Query EHR using US Core profile APIs to extract the data necessary to populate the instrument

#### Transforming QuestionnaireResponse to FHIR Resources

Many systems deal with granular FHIR Resources such as Observations, Conditions, AllergyIntolerance, MedicationStatement etc and capturing information using these FHIR Resources will make the data available for many use cases. On the other hand when instruments are used to capture data in the form of QuestionnaireResponse and stored as QuestionnaireResponse, the data is not widely available for a number of use cases. In order to reuse the data for different use cases and make it available via appropriate FHIR Resources, the QuestionnaireResponse can be translated into FHIR Resources using the techniques outlined at [SDC Extract Operations](http://build.fhir.org/ig/HL7/sdc/extraction.html).

External CRN Data Collection System **SHOULD** support the [SDC Extract Operations](http://build.fhir.org/ig/HL7/sdc/extraction.html) to transform data from QuestionnaireResponse to FHIR Resources. 

#### Administering Adaptive Questionnaires and PRO Measures

External CRN Data Collection System **SHOULD** use the [PRO FHIR IG](http://build.fhir.org/ig/HL7/patient-reported-outcomes/index.html) capabilities to administer Adaptive Questionnaires and PRO Measures.

#### Security Requirements

The External CRN Data Collection System **SHALL** support the Communication security mechanisms outlined in [FHIR Security Specification](http://hl7.org/fhir/security.html#http)

The External CRN Data Collection System **SHALL** support the Authentication security mechanisms outlined in [FHIR Security Specification](http://hl7.org/fhir/security.html#authentication)

The External CRN Data Collection System **SHOULD** support other security recommendations outlined in FHIR Security as appropriate.

#### SMART on FHIR App Interactions 

For External CRN Data Collection System interacting with EHRs to receive patient and other clinical context data from the EHR the following requirments apply:

The External CRN Data Collection System **SHALL** support the **EHR Launch Sequence** from the [SMART on FHIR App Authorization guide](http://docs.smarthealthit.org/authorization) as a client.

The External CRN Data Collection System **SHALL** request information from EHR during **EHR Launch Sequence** using tokens and parameters for [US Core profiles](http://hl7.org/fhir/us/core/index.html) as a client.

In order to store collected CRN data in the EHR, The External CRN Data Collection System **SHALL** use create interaction for the  SDC QuestionnnaireResponse profile with the EHR as the target system. (In other words the External App will do a POST to the EHR FHIR endpoint to store the QuestionnaireResponse data).

### Womens Health Registry

The following are the conformance requirements for the Womens Health Registry actor.

#### Behavior and Formats

The Womens Health Registry **SHALL**: 
* Implement the RESTful behavior according to the [FHIR HTTP Specification](http://hl7.org/fhir/http.html).
* Support **json** resource formats for all CRN interactions.
* Declare a CapabilityStatement identifying the list of profiles, operations and search parameters supported.

---
**Implementation Note**
The FHIR HTTP specification outlines specific requirements on how to deal with successful operations, invalid parameters, unauthorized request, insufficient scopes, unknown resources etc.

---
#### Profiles and Interactions

The Womens Health Registry needs to implement the profile specific interactions as specified in the table below.

---
**Implementation Note**
The way to read the table (for example the first row) is as follows

The Womens Health Registry **SHALL** support the CREATE, READ, SEARCH operations, SHOULD support the vREAD and HISTORY operations for the SDC Questionnaire profile.

--- 

| Profile/Resource Name          | create     | read       | search (type level)      | vread          |  history (instance level) |
|:----------------------|-----------:|-----------:|-------------------------:|---------------:|--------------------------:|
|[SDC Questionnaire](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire.html)|SHALL|SHALL|SHALL|SHOULD|SHOULD|
|[SDC QuestionnaireResponse](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaireresponse.html)|SHALL|SHALL|SHALL|SHOULD|SHOULD|
|[US Core Profiles - Note1](http://hl7.org/fhir/us/core/index.html)|SHOULD|SHOULD|SHOULD|SHOULD|SHOULD|

---
**Note1**
US Core Profiles are optional and only needs to be supported if the Womens Health Registry receives data in the form of US Core profiles or if it transforms the QuestionnaireResponse to other FHIR Resources.

--- 

#### Search and Other Parameters

The Womens Health Registry needs to implement the search parameters as specified in the table below.

---
**Implementation Note**
The way to read the table (for example the first row) is as follows

The Womens Health Registry **SHALL** support _id, identifier, combination of identifier & version search parameters and _summary search result parameters for the SDC Questionnaire profile.

--- 

| Profile Name          | SEARCH and Search Result parameters and combinations     |   
|:----------------------|---------------------------------------------------------:|
|[All SDC Questionnaire profiles](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire.html)|_id (SHALL)|
||identifier (SHALL)|
||identifier & version (SHALL)|
||_summary (SHALL)|
|[SDC QuestionnaireResponse](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaireresponse.html)|_id (SHALL)|
||identifier (SHALL)|
||patient (SHALL)|
||questionnaire (SHALL)|
||author (SHALL)|
||authored (SHALL)|
|[US Core profiles](http://hl7.org/fhir/us/core/index.html)|SHOULD support Search parameters as specified by US Core|

#### Transforming QuestionnaireResponse to FHIR Resources

Many systems deal with granular FHIR Resources such as Observations, Conditions, AllergyIntolerance, MedicationStatement etc and capturing information using these FHIR Resources will make the data available for many use cases. On the other hand when instruments are used to capture data in the form of QuestionnaireResponse and stored as QuestionnaireResponse, the data is not widely available for a number of use cases. In order to reuse the data for different use cases and make it available via appropriate FHIR Resources, the QuestionnaireResponse can be translated into FHIR Resources using the techniques outlined at [SDC Extract Operations](http://build.fhir.org/ig/HL7/sdc/extraction.html).

Womens Health Registry **SHOULD** support the [SDC Extract Operations](http://build.fhir.org/ig/HL7/sdc/extraction.html) to transform data from QuestionnaireResponse to FHIR Resources in cases where the sender does not create the necessary FHIR Resources.

#### Security Requirements

The Womens Health Registry **SHALL** support the Communication security mechanisms outlined in [FHIR Security Specification](http://hl7.org/fhir/security.html#http)

The Womens Health Registry **SHALL** support the Authentication security mechanisms outlined in [FHIR Security Specification](http://hl7.org/fhir/security.html#authentication)

The Womens Health Registry **SHOULD** support other security recommendations outlined in FHIR Security as appropriate.

---
**Feedback Required**
Should we require the use of SMART on FHIR Backend Services specification for interactions between the External CRN Data Collection System and the Womens Health Registry or leave it open ended until we get more experience using implementations.

---

### EHR or Other Health IT System Conformance Requirements

The following are the conformance requirements for the EHR or Other Health IT System.

#### Behavior and Formats

The EHR or Other Health IT System **SHALL**: 
* Implement the RESTful behavior according to the [FHIR HTTP Specification](http://hl7.org/fhir/http.html).
* Support **json** resource formats for all CRN interactions.
* Declare a CapabilityStatement identifying the list of profiles, operations and search parameters supported.

---
**Implementation Note**
The FHIR HTTP specification outlines specific requirements on how to deal with successful operations, invalid parameters, unauthorized request, insufficient scopes, unknown resources etc.

---
#### Profiles and Interactions

The EHR or Other Health IT System needs to implement the profile specific interactions as specified in the table below.

---
**Implementation Note**
The way to read the table (for example the first row) is as follows

The EHR or Other Health IT System **SHALL** support the READ, SEARCH operations,and MAY support the vREAD, CREATE and HISTORY operations for the US Core profiles.

--- 

| Profile/Resource Name          | create     | read       | search (type level)      | vread          |  history (instance level) |
|:----------------------|-----------:|-----------:|-------------------------:|---------------:|--------------------------:|
|[US Core Profiles - Note1](http://hl7.org/fhir/us/core/index.html)|MAY|SHALL|SHALL|MAY|MAY|

---
**Note1**
US Core profiles are required to be supported by the EHR in order to facilitate the auto population of the CRN instrument.

--- 

#### Search and Other Parameters

The EHR or Other Health IT System needs to implement the search parameters as specified in the table below.


| Profile Name          | SEARCH and Search Result parameters and combinations     |   
|:----------------------|---------------------------------------------------------:|
|[US Core profiles](http://hl7.org/fhir/us/core/index.html)|SHOULD support Search parameters as specified by US Core|


#### Security Requirements

The EHR or Other Health IT System **SHALL** support the Communication security mechanisms outlined in [FHIR Security Specification](http://hl7.org/fhir/security.html#http)

The EHR or Other Health IT System **SHALL** support the Authentication security mechanisms outlined in [FHIR Security Specification](http://hl7.org/fhir/security.html#authentication)

The EHR or Other Health IT System **SHOULD** support other security recommendations outlined in FHIR Security as appropriate.

#### SMART on FHIR App Interactions 

For EHR or Other Health IT Systems supporting the collection of PRO data using External PRO Administration System by passing patient context information the following requirements apply. 

The EHR or Other Health IT System **SHALL** support the **EHR Launch Sequence** from the [SMART on FHIR App Authorization guide](http://docs.smarthealthit.org/authorization) applicable to the EHR.

The EHR or Other Health IT System **SHALL** support information retrieval during **EHR Launch Sequence** using tokens and parameters for [US Core profiles](http://hl7.org/fhir/us/core/index.html)

### GUDID Database Conformance Requirements

The following are the conformance requirements for the GUDID database.

#### Behavior and Formats

The GUDID database **SHALL**: 
* Implement the RESTful behavior according to the [FHIR HTTP Specification](http://hl7.org/fhir/http.html).
* Support **json** resource formats for all CRN interactions.
* Declare a CapabilityStatement identifying the list of profiles, operations and search parameters supported.

---
**Implementation Note**
The FHIR HTTP specification outlines specific requirements on how to deal with successful operations, invalid parameters, unauthorized request, insufficient scopes, unknown resources etc.

---
#### Profiles and Interactions

The GUDID database needs to implement the profile specific interactions as specified in the table below.

---
**Implementation Note**
The way to read the table (for example the first row) is as follows

The GUDID database **SHALL** support the READ, SEARCH operations,and MAY support the vREAD, CREATE and HISTORY operations for the device-crn profile.

--- 

| Profile/Resource Name          | create     | read       | search (type level)      | vread          |  history (instance level) |
|:----------------------|-----------:|-----------:|-------------------------:|---------------:|--------------------------:|
|device-crn profile|MAY|SHALL|SHALL|MAY|MAY|
|devicedefinition-crn profile|MAY|SHALL|SHALL|MAY|MAY|


#### Search and Other Parameters

The GUDID database needs to implement the search parameters as specified in the table below.


| Profile Name          | SEARCH and Search Result parameters and combinations     |   
|:----------------------|---------------------------------------------------------:|
|device-crn|udiCarrier (DI) - SHALL|
|devicedefinition-crn|udiCarrier (DI) - SHALL|


#### Security Requirements

The GUDID database **SHALL** support the Communication security mechanisms outlined in [FHIR Security Specification](http://hl7.org/fhir/security.html#http)

The GUDID database **SHALL** support the Authentication security mechanisms outlined in [FHIR Security Specification](http://hl7.org/fhir/security.html#authentication)

The GUDID database **SHOULD** support other security recommendations outlined in FHIR Security as appropriate.

### Terminology System Conformance Requirements

The following are the conformance requirements for the Terminology System

#### Behavior and Formats

The Terminology System **SHALL**: 
* Implement the RESTful behavior according to the [FHIR HTTP Specification](http://hl7.org/fhir/http.html).
* Support **json** resource formats for all CRN interactions.
* Declare a CapabilityStatement identifying the list of profiles, operations and search parameters supported.

---
**Implementation Note**
The FHIR HTTP specification outlines specific requirements on how to deal with successful operations, invalid parameters, unauthorized request, insufficient scopes, unknown resources etc.

---
#### Profiles and Interactions

The Terminology System **SHALL* support the CodeSystems and ValueSets along with their FHIR operations required for the CRN IG.
 needs to implement the profile specific interactions as specified in the table below.


#### Security Requirements

The Terminology System **SHALL** support the Communication security mechanisms outlined in [FHIR Security Specification](http://hl7.org/fhir/security.html#http)

The Terminology System **SHALL** support the Authentication security mechanisms outlined in [FHIR Security Specification](http://hl7.org/fhir/security.html#authentication)

The Terminology System **SHOULD** support other security recommendations outlined in FHIR Security as appropriate.


<br />
