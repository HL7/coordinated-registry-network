---
title: Mappings and Profiles
layout: default
active: profiles
---

#### Mappings of CDEs to FHIR

The following is a mapping of each of the specific CDE element to its FHIR Resource/profile. The table contains three columns. The first column represents the data element that has been approved via consensus within the WHT CRN project. This is mapped to the specific FHIR Resource and its data elements in the second column. The third column provides a recommendation for pilots to use a specific profile for the project if appropriate or recommends the use of the FHIR Resource directly to experiment and gain more experience before creating and proliferating profiles. 

Note: The mapping provided below along the profile and resource suggestions will be used to auto-populate the Questionnaire (which contains the questions) and/or transform QuestionnaireResponse (which contains the collected data) into first class FHIR resources. 

{% include CDEs_FHIR.html %}


#### Profiles

**US Core Profiles Reuse:** 
The WHT CRN IG re-uses the US-Core profiles identified in the above table to auto-populate Questionnaires and/or transform QuestionnaireResponses to first class FHIR resources.


**SDC profiles Reuse**

The WHT CRN IG re-uses the following profiles from SDC.
SDC profiles are used for collecting observational data related to procedures, conditions and other aspects.

| SDC profile  | Specific Usage for SDC profile               |
:------------------|-----------------------------------------------------------------------------------------:|
| [SDC Questionnaire](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire.html) | Collect observational data |
| [SDC QuestionnaireResponse](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaireresponse.html) |Collect observational data  |
| [SDC Populatable Questionnaire](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire-populate.html)| Questionnaire with information required for auto or pre population |
| [SDC Extractable Questionnaire](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire-extract.html)|Questionnaire with information that can be used to transform answers to FHIR Resources|

**PRO profiles Reuse**

The WHT CRN IG re-uses the following profiles from PRO.
The PRO profiles will be used to administer questionnaires such as QOL, AMSS, FSFI etc.


| PRO profile  | Specific Usage for PRO profile               |
:------------------|-----------------------------------------------------------------------------------------:|
|[SDC Adaptive Questionnaire](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaire-adapt.html)| Collect PRO data (e.g QOL) and score data from patients |
|[SDC Adaptive QuestionnaireResponse](http://build.fhir.org/ig/HL7/sdc/sdc-questionnaireresponse-adapt.html) |Collect PRO (e.g) data and score data from patients. |


**CRN Specific Profiles**

The following are profiles that will be created specifically by CRN to collect Device and Procedure data.



{% include list-profiles.xhtml %}

---
**Feedback Required**

Please provide feedback and comments on the usage of the above listed profiles and their purpose through pilot implementations.

---

<br />



#### Extensions

There are currently no extensions defined for this implementaiton guide since the data elements list is still being finalized.


{% include list-extensions.xhtml %}


{% include link-list.md %}

<br />
