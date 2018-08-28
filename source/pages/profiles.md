---
title: Profiles defined as part of this Guide
layout: default
active: profiles
---
#### Profiles

**US Core Profiles Reuse:** 
The WHT CRN IG re-uses the following profiles from US-Core.

**Note:** Since the data elements are not finalized yet, we are starting with US Core profiles as needed for the specific resources.As new data elements get finalized and are required for WHT CRN project in addition to data elements already present in US Core, then new profiles for CRN project will be created. The table below lists example data elements that are being considered for each US Core profile that is relevant to WHT CRN project. For a comprehensive list of date elements being considered to be added on top of US Core please refer to the data element spreadsheets documented as part of the [CRN Overview](crn-overview.html).

| US-Core profile  | Example Data Elements that are in addition to US-Core being considered                   |
:------------------|-----------------------------------------------------------------------------------------:|
| [US Core Allergy Intolerance Profile](http://hl7.org/fhir/us/core/StructureDefinition-us-core-allergyintolerance.html) | None|
| [US Core Condition (a.k.a Problem) Profile](http://hl7.org/fhir/us/core/StructureDefinition-us-core-condition.html) |Bodysite, Manifestation, symptoms, Age |
| [US Core Diagnostic Report Profile](http://hl7.org/fhir/us/core/StructureDefinition-us-core-diagnosticreport.html) | Based on, Specimen|
| [US Core Immunization Profile](http://hl7.org/fhir/us/core/StructureDefinition-us-core-immunization.html) | None|
| [US Core Location Profile](http://hl7.org/fhir/us/core/StructureDefinition-us-core-location.html) | None|
| [US Core Medication Profile](http://hl7.org/fhir/us/core/StructureDefinition-us-core-medication.html) | None|
| [US Core MedicationRequest Profile](http://hl7.org/fhir/us/core/StructureDefinition-us-core-medicationrequest.html) | None|
| [US Core MedicationStatement Profile](http://hl7.org/fhir/us/core/StructureDefinition-us-core-medicationstatement.html) | None|
| [US Core Practitioner Profile](http://hl7.org/fhir/us/core/StructureDefinition-us-core-practitioner.html)| None|
| [US Core Results Profile](http://hl7.org/fhir/us/core/StructureDefinition-us-core-observationresults.html) |Age of patient when observation was recorded, device information |
| [US Core Smoking Status Profile](http://hl7.org/fhir/us/core/StructureDefinition-us-core-smokingstatus.html) |Age of patient|
| [US Core Organization Profile](http://hl7.org/fhir/us/core/StructureDefinition-us-core-organization.html) | None|
| [US Core Patient Profile](http://hl7.org/fhir/us/core/StructureDefinition-us-core-patient.html) | Address, Marital Status, Contact Information |
| [Vital Signs from FHIR Core](http://hl7.org/fhir/us/core/us-core-vitalsigns.html) | None |


**SDC profiles Reuse**

The WHT CRN IG re-uses the following profiles from SDC.
SDC profiles are used for collecting observational data related to procedures, conditions and other aspects.

| SDC profile  | Specific Usage for SDC profile               |
:------------------|-----------------------------------------------------------------------------------------:|
| [Questionnaire Profile](http://hl7.org/fhir/us/sdc/sdc-questionnaire.html) | Collect observational data |
| [QuestionnaireResponse Profile](http://hl7.org/fhir/us/sdc/sdc-questionnaireresponse.html) |Collect observational data  |


**PRO profiles Reuse**

The WHT CRN IG re-uses the following profiles from PRO.
The PRO profiles will be used to administer questionnaires such as QOL, AMSS, FSFI etc.


| PRO profile  | Specific Usage for PRO profile               |
:------------------|-----------------------------------------------------------------------------------------:|
| [Questionnaire Profile](http://hl7.org/fhir/us/sdc/sdc-questionnaire.html) | Collect PRO data (e.g QOL) and score data from patients |
| [QuestionnaireResponse Profile](http://hl7.org/fhir/us/sdc/sdc-questionnaireresponse.html) |Collect PRO (e.g) data and score data from patients. |


**CRN Specific Profiles**

The following are profiles that will be created specifically by CRN to collect Device and Procedure data.



{% include list-profiles.xhtml %}

<br />

#### Extensions

There are currently no extensions defined for this implementaiton guide since the data elements list is still being finalized.


{% include list-extensions.xhtml %}


{% include link-list.md %}

<br />
