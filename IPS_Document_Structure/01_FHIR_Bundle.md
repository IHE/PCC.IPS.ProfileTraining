# FHIR Bundle
1. See http://hl7.org/fhir/bundle.html
2. Review the top level items that are in a FHIR Bundle
  * identifier
  * type
  * timestamp
  * total
  * link
  * entry
3. Open the file [../samples/EU_Giorgio_Cangioli_01.json](../samples/EU_Giorgio_Cangioli_01.json). Note these properties at the top level
  * resourceType (Fixed value)
  * id (sample id)
  * identifier
  * type (Fixed value)
  * timestamp
  * entry
4. Compare the property list to the specification at http://hl7.org/fhir/bundle.html
5. Validate this file as a Bundle using an online tool.
  * https://gazelle.ihe.net/matchbox/#/validate
  * Add file: samples/EU_Giorgio_Cangioli_01.json
  * The application recognizes the resource as a Bundle and generates a report
  * Select the profile: http://hl7.org/fhir/StructureDefinition/Bundle and validate again
  * A new report is generated. This report has one fewer info items than the previous report.
  ![Screenshot](../images/cangioli_01-1.png)
  * Scroll down through the report. It will provide information with line numbers in the original file.

# FHIR Bundle With Dangling Resource
1. Validate this file as a Bundle using the same online tool.
  * https://gazelle.ihe.net/matchbox/#/validate
  * Add file: [../samples/EU_Giorgio_Cangioli_01-a.json](../samples/EU_Giorgio_Cangioli_01-a.json)
  * In this version, we replaced the fullURL of the last Medication resource with a new value (urn:uuid:debc3910-d87c-11ec-9d64-0242ac120002).
  * Make sure you validate as before with the Bundle profile. You get one additional warning:
  : Bundle.entry[9].resource.ofType(MedicationStatement).medication.ofType(Reference):
URN reference is not locally contained within the bundle urn:uuid:9ac3356c-4ea4-4814-84c3-235484f2ef19 
 * That warning matches the change that was made to create samples/EU_Giorgio_Cangioli_01-a.json

## Pages to Read (In Order)
* [FHIR Bundle](01_FHIR_Bundle.md)
* [&rarr; Composition](02_Composition.md)
* [IPS Sections](03_IPS_Sections.md)
* [Header Sections](04_Header_Sections.md)
* [Required Sections](05_Required_Sections.md)
* [Full Resources](06_Full_Resources.md)
* [IPS_Document_Validation/README.md](../IPS_Document_Validation/README.md)