---
title: Implementation Guidance
layout: default
active: guidance
f: http://build.fhir.org/
---

{:.no_toc}

<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

* Do not remove this line (it will not be displayed)
{:toc}

### Introduction

The implementation guidance outlined in this page provides useful information for developers implementing the various CRN actors and their capabilities. All resources and parameters used in this part of the IG are examples and are expected to conform to the resources, profiles and other constraints outlined in the [CapabilityStatements](capstatements.html).


#### CRN Instrument and Meta data Repository Implementation

​The capabilities and requirements that need to be implemented by the CRN Instrument and Meta data Repository are outlined at Conformance Requirements.

Developers can follow these steps to implement the above capabilities.

**Step 1:** Implement a FHIR Server. (Choose either STU3 or DSTU2)

There are many open source FHIR Servers that are available to be downloaded and used instead of starting from scratch. These can be found at [FHIR Open Source Implementations](http://wiki.hl7.org/index.php?title=Open_Source_FHIR_implementations).

Publish the FHIR Server Capability Statement for the Server.

**Step 2:** Implement the APIs for Questionnaires

* POST API : Support Creation of a CRN instrument using Questionnaire Resource and store it in a repository. 

`POST [BaseURL]/Questionnaire/` - Submit payload (body) of Questionnaire in JSON format.


* GET API : Will be used by an External CRN Data Collection System to download a specific questionnaire.

`GET [BaseURL]/Questionnaire/1234` - Receive a payload (body) of Questionnaire in JSON format.

`GET [BaseURL]/Questionnaire/?_summary` - Receive all Questionnaires present in the system in summary format.

* Search API - Find Specific questionnaires.

`GET [BaseURL]/Questionnaire?_identifier=phq-9` - Receive a phq-9 Questionnaire.


**Step 3:** Implement appropriate security protocols for the Server.

At a minimum, HTTPS protocols must be used for the implementation using the right certificate.


#### External CRN Data Collection System Implementation

​The capabilities and requirements that need to be implemented by the External CRN Data Collection System are outlined at Conformance Requirements.

Developers can follow these steps to implement the above capabilities.

**Step 1:** Implement a FHIR Server. (Choose either STU3 or DSTU2)

There are many open source FHIR Servers that are available to be downloaded and used instead of starting from scratch. These can be found at [FHIR Open Source Implementations](http://wiki.hl7.org/index.php?title=Open_Source_FHIR_implementations).

Publish the FHIR Server Capability Statement for the Server.

**Step 2a:** Implement the APIs for Questionnaires

* POST API : Support creation of CRN instrument using Questionnaire Resource and store it internally for tracking administrations. 

`POST [BaseURL]/Questionnaire/` - Submit payload (body) of Questionnaire in JSON format.

* GET API : Will be used to download a specific Questionnaire by authorized systems and personnel.

`GET [BaseURL]/Questionnaire/1234` - Receive a payload (body) of Questionnaire in JSON format.

`GET [BaseURL]/Questionnaire/?_summary` - Receive all Questionnaires present in the system in summary format.

* Search API - Find Specific questionnaires.

`GET [BaseURL]/Questionnaire?_identifier=phq-9` - Receive a phq-9 Questionnaire.

**Step 2b:** Implement the APIs for QuestionnaireResponse

* POST API : Support collection of CRN data using QuestionnaireResponse Resource and store it internally for tracking administrations. 

`POST [BaseURL]/QuestionnaireResponse/` - Submit payload (body) of QuestionnaireResponse in JSON format.


* GET API : Will be used to download a specific QuestionnaireResponse (CRN data) by authorized systems and personnel.

`GET [BaseURL]/QuestionnaireResponse/1234` - Receive a payload (body) of QuestionnaireResponse in JSON format.

* Search API - Find Specific QuestionnaireResponses.

`GET [BaseURL]/QuestionnaireResponse?patient=1234` - Receive all QuestionnaireResponses for a patient

`GET [BaseURL]/QuestionnaireResponse?questionnaire=1234&authored=gt2017-01-15` - Receive QuestionnaireResponses for a specific questionnaire administered after Jan 15 2017.

**Step 3:** Implement appropriate security protocols for the Server.

At a minimum, HTTPS protocols must be used for the implementation using the right certificate.

**Step 4:** Implement SMART on FHIR Authorization for clients (Only if the External CRN Data Collection System interacts with an EHR)

When the External CRN Data Collection System interacts with an EHR, it has to be registered with the EHRs Authorization Server to enable launching from within the EHR using SMART on FHIR Authorization protocols. After launch, the External CRN Data Collection System must support the query of appropriate resources for context and pre-population using US Core profiles.

To implement the SMART on FHIR Authorization Server and other SMART on FHIR capabilities, refer to [SMART on FHIR Sandbox](https://sandbox.smarthealthit.org).

Once the data is collected, the External CRN Data Collection System may store the CRN data in the EHR using the POST API creating the QuestionnaireResponse.

**Step 5:** Implement GUDID interactions

The External CRN Data Collection System should invoke the GUDID API to retrieve the Device Information using the device-crn and devicedefinition-crn profiles. This will require GUDID database to support getting device information using these FHIR APIs. 

In case these APIs are not available in the GUDID database, then other published APIs may have to be used. 

**Step 6:** Implement Terminology Validations 

The External CRN Data Collection System should invoke the CodeSystem and ValueSet FHIR APIs published by the Terminology System to validate the answers submitted during the data collection process.

**Step 7:** Implement Auto population  

The External CRN Data Collection System should implement the FHIRPath based auto population mechanism if the Questionnaire supports auto population using US Core profiles and retrieving information from an EHR.

**Step 8:** Implement data extraction

The External CRN Data Collection System should implement the FHIRPath based extraction mechanism to create FHIR Resources from the QuestionnaireResponse which was created during data collection.

**Step 9:** Submit data to Womens Health Registry

The External CRN Data Collection System should invoke the POST APIs on the Womens Health Registry to submit the collected data for the patient using QuestionnaireResponse and when available US Core profiles representing other FHIR Resources.

#### Womens Health Registry Implementation

​The capabilities and requirements that need to be implemented by the Womens Health Registry are outlined at Conformance Requirements.

Developers can follow these steps to implement the above capabilities.

**Step 1:** Implement a FHIR Server. (Choose either STU3 or DSTU2)

There are many open source FHIR Servers that are available to be downloaded and used instead of starting from scratch. These can be found at [FHIR Open Source Implementations](http://wiki.hl7.org/index.php?title=Open_Source_FHIR_implementations).

Publish the FHIR Server Capability Statement for the Server.

**Step 2a:** Implement the APIs for Questionnaires

* POST API : Support creation of CRN instrument using Questionnaire Resource and store it internally for tracking administrations. 

`POST [BaseURL]/Questionnaire/` - Submit payload (body) of Questionnaire in JSON format.

* GET API : Will be used to download a specific Questionnaire by authorized systems and personnel.

`GET [BaseURL]/Questionnaire/1234` - Receive a payload (body) of Questionnaire in JSON format.

`GET [BaseURL]/Questionnaire/?_summary` - Receive all Questionnaires present in the system in summary format.

* Search API - Find Specific questionnaires.

`GET [BaseURL]/Questionnaire?_identifier=phq-9` - Receive a phq-9 Questionnaire.

**Step 2b:** Implement the APIs for QuestionnaireResponse

* POST API : Support collection of CRN data using QuestionnaireResponse Resource and store it internally for tracking administrations. 

`POST [BaseURL]/QuestionnaireResponse/` - Submit payload (body) of QuestionnaireResponse in JSON format.


* GET API : Will be used to download a specific QuestionnaireResponse (CRN data) by authorized systems and personnel.

`GET [BaseURL]/QuestionnaireResponse/1234` - Receive a payload (body) of QuestionnaireResponse in JSON format.

* Search API - Find Specific QuestionnaireResponses.

`GET [BaseURL]/QuestionnaireResponse?patient=1234` - Receive all QuestionnaireResponses for a patient

`GET [BaseURL]/QuestionnaireResponse?questionnaire=1234&authored=gt2017-01-15` - Receive QuestionnaireResponses for a specific questionnaire administered after Jan 15 2017.

**Step 3:** Implement appropriate security protocols for the Server.

At a minimum, HTTPS protocols must be used for the implementation using the right certificate.

**Step 4:** Implement Support for US Core profiles.

The Womens Health Registry should support US Core profiles in order to receive granular FHIR Resources representing collected data. For more information on the APIs to be supported refer to the US Core IG.







