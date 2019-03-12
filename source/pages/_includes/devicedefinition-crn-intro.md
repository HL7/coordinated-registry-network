
{% assign id = {{page.id}} %}
source file: source/pages/\_includes/{{id}}-intro.md

{{site.data.structuredefinitions.[id].description}}

#### Scope and Usage

The profile is to be used for the WTH CRN project to capture the specific device information that is the present in the GUDID database for devices used to treat women with various health conditions.

#### Mandatory Data Elements and Terminology

The following data-elements are mandatory (i.e data MUST be present).

**must have:**

1. manufacturer

**Additional Profile specific implementation guidance:**

When available, the DeviceDefinition data elements manufacturer, deviceName, modelNumber and type should be populated when found in the GUDID database using the deviceIdentifier. 
