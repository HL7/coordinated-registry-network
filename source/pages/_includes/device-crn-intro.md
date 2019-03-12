
{% assign id = {{page.id}} %}
source file: source/pages/\_includes/{{id}}-intro.md

{{site.data.structuredefinitions.[id].description}}

#### Scope and Usage

The profile is to be used for the WTH CRN project to capture the specific device information used to treat women with various health conditions.

#### Mandatory Data Elements and Terminology

The following data-elements are mandatory (i.e data MUST be present).

**must have:**

1. identifier
1. patient

**Additional Profile specific implementation guidance:**

The udiCarrier can only contain either carrierAIDC or carrierHRF along with its appropriate entryType.
In case an organization wants to represent both carrierAIDC or carrierHRF, then multiple udiCarrier entries must be used.
Also refer to the invariants present on the various data elements in the profile.
