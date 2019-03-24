---
title: Mappings and Profiles
layout: default
active: profiles
---

#### Mappings of CDEs to FHIR

The following is a mapping of each of the specific CDE element to a FHIR Resource/profile. The table contains three columns. The first column represents the data element that has been approved via consensus within the WHT CRN project. This is mapped to a specific FHIR Resource and its data elements in the second column. The third column provides a recommendation for pilots to use a specific profile for the project if appropriate or recommends the use of the FHIR Resource directly to experiment and gain more experience before creating and proliferating profiles. 

Note: The mapping provided below along the profile and resource suggestions will be used to auto-populate the Questionnaire (which contains the questions) and/or transform QuestionnaireResponse (which contains the collected data) into first class FHIR resources. 

{% include CDEs_FHIR.html %}


#### Profiles

**NOTE:** All the profiles listed here are not required for conformance. For detailed conformance requirements please refer to the CapabilityStatements section.


**US Core Profiles Reuse:** 
The WHT CRN IG re-uses the US-Core profiles identified in the above table to auto-populate Questionnaires and/or transform QuestionnaireResponses to first class FHIR resources.


**SDC profiles Reuse**

The WHT CRN IG re-uses the following profiles from SDC.
SDC profiles of Questionnaires and QuestionnaireResponse are used for collecting data related to procedures, conditions and demographic data for WHT CRN purposes. 

| SDC profile  | Specific Usage of SDC profile in WHT CRN              |
:------------------|-----------------------------------------------------------------------------------------:|
| [SDC Questionnaire](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire.html) | Basic data collection questions|
| [SDC QuestionnaireResponse](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaireresponse.html) |Basic data collection storing responses |
| [SDC Populatable Questionnaire](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire-populate.html)| Questionnaire with information required for auto or pre population during data collection|
| [SDC Extractable Questionnaire](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire-extract.html)|Questionnaire with information that can be used to transform answers to FHIR Resources|

**PRO profiles Reuse**

The WHT CRN IG re-uses the following profiles from PRO.
The PRO profiles will be used to administer questionnaires such as QOL, AMSS, FSFI etc.


| PRO profile  | Specific Usage of PRO profile in WHT CRN              |
:------------------|-----------------------------------------------------------------------------------------:|
|[SDC Adaptive Questionnaire](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire-adapt.html)| Collect PRO data (e.g QOL) and score data from patients |
|[SDC Adaptive QuestionnaireResponse](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaireresponse-adapt.html) |Collect PRO (e.g QOL, AMSS, FSFI) data and score collected data. |


**CRN Specific Profiles**

The following are profiles that will be created specifically by CRN to collect Device and Procedure data.



{% include list-profiles.xhtml %}

---
**Feedback Required**

Please provide feedback and comments on the usage of the above profiles and their purpose through pilot implementations.

---

<br />



#### Extensions

There are currently no extensions defined for this implementation guide.


{% include list-extensions.xhtml %}


{% include link-list.md %}

<br />
