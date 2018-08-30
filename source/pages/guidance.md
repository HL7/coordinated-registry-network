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

The implementation guidance outlined in this page provides useful information for developers implementing the various CRN actors and their capabilities.

#### CRN Instrument and Meta data Repository Implementation

​The capabilities and requirements that need to be implemented by the CRN Instrument and Meta data Repository are outlined at Conformance Requirements.

Developers can follow these steps to implement the above capabilities.

**Step 1:** Implement a FHIR Server. (Choose either STU3 or DSTU2)

There are many open source FHIR Servers that are available to be downloaded and used instead of starting from scratch. These can be found at FHIR Open Source Implementations.

Publish the FHIR Server Capability Statement for the Server.

**Step 2:** Implement the APIs for Questionnaires

Depending on the implementation of the FHIR Server, the Questionnaire Resource has to be implemented and the following APIs have to be exposed.

* POST API
* GET API
* Search API.

**Step 3:** Implement appropriate security protocols for the Server.

At a minimum, HTTPS protocols must be used for the implementation using the right certificate.

#### External CRN Data Collection System Implementation
​The capabilities and requirements that need to be implemented by the External CRN Data Collection System are outlined at Conformance Requirements.

Developers can follow these steps to implement the above capabilities.

**Step 1:** Implement a FHIR Server. (Choose either STU3 or DSTU2)

There are many open source FHIR Servers that are available to be downloaded and used instead of starting from scratch. These can be found at FHIR Open Source Implementations

Publish the FHIR Server Capability Statement for the Server.

**Step 2:** Implement the APIs

Questionnaire APIs The following APIs must be implemented by the External CRN Data Collection System.

* GET API to retrieve a Questionnaire from the Repository.
* POST API to create a Questionnaire Resource internally for linking and tracking.
* Search API to search for Questionnaires stored within the system.

QuestionnaireResponse APIs The following APIs must be implemented by the External CRN Data Collection System.

* GET API to retrieve a QuestionnaireResponse from EHRs.
* POST API to create a QuestionnaireResponse Resource for storing collected data.
* Search API to search for QuestionnaireResponse within the EHR system.

**Step 3:** Implement appropriate security protocols for the Server.

At a minimum, HTTPS protocols must be used for the implementation using the right certificate.

**Step 4:** Implement SMART on FHIR Authorization Client (Only if the External CRN Data Collection System interacts with EHR)

When the External CRN Data Collection System supports integration with an EHR, the External CRN Data Collection System must implement the Client capabilities per SMART on FHIR Specifications, so that the external app can be launched with the patient context and after collecting the CRN data, the QuestionnaireResponse can be submitted to the EHR system.

To implement the SMART on FHIR Authorization Server and other SMART on FHIR capabilities, refer to SMART on FHIR Sandbox.

