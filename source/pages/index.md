---
title: Women's Health Technologies (WHT) Coordinated Registry Network (CRN) FHIR Implementation Guide
layout: default
active: home
---

{% include publish-box.html %}


<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

* Do not remove this line (it will not be displayed)
{:toc}


<!-- end TOC -->



###  Introduction

The Women's Health Technologies (WHT) Coordinated Registry Network (CRN) FHIR Implementation Guide (IG) will focus on capturing and exchanging data related to women's health. The data that is captured will be made available to both providers and authorized researchers. While the CRN FHIR IG can be applied to multiple use cases, the current requirements have been drawn from [PCORnet] use cases and implementations. The capabilities described as part of the IG are intended to be leveraged to build US data infrastructure for a Learning Health System (LHS).

CRN FHIR IG will leverage the US-Core IG and profiles for the resources that overlap with US-Core. CRN FHIR IG will also leverage the Structured Data Capture (SDC) FHIR IG. In addition the IG will create profiles and extensions necessary for CRN purposes which do not exist in US-Core and SDC FHIR IG.

The next section provides a road map for the reader to walk through the implementation guide.

###  Guidance to the readers

The following table will provide a road map to the reader to follow and absorb the content of the implementation guide.

| Topic to Read  | What it Contains and its relationship to CRN IG | Where can I find the content ? |
|:---------------|:------------------------------------------------|-------------------------------:|
| US Core Definitions | The set of definitions applicable to the CRN FHIR IG. (For e.g Definition of“Supported”).| [US-Core Definitions](http://hl7.org/fhir/us/core/STU1//guidance.html)|
| SDC IG | The artifact provides the framework to use questionnaires for multiple use cases.| [SDC](http://hl7.org/fhir/us/core/sdc/index.html)|
| CRN Overview | The artifact provides background on Coordinated Registry Network project.| [CRN Overview](crn-overview.html)|
| Profiles | The artifact defines the various profiles, extensions and resources that make up the CRN FHIR IG.| [Profiles](./guidance.html)|
| Capability Statements | The artifact defines the various capability statements (implementation requirements) for each CRN actor that make up the PRO FHIR IG.| [Capability Statements](./guidance.html)|
| Implementation Guidance | The artifact contains guidance and examples that will help implementers of CRN FHIR IG.| [Implementation Guidance](guidance.html)|




<!-- {% raw %}>{% include link-list.md %} {% endraw %}-->

{% include link-list.md %}
