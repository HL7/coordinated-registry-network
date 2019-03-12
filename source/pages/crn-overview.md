---
title: WHT CRN Overview
layout: default
active: overview
---

{% include publish-box.html %}


<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

* Do not remove this line (it will not be displayed)
{:toc}


<!-- end TOC -->



###  Background

Clinical data registries serve as a repository that maintains various health data on a patient and the healthcare they receive over a period of time. A clinical data registry can focus on a disease or condition, a procedure or even track performance of medical devices used to improve patients’ health. Capturing a holistic picture of a patients’ clinical data in a registry will enable researchers and clinicians to evaluate patient outcomes and quality improvement. In addition, the infrastructure can also provide a basis for post market surveillance of medical devices  and for the development of evidence to support medical device innovation. Finally, the collected, curated data sets, methods, and tools developed can also be used for regulatory purposes, quality benchmarking, coverage decisions, patient-centered outcomes research (PCOR), and other uses.
However, one of the many challenges with single purpose registries are that they prove too often to be time and cost-intensive, not only for the organizations that collect, manage and analyze the datasets, but also for the hospitals and medical practices that participate in providing data.  In addition, existing patient-centered outcomes research often relies on data captured at the point of care, re-entered into clinical research systems, and then consolidated and transformed for the analysis and research purposes, which is a very complex process. This process is labor-intensive and expensive, as it requires extensive data validation and normalization to assure accurate and effective evaluation. As a result, study designs are often limited to the effects of one particular therapy (i.e., medication or device), rather than a combination of two or more therapies as would exist in the real world. Therefore, having a coordinated network of registries would benefit in improving patient-centered outcomes research where data from multiple registries can be leveraged for multiple use cases, assuming the necessary data elements are already being collected. In order to accomplish the objective of establishing a coordinated registry network, the Women’s Health Technologies (WHT) Coordinated Registry Network (CRN)  project was funded by the Patient-Centered Outcomes Research Trust Fund (PCORTF),  under the Assistant Secretary for Planning and Evaluation (ASPE), part of the U.S. Department of Health and Human Services (HHS).
 


###  Purpose and Goals of the Project

The purpose of the WHT CRN project is to create a strategically coordinated registry network for women’s health technologies that will collect patient reported outcomes and other related clinical data from care delivery systems including electronic health records (EHRs) to both enhance existing registries and enrich PCOR data infrastructure pertinent to women’s health conditions. The WHT CRN project is a multi-agency project that includes clinical and informatics experts from the Food and Drug Administration (FDA), the National Institutes of Health (NIH)/National Library of Medicine (NLM), the Office of the National Coordinator for Health Information Technology (ONC), the Agency for Healthcare Research and Quality (AHRQ) and the Medical Device Epidemiology Network Initiative (MDEpiNet),  part of the Epidemiology Research Program (ERP) at the FDA's Center for Devices and Radiological Health (CDRH). 

The WHT CRN project focuses on women’s health as there are many clinical conditions that uniquely affect women (e.g., pelvic floor disorders, uterine fibroids, and female sterilization). The project aims to create a set of linked registries focused on women’s health using data elements and measures expressed in standard structured definitions with the capability to capture and exchange data using the national standards. Usage of national standards will  support interoperability with other data sources via software apps and application programming interfaces (APIs), including those related to a unique device identifier (UDI). These linked registries would be valuable to researchers to design studies that are reflective of the real-world combination of multiple therapies. Additionally, since the original Centers for Disease Control and Prevention’s (CDC) Collaborative Review of Sterilization (CREST) study conducted several decades ago, there has not been a systematic national effort to generate evidence across various sterilization technologies, and, the recent safety concerns have also prompted the FDA to mandate a study of hysteroscopic female contraceptive devices. Manufacturers’ ongoing efforts to address public health questions can greatly benefit from a national registry infrastructure to ensure proper comparison groups. The FDA envisions the WHT CRN project as a way to coordinate and use the findings from this project to inform other CRNs within the FDA’s Center for Devices and Radiological Health (CDRH) Informatics group and to build upon the National Evaluation System for health Technology (NEST)  to “more efficiently generate better evidence for medical device evaluation and regulatory decision-making.” 

The specific goals of the WHT CRN project include:
* Help establish a strategically coordinated registry network (CRN) for women’s health technologies and develop tools to facilitate collection of data within the existing and new registries by leveraging clinical care data.
* Demonstrate that data in these registries can be used to do the following:
    * Evaluate the effectiveness, quality of life and safety associated with differing treatment options,
    * Assess the effectiveness and quality of life associated with varying treatment options,
    * Provide a framework for clinical studies to be conducted within the registry, including industry-sponsored studies for pre-market and post-market regulatory activities, and,
    * Allow healthcare providers to track surgeon volume, patient outcomes, and quality measures for quality improvement activities and fulfill upcoming Centers for Medicaid and Medicare Services (CMS), Physician Quality and Reporting Systems (PQRS) and maintenance of certification requirements.


###  WHT CRN Project Data Elements

This section outlines the data elements that will be collected by each of the registries to achieve the specific project goals. 

The data element list is called as the [Common Data Elements](https://drive.google.com/file/d/1GGRZOJcLBAW_p_czcfaSe7xAirs8KPw6/view?usp=sharing) (CDEs) for the CRN project. The list of data elements may change as the project progresses, pilots are completed and new use cases are added, however the above spreadsheet is the consensus approved CDE list for the project.

**Note: The list of data elements were curated by NLM working with the various registries and FDA Clinical Working Groups. The below table contains data element lists provided by different working groups which helped in creating the final CDE list.** 

| FDA Clinical Working Group Name  | Initial List of Data Elements Identified for WHT CRN project |
:----------------|-------------------------------------------------------------:|
| Long Acting Reversible Contraceptives (LARC) | [LARC Draft Data Elements](https://drive.google.com/file/d/17h-EFoae123Sfr4YexFsEEM8xzcPRElF/view?usp=sharing)|
| Pelvic Organ Prolapse (POP) | [POP Draft Data Elements](https://drive.google.com/file/d/1Wo0aMvGkfBsamzaO7lBKftkfKZZoDqo5/view?usp=sharing)|
| Uterine Fibroids (UF) | [UF Draft Data Elements](https://drive.google.com/file/d/1TTAgkFzDEcVJbfrYI4fQChjokaYTbYEz/view?usp=sharing)|


#### NLM's CDE Repository
 
The [Common Data Elements](https://drive.google.com/file/d/1GGRZOJcLBAW_p_czcfaSe7xAirs8KPw6/view?usp=sharing) 
The data elements are published by National Library of Medicine (NLM) at [CDE Repository](https://cde.nlm.nih.gov/cde/search) for others to use the data elements as part of their activities. The CDEs can also be accessed as Questionnaire Resource at the NLM's [Questionnaire Representation of CDE](https://cde.nlm.nih.gov/formView?tinyId=XJwYSNJ4I).
 
#### Data Elements and FHIR Profiles, Extensions
 
The CDEs are mapped to various existing profiles from US-Core IG which is based on Common Clinical Data Set from ONC 2015 Edition, Structured Data Capture (SDC) IG which provides the framework for using Questionnaire and Questionnaire Response resources to collect data in a structured manner and Patient Reported Outcomes (PRO) FHIR IG which provides the framework on how to use the Questionnaire Resource for capturing Patient Reported Outcome data. 
In cases where the data elements are not directly mappable to any of the existing profiles from the other IGs, new profiles and extensions are created as necessary. The results of the mapping can be found in the profiles tab of the implementation guide.
 
 
###  Abstract Model, Actors and Definitions

This section outlines the abstract model which is used to identify the specific actors and interactions that are in-scope for the WHT CRN IG. There are two different abstract models to consider and are outlined below

* __Abstract model for collecting WHT CRN data__: In this model, the focus is on the data collection from patients undergoing various treatments of interest using a combination of clinical care delivery systems like EHRs and independent apps to collect specific CRN data elements.
	 	
* __Abstract model for accessing collected data from Womens Health Registries__: In this model, the focus is on the ability of researchers to access the data already collected and persisted in the registries.
	
	
#### Abstract Model for collecting WHT CRN data 

Figure 1 below shows the abstract model, actors and the data flow for WHT CRN data collection. The actors and their interactions are outlined in the next few paragraphs.

 {% include img.html img="crn-abstract-model-datacollection.png" caption="Figure 1: Abstract Model for WHT CRN Data Collection " %}
 
**CRN Instrument**: The CRN Instrument is essentially a form or a questionnaire that is used to collect data from patients. The instrument is designed based on data that needs to be collected using the data element definitions previously described. In the WHT CRN IG, the CRN Instrument is also referred to as the CRN Form and CRN Questionnaires interchangeably.
 
**CRN Instrument and Meta data Repository**: The CRN Instrument and Meta data Repository is a system that is capable of storing the CRN Instruments along with its meta data. In addition to storing the CRN Instruments, the repository provides APIs to health IT systems to retrieve the instruments for administration. The repository may be hosted by an organization (e.g Specific Registry) individually or can be hosted centrally by a federal agency (e.g NIH/NLM) or a network such as Common Well or an independent organization providing CRN services.

**EHR or Other Health IT System**: In the context of CRN work flows, EHR or Other Health IT Systems are used by providers to deliver care and can capture and store the health information about the patient which is relevant for the WHT CRN project. These EHR or Other Health IT systems can also be used to administer CRN Instruments to patient as part of routine care.

**External CRN Data Collection System**: In the context of CRN work flows, External CRN Data Collection Systems are those which are considered to be independent and external to the EHR or Other Health IT system used for care delivery. There are many different variations of these systems. Some examples include independent health IT systems which have no connection to an EHR (e.g Tablets with CRN modules used to collect CRN data and have their own databases to store the data), a SMART on FHIR App which can be launched from an EHR with the patient context and communicate with the EHR is used to collect and store CRN data. The key aspect of these external CRN data collection systems is the fact that they are outside the clinical care delivery system (i.e EHR) and hence will need a mechanism to integrate with the EHR for the CRN data to be useful widely.

**Womens Health Registry**: In the context of CRN work flows, Womens Health Registry is the system that collects the data relevant to specific conditions related to women's health and makes the data available to researchers and authorized federal agencies for studies.

**GUDID Database**: The Global Unique Device Identification Database (GUDID) is a database administered by the FDA that serves as a reference catalog for every device with an identifier. Under the FDA UDI rule, the labeler of each medical device labeled with a unique device identifier (UDI) must submit information concerning that device to the GUDID, unless subject to an exception or alternative.
According to the UDI rule, “The labeler is the person who causes a label to be applied to a device, or who causes the label to be modified, with the intent that the device will be introduced into interstate commerce without any subsequent replacement or modification of the label; in most instances, the labeler would be the device manufacturer, but the labeler may be a specification developer, a single-use device reprocessor, a convenience kit assembler, a repackager, or a relabeler.”
The GUDID is being populated with data about devices according to the compliance timeline published in conjunction with the UDI rule. The GUDID contains ONLY the device identifier (DI), which serves as the primary key to obtain device information in the database. Production Identifiers (PIs) are not submitted to or stored in the GUDID, but the GUDID contains PI flags to indicate which PI attributes are on the device label.
 
In the context of the CRN workflows, data from the GUDID database will be used to populate fields in the CRN Instrument being used for data collection. 

The APIs to be used for accessing the GUDID can be found at [GUDID Database APIs](https://accessgudid.nlm.nih.gov/resources/home). 

**Terminology APIs**: In the context of CRN work flows, Terminology APIs provide CodeSystems and ValueSets to be used in conjunction with the CRN Instrument so that data being collected can be validated in real-time to avoid errors, and collect codified data that is ready for machine processing and analysis.

**Data Flow Description**
As shown in the Figure 1 above, the data flow is as follows

* Step 1: An organization creates the CRN Instrument along with its meta data and publishes the instrument in the CRN Instrument and Meta data repository. 
* Step 2: In Step 2, a provider or a care giver launches the External CRN Data Collection System (App) from within the context of an EHR or Other care delivery Health IT system. This step is optional when there is no EHR or Other Health IT system connected to the External CRN Data Collection System. 
* Step 3: The External CRN Data Collection System access the CRN Instrument from the CRN Instrument and Meta data Repository and renders the instrument for data collection.
* Step 4a: In this step, the External CRN Data Collection System may optionally pre populate fields in the form using data from the EHR.
*  Step 4b: In this step, the provider or care giver or patient enters additional data required to be filled out in the instrument. 
* Step 4c: In this step, the External CRN Data Collection System using the GUDID database to pull any device related information that is relevant and can be used for populating details in the form based on the UDI information entered.
* Step 4d: In this step, the External CRN Data Collection System uses the Terminology API to validate data that is entered into the form where appropriate using terminologies relevant to the instrument.
* Step 5: In this step, the External CRN Data Collection System sends the information collected to the Women's Health Registry as needed.  


#### Abstract Model for accessing collected data from Womens Health Registries

Figure 2 below shows the abstract model, actors and the data flow accessing the collected data from registries. The actors and their interactions are outlined in the next few paragraphs.

{% include img.html img="crn-abstract-model-data-access.png" caption="Figure 2: Abstract Model for WHT CRN data access " %}

The following are the additional actors that are part of the abstract model for data access.
 
**Researcher Portal**: The Researcher Portal is a system that can be used by authorized researchers and other personnel to compose queries and submit queries to the various registries that contain womens health data. Once the data is received the Researcher Portal provides user interfaces for the researchers to view, download and analyze the data received. 

**Data Partner Client**: Data Partner Client is specific software module that is instantiated for each Women's Health Registry so that it can coordinate with the Researcher Portal and download the queries that needs to be executed, execute the queries on the registry infrastructure and compile the results and submit the results back to the Researcher Portal.  


**Data Flow Description**
As shown in Figure 2 above, the data flow is as follows

* Step 6: In this step, a researcher or an authorized user will compose a query to access data from the registry and submit the query for distribution to the various registries. As part of the query composition, the data element definitions could be used to create a query. 
* Step 7: In Step 7, the Data Partner Client will collaborate with the Researcher Portal to download the queries that are intended for its registry and queue them for execution.
* Step 8: The Data Partner Client will collaborate withe local administrators and systems to execut the query.
* Step 9: In this step, the Data Partner Client will compile the query results and submit it back to the Researcher Portal.
*  Step 10: In this step, the researcher or authorized user will access the data retrieved based on the query submitted. 

All of the interactions outlined above are published and discussed in more detail in [Data Access Framework (DAF) Research](http://hl7.org/fhir/us/daf-research/index.html) Implementation Guide.

### Relationship between CRN, Structured Data Capture (SDC), US Core, Patient Reported Outcomes (PRO) and DAF-Research IGs

The WHT CRN project's vast scope requires multiple modules with various capabilities to create the necessary infrastructure. These modules and their specifications can be created newly as part of the WHT CRN project or we can evaluate similar modules that already exist and evaluate their effectiveness in meeting the use cases requirements of the WHT CRN project.

In this section we outline the purpose of the different IG's and how they can be leveraged to implement the required CRN capabilities. 

**CRN and US Core**: 
The [US Core Implementation Guide](http://hl7.org/fhir/us/core/index.html) is based on the ONC 2015 Edition Common Clinical Data Set (CCDS) requirements and **contains profiles that are used to access** the 2015 Edition data elements that are already captured by clinical care delivery systems such as EHRs. The US Core profiles have broad adoption in the real-world compartively due to the Argonaut project (consisting of multiple EHR vendors) and the ONC 2015 Edition API certification requirements. 

As part of the WHT CRN project, when the data elements required to be captured overlap with the ONC 2015 Edition CCDS, the US Core profiles and their existing data element definitions should be considered due to their broad adoption in the real-world. Additionally, if the CRN systems can interface with the EHR or Care Delivery Systems capturing the CCDS data, then the WHT CRN project should consider auto-populating the instruments with data already collected to reduce the burden on the providers and care givers.

**CRN and SDC** 
The [SDC IG](http://build.fhir.org/ig/HL7/sdc/index.html) provides a framework to use the Questionnaire and QuestionnaireResponse FHIR Resources for multiple use cases. The capabilities described in the SDC IG include 
* Ability to create instruments for real-world in an interoperable manner.
* Ability to specify display and rendering requirements for instruments
* Ability to pre-populate instruments from existing clinical data
* Ability to convert data collected into FHIR Resources
* Ability to administer Adaptive Questionnaires or instruments. 
* Associating Instruments with Research protocols and Studies.

The WHT CRN project requires many of these capabilities for real-world implementation and hence WHT CRN IG will reuse the SDC IG capabilities before re-creating similar capabilities from scratch. 

**CRN and PRO** 
The [PRO IG](http://build.fhir.org/ig/HL7/patient-reported-outcomes/index.html) provides a framework to use the Questionnaire and QuestionnaireResponse FHIR Resources for administering Patient Reported Outcome Measures and score the collected responses. Administering PRO Measures and capturing their data is an integral part of CRN requirements. 

When PRO Measures need to be administered for CRN purposes, the CRN IG will reuse these capabilities from the PRO IG.

**CRN and DAF-Research** 
The [DAF-Research](http://hl7.org/fhir/us/daf-research/index.html) provides a framework for researchers to access data from multiple data sources by composing queries and submitting these queries for data extraction, monitoring the status of these queries and retrieving results for the various submitted queries. 

When the CRN project requires these data access capabilities, the CRN IG will reuse the capabilities from the DAF-Research IG.


<!-- {% raw %}>{% include link-list.md %} {% endraw %}-->

{% include link-list.md %}
