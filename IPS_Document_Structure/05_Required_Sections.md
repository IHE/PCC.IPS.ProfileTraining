# IPS Required Sections

1. See: https://build.fhir.org/ig/HL7/fhir-ips/ipsStructure.html
2. List of required sections

|  Category    |  Section                     |
|--------------|------------------------------|
| Required     | Medication Summary           |
| Required     | Allergies and Intolerances   |
| Required     | Problem List                 |

3. Open the file samples/EU_Giorgio_Cangioli_01.json
4. In the Composition.section array, locate these:
 * Allergies and Intolerances
 * Problem List
 * Medication List
5. You see this in each section
 * title
 * code
 * text
 * entry[].reference (To a resource later in the document)
 * entry[].display

6. Open the file samples/IPS_IG-bundle-01.json
7. In the Composition.section array, locate these:
 * Active Problems
 * Medication
 * Allergies and Intolerances
 * Ignore the other sections for now
8. Notes:
 * entry[].reference uses a different syntax to reference a resource than the previous document
 * entry[] does not contain a display property

9. Open samples/DK_Jens_Villadsen_01.json
10. Note that entry[].reference uses the syntax from the first sample document

11. Examine other sample documents. Reference can be:
 * urn:uuid:xxxx-yyyyy-zzzz
 * Resource/xxxx-yyyyy-zzzz

## Pages to Read (In Order)
* [FHIR Bundle](01_FHIR_Bundle.md)
* [Composition](02_Composition.md)
* [IPS Sections](03_IPS_Sections.md)
* [Header Sections](04_Header_Sections.md)
* [Required Sections](05_Required_Sections.md)
* [&rarr;  Full Resources](06_Full_Resources.md)
* [IPS_Document_Validation/README.md](../IPS_Document_Validation/README.md)