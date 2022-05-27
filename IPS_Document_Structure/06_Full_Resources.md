# IPS Full Resources

1. See: https://build.fhir.org/ig/HL7/fhir-ips/ipsStructure.html
2. The data in the Composition reference full resources that are included in the Bundle.
3. Open the file [../samples/EU_Giorgio_Cangioli_01.json](../samples/EU_Giorgio_Cangioli_01.json)
4. Open the file [../samples/sections.xlsx](../samples/sections.xlsx)
 * Sections by Document sheet is a summary across documents
 * EU_Giorgio_Cangioli_01 sheet is specific to that document
5. Go through the rows in the sheet EU_Giorgio_Cangioli_01
 * These correspond to resources in the Bundle
 * See the fullURL for each resource
 * Use that fullURL to find where this resource is referenced. That is, who/what is pointing at this resource?
 * Note that the MedicationStatement resource points a Medication resource.
6. Look at individual resources (AllergyIntolerance, Condition, MedicationStatement) that are defined as part of the IPS.
  * Medication is included because it is referenced by MedicationStatement
  * Each resource (AllergyIntolerance, Condition, MedicationStatement) has its own structure
7. Validate this AllergyIntolerance resource:
 * [../samples/EU_Giorgio_Cangioli_01-AllergyIntolerance.json](../samples/EU_Giorgio_Cangioli_01-AllergyIntolerance.json)
 * You will get one warning
