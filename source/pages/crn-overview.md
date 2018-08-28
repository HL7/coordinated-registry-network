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

This section outlines the data elements that need to be collected by each of the registries to achieve the specific project goals. 

At the time of creation of this IG, the list of data elements have not been finalized, however an initial list of data elements have been identified by registries dealing with different women's health conditions and therapies and the links to the spreadsheets capturing these data elements are present in the table below. 

**Note: The list of data elements are just a draft and are not final and hence are excluded from the ballot** 

| FDA Clinical Working Group Name  | Initial List of Data Elements Identified for WHT CRN project |
:----------------|-------------------------------------------------------------:|
| Long Acting Reversible Contraceptives (LARC) | [LARC Draft Data Elements](https://drive.google.com/file/d/17h-EFoae123Sfr4YexFsEEM8xzcPRElF/view?usp=sharing)|
| Pelvic Organ Prolapse (POP) | [POP Draft Data Elements](https://drive.google.com/file/d/1Wo0aMvGkfBsamzaO7lBKftkfKZZoDqo5/view?usp=sharing)|
| Uterine Fibroids (UF) | [UF Draft Data Elements](https://drive.google.com/file/d/1TTAgkFzDEcVJbfrYI4fQChjokaYTbYEz/view?usp=sharing)|


#### Next Steps for Data Elements Finalization
 
The initial list of data elements have been identified by each of the registries participating in the WHT CRN project, however additional work will be performed to harmonize these data elements and reach consensus on the final list of data elements that will be used by the project for piloting and real-world adoption as the IG gets finalized for the STU ballot. The final list of data elements will be published by National Library of Medicine (NLM) at [CDE Repository](https://cde.nlm.nih.gov/cde/search) for others to use the data elements as part of their activities. 
 
#### Data Elements and FHIR Profiles, Extensions
 
Once consensus is achieved and a final list of data elements are created for the WHT CRN project, these data elements will be mapped to various existing profiles from US-Core IG which is based on Common Clinical Data Set from ONC 2015 Edition, Structured Data Capture (SDC) IG which provides the framework for using Questionnaire and Questionnaire Response resources to collect data in a structured manner and Patient Reported Outcomes (PRO) FHIR IG which provides the framework on how to use the Questionnaire Resource for capturing Patient Reported Outcome data. 
In cases where the data elements are not directly mappable to any of the existing profiles from the other IGs, new profiles and extensions will be created as necessary. The approach used can be examined in the Profiles tab of the IG.
 
 
###  Abstract Model, Actors and Definitions

This section outlines the abstract model which is used to identify the specific actors and interactions that are in-scope for the PRO FHIR IG. There are two different abstract models to consider and are outlined below

* __Abstract model for administering fixed format (Basic) questionnaires__: In this model the all the items of the questionnaires are administered to the patient unless some of the items have to be skipped based on skip logic or other simple criteria. For e.g A Questionnaire might skip a question on pregnancy if the person is a male.
	 	
* __Abstract model for administering Item Response Theory (IRT) based questionnaires__: This is also known as Computerized Adaptive Testing (CAT), or administration of Adaptive Questionnaires. In this cases a set of questions typically 4 to 12 are administered from a question bank containing a large number of questions. The selected questions is based on Item Response Theory algorithms which look at the answers provided and select the next question based on IRT algorithms. The selection of questions will help in obtaining responses for a few questions and finish the administration. These small set of questions still provide the necessary confidence and scores required to interpret the data appropriately as if the whole questionnaire was administered. 
	
	
#### Abstract Model for administering Basic (fixed format) Questionnaires

Figure 2 below shows the abstract model, actors and the data flows for the administration of Basic Questionnaires. The actors and their interactions are outlined in the next few paragraphs.

 {% include img.html img="pro-abstract-model-basic.png" caption="Figure 2: Abstract Model for Basic Questionnaires " %}
 
**PROM Instrument and Meta data Repository**: The PROM Instrument and Meta data Repository is a system that is capable of storing the PROMs along with its meta data. In addition to storing the PROMs, the repository provides APIs to health IT systems to retrieve PROMs for administration. The repository may be hosted by an organization (e.g PCORnet CDRN such as REACHnet, pSCANNER) individually or can be hosted centrally by a federal agency (e.g NIH) or a network such as Common Well or an independent organization providing PRO services (e.g Northwestern).

**EHR or Care Delivery Health IT System**: In the context of PRO work flows, EHR or Care Delivery Health IT Systems are used by providers to deliver care and can capture and store the health information about the patient. These EHR or Care Delivery systems can be used to administer PROs to patient as part of routine care. These EHRs or Care Delivery systems will render the PRO instrument natively, capture the PRO data and then persist the captured PRO data within the system.

**External PRO Administration System**: In the context of PRO work flows, External PRO Administration Systems are those which are considered to be independent and external to the EHR or Care Delivery Health IT system. There are many different variations of these systems. Some examples include independent health IT systems which have no connection to an EHR (e.g Tablets with PRO modules used to collect PRO data and have their own databases to store the data), a SMART on FHIR App which can be launched from an EHR with the patient context and communicate with the EHR is used to collect and store PRO data. The key aspect of these external PRO systems is the fact that they are outside the clinical care delivery system (i.e EHR) and hence will need a mechanism to integrate with the EHR for the PRO data to be useful widely.

**Data Flow Descriptions**
As shown in the Figure 2 above, there are multiple ways a PROM can be administered in the real-world. We will examine these different work flows in the next few paragraphs.

__PROM Administration using EHR or Care Delivery Health IT System (Identified as DF1 in Abstract Model)__ All PROM administration activities start with the creation and publishing of the instrument along with the meta data necessary for administration which is shown in Step 1 of the diagram. When the PROM is administered using an EHR or Care Delivery system natively, the PROM is retrieved by the EHR as shown in step 2. (The context of which patient should be administered a PROM is part of the PROM Administration and Planning activity and is not shown as part of the abstract model) Once the PROM is retrieved and rendered the patient will fill out the PROM (the actual user interface may be a tablet or web interface or a patient portal etc) and the responses are collected and scored as shown in Step 3. The collected PRO data is then made available to Providers, Care givers and Researchers as part of Step 6 and 7. The APIs to be used by providers and researchers to access the PRO data will be specified in the IG , however the required security and privacy controls and user interfaces to be used to access the PRO data are not defined as part of the abstract model.

__PROM Administration using External PRO Administration System (Identified as DF2 in Abstract Model)__ All PROM administration activities start with the creation and publishing of the instrument along with meta data necessary for administration which is shown in Step 1 of the diagram. When a PROM is administered using an External PRO Administration System, the PROM is retrieved as shown in step 2a. (The context of which patient should be administered a PROM is part of the PROM Administration and Planning activity and is not shown as part of the abstract model). Once the PROM is retrieved and rendered the patient will fill out the PROM (the actual user interface may be a tablet or web interface or a mobile app) and the responses are collected and scored as shown in Step 3a. If the collected PRO data is to be persisted in an EHR, then the PRO data will be submitted to the EHR via a message or an API as shown in Step 5. The collected PRO data will be made available to Researchers as part of Step 7. The APIs to be used by providers and researchers to access the PRO data will be specified in the IG , however the required security and privacy controls and user interfaces to be used to access the PRO data are not defined as part of the abstract model.

__PROM Administration using SMART on FHIR App (Identified as DF3 in Abstract Model)__ All PROM administration activities start with the creation and publishing of the instrument along with meta data necessary for administration which is shown in Step 1 of the diagram. When a PROM is administered using an External PRO Administration System which is coupled to an EHR or Care Delivery system such as a SMART on FHIR App, the provider has to launch the SMART on FHIR App with the user context as shown in Step 4. Once the app is launched with the appropriate permissions, the PROM is retrieved as shown in step 2a. (The context of which patient should be administered a PROM is part of the PROM Administration and Planning activity and is not shown as part of the abstract model). Once the PROM is retrieved and rendered the patient will fill out the PROM (the actual user interface may be a tablet or web interface or a mobile app) and the responses are collected and scored as shown in Step 3a. The collected PRO data is then persisted in the EHR, using APIs as shown in Step 5. The collected PRO data will be made available to Providers, Care givers and Researchers as part of Steps 6 and 7. The APIs to be used by providers and researchers to access the PRO data will be specified in the IG , however the required security and privacy controls and user interfaces to be used to access the PRO data are not defined as part of the abstract model.
	

#### Abstract Model for administering IRT based (Adaptive or CAT) Questionnaires

Figure 3 below shows the abstract model, actors and the data flows for the administration of Basic Questionnaires. The actors and their interactions are outlined in the next few paragraphs.

{% include img.html img="pro-abstract-model-adaptive.png" caption="Figure 3: Abstract Model for Adaptive Questionnaires " %}
 
**External Assessment Center**: The External Assessment Center is a system that is capable of administering a questionnaire based on IRT algorithms. The data that is necessary for the administration is only the initial item bank. The External Assessment Center does not need to know about the specific patient identity or any other clinical information. The Assessment Center will use alogorithms recommended by the Questionnaire designer to determine how to administer the questionnaire.

**Patient Facing Administration App**: The Patient Facing Administration App is the actual app that is being used to present the questions to the patient. It can be an EHR, a SMART on FHIR App, an Independent PRO Administration App. 


**Data Flow Description for Adaptive Questionnaires Administration**

As shown in Figure 3 above, the Patient Facing Administration App (EHR, Care Delivery System, Independent App or SMART on FHIR App) acts as the client and initiates the administration process. In the first step, the available adaptive questionnaires are discovered and a specific PROM is selected for administration. (Note: this step is optional) The following are the steps that take place in the interaction.
* The administration is initiated with a specific PROM.
* The Assessment Center responds to the start request with a Questionnaire and the first item for administration.
* The Patient Facing Administration App will then display the question to the user and collect the response.
* The Patient Facing Administration App will then send the answer to the Assessment Center and ask for the next question.
* The Assessment Center will use the answer to determine the next question based on the algorithm and respond back with the next question until the assessment is done.
* If the Assessment Center determines that the assessment is done, it will respond with the final results which will contain all the questions that were answered, along with the answers, the individual scores and the overall score.



<!-- {% raw %}>{% include link-list.md %} {% endraw %}-->

{% include link-list.md %}
